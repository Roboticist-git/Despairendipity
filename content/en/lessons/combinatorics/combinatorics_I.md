---
title: "Combinatorics"
date: 2025-02-10
---
# Part I.

What is combinatorics? It is a branch of mathematics that studies methods of selecting, ordering, and counting various configurations of elements. What can be considered “elements”? They can be physical objects as well as abstract mathematical entities, such as numbers, sets, or graphs.

Here we will examine the basic principles of combinatorics: the principles of addition and multiplication, as well as the concepts of **permutations**, **combinations**, and **arrangements**.

#### Principle of Addition:

We have 100 coins (insert any currency name) to buy some food.
Upon arriving at the store, we have a “choice”: onigiri for 99 coins, a burger for 100 coins, as well as a soda for 70 coins, coffee for 100 coins, and ice cream for 65 coins.

How many ways are there to buy something from what is available?

Well, out of these 5 options, we can pick **just one** of them $\implies$ a total of 5 ways.

🔹Formally: in combinatorics, addition means that we sum all the possible **independent** ways and get the total number of possible ways.

#### Principle of Multiplication:

When getting ready in the morning for classes, we need to decide how to dress today:

Top: black shirt ($A$), black hoodie ($B$), gray T-shirt ($C$)  
Bottom: black jeans ($D$), dark blue pants ($E$)

Let’s create a table of possible outfit options:

| Top  | Bottom |                                   |
| ---- | ------ | --------------------------------- |
| $A$  | $D$    | Black shirt and black jeans       |
| $A$  | $E$    | Black shirt and dark blue pants   |
| $B$  | $D$    | Black hoodie and black jeans      |
| $B$  | $E$    | Black hoodie and dark blue pants  |
| $C$  | $D$    | Gray T-shirt and black jeans      |
| $C$  | $E$    | Gray T-shirt and dark blue pants  |

As we can see from the table, we have 6 combinations. What’s the point? We can’t leave the house without wearing pants or with a bare torso (well, presumably we can’t). Nonetheless, we can combine our clothes in many ways to bring at least some variety to daily life... Also, when we put on pants and a top, it **doesn’t matter** which we put on first or second. Why make this point? We’ll see later that in some situations, the **order** of elements plays a crucial role.

🔹Formally: if the first choice can be made in $m$ ways, and the second in $n$ ways, then the total number of options is $n \cdot m$.

---

## Permutations, Arrangements, and Combinations

Now let’s look at the main ways to **select and order elements**.

### Permutations

We have $n$ different elements, and we want to order them.

**How many ways can we do that?**

Suppose we have **3 books** ($A$, $B$, $C$), and we want to place them on a shelf in various orders.

The first book can be chosen in **3 ways**, the second in **2 ways**, and the third will automatically end up in its place.

The total number of ways to arrange 3 books is $P(3) = 3! = 3 \cdot 2 \cdot 1 = 6$.

**General case:**

If we have $n$ elements, then the number of **permutations** of all elements is:
$$
P(n) = n!
$$  
*Note*: here the notation "$n!$" means we compute the **factorial** of $n$, i.e., the product of all numbers from 1 to $n$ ($1 \cdot 2 \cdot 3 \cdot 4 \cdot \dots \cdot n$).

🔹 **Example:** In how many ways can we arrange 5 different books on a shelf?
$$
P(5) = 5! = 5 \cdot 4 \cdot 3 \cdot 2 \cdot 1 = 120
$$

---

### Combinations

Next, let’s consider the situation where **order does not matter**.

For example, we have **10 students**, and we want to select **3** of them to send to a competition (or for a retake).

Choosing **A, B, C** and **C, A, B** is **the same choice**, since order does not matter.

The formula for **combinations** $C(n, k)$ is:
$$
C(n, k) = \frac{n!}{k!(n-k)!}
$$

🔹 **Example:** How many ways can we choose 3 students out of 10?
$$
C(10,3) = \frac{10!}{3!(10-3)!} = \frac{10!}{3!7!} = \frac{10 \cdot 9 \cdot 8}{3 \cdot 2 \cdot 1} = 120
$$

🔹 **What’s going on here?**

First we calculate **arrangements** ($A(n, k)$), which includes all permutations.  
To eliminate the redundant consideration of **order**, we divide by $k!$ (the number of ways to permute $k$ elements).

---

### Combinations with Repetitions

If elements **can be repeated**, we use **combinations with repetitions**:
$$
\widetilde{C}(n, k) = C(n+k-1, k) = \frac{(n+k-1)!}{k!(n-1)!}
$$

🔹 **Example:** We have 5 types of flowers, and we want to choose 3 bouquets (flowers may repeat).
$$
\widetilde{C}(5,3) = \frac{(5+3-1)!}{3!(5-1)!} = \frac{7!}{3!4!} = 35
$$

---

### Arrangements (= combinations with order)

Now consider the case when we have **more objects than we choose**.

For example, we have **8 participants**, and we need to select **3 prize places** (first, second, and third).

Order matters: if we pick **A, B, C**, that is **not** the same as **B, C, A**.

The formula for **arrangements** $A(n, k)$ is:
$$
A(n, k) = \frac{n!}{(n-k)!}
$$

🔹 **Example:** How many ways can we choose 3 winners out of 8 participants?
$$
A(8,3) = \frac{8!}{(8-3)!} = \frac{8!}{5!} = 8 \cdot 7 \cdot 6 = 336
$$

🔹 **What’s going on here?**

For first place we choose from **8 participants**.  
For second place, from the **7 remaining**.  
For third place, from the **6 remaining**.

Hence, we multiply these three numbers, which gives us the **arrangement** formula.

**Note:** Arrangements are essentially **combinations with order**.  
First, we choose **k elements** (as in combinations), then **order them** (as in permutations):
$$
A(n, k) = C(n, k) \cdot k!
$$

---

### Arrangements with Repetitions

If we can **choose the same element multiple times**, a different formula is used:
$$
\widetilde{A}(n, k) = n^k
$$

🔹 **Example:** We have 10 types of ice cream, and we want to choose 4 servings (possibly the same flavor).
$$
\widetilde{A}(10,4) = 10^4 = 10000
$$

---

## **Summary**

| Name                          | Formula                                             | Order Matters? | Example                              |
| ----------------------------- | --------------------------------------------------- | -------------- | ------------------------------------- |
| **Permutations**             | $P(n) = n!$                                         | ✅ Yes          | Arranging 5 books on a shelf          |
| **Arrangements**             | $A(n, k) = \frac{n!}{(n-k)!}$                       | ✅ Yes          | Choosing 3 winners out of 8           |
| **Arrangements with Reps**   | $\widetilde{A}(n, k) = n^k$                         | ✅ Yes          | Choosing 4 servings of ice cream      |
| **Combinations**             | $C(n, k) = \frac{n!}{k!(n-k)!}$                     | ❌ No           | Choosing 3 students out of 10         |
| **Combinations with Reps**   | $\widetilde{C}(n, k) = \frac{(n+k-1)!}{k!(n-1)!}$   | ❌ No           | Choosing 3 bouquets of flowers        |

---

## Some Examples

#### 1. How many ways are there to place 5 *different* chess pieces on a board?

The first thing to note: the simple permutation formula, like in the case of books on a shelf, doesn’t work here.

We can place the first piece in 64 ways, the second in 63 ways, the third in 62 ways, and so on.

This is **arrangements**: 5 pieces, 64 squares

$$
\boxed{A(64,5) = \frac{64!}{59!} = 64 \cdot 63 \cdot 62 \cdot 61 \cdot 60}
$$

What if the pieces were **identical and indistinguishable**?

In essence, we can place our **identical pieces** in exactly the same number of ways, but then the question arises: do we need to consider permutation factors? All pieces are indistinguishable, and if we swap any two, the arrangement is exactly the same; nothing has changed. Permuting identical objects is pointless... No matter how hard we try, desperately rearranging identical, template-made pieces, the result remains the same. We can only place them on the board, not rearrange them among themselves... As a result, the number of ways to place 5 identical pieces on the board is the number of **arrangements**, but **without** accounting for permutations.  
Recalling the principle of multiplication, in this case we have to divide instead:

$$
\boxed{C(64,5) = \frac{A(64,5)}{P(5)} = \frac{64!}{5!(64-5)!}}
$$
