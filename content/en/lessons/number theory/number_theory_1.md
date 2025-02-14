---
title: "Part 1. Basic Concepts. Arithmetic of Remainders."
---

## Subject of Study

This section studies, strangely enough, numbers and their properties. We will examine some of them necessary for the start.

Let's start with the types of numbers. The image below shows the types of number sets as nested ellipses. We will move from the smaller to the larger:


$$
\mathbb{P} \subset \mathbb{N} \subset \mathbb{Z} \subset \mathbb{Q} \subset \mathbb{R} \subset \mathbb{C}
$$

![](/data/number_theory.svg)

What do these letters mean?

$\mathbb{P}$ — the set of prime numbers. Prime numbers are those that are divisible by themselves and by one. The set of prime numbers is not actually a strict subset of natural numbers. True mathematicians may criticize me for the picture I made and for what I wrote, but I will explain my choice as follows: any element (number) of the prime set is also an element of any higher set.
In this section, we will often work with prime numbers because of their unique properties.

*Note*: One is **not** a prime number because it is only divisible by itself.

Examples of prime numbers: {$2, ~ 3, ~ 5, ~ 7, ~ 11, ~ 13, ~~ \dots$}

---

$\mathbb{N}$ — the set of natural numbers. These are the numbers familiar to us from a young age, those we can use to count the number of objects or our age in years. The set of natural numbers includes **one** as a fundamental building block, with which other numbers in this set are constructed. In fact, any number from the set of prime numbers can also be constructed using ones: $2 = 1+1; ~ ~ ~  5= ~ 1 + 1 + 1 + 1 + 1$ and so on...

*Note*: In my lessons, I will consider natural numbers to start from one.

---

$\mathbb{Z}$ — the set of integers. It is defined as the union of the set of natural numbers, zero, and negative natural numbers ($\mathbb{Z} = ~ -\mathbb{N} ~ \cup ~ \{0\} ~ \cup ~ \mathbb{N}$)

---

$\mathbb{Q}$ — the set of rational numbers. These are numbers that can be represented as a fraction: $$ \frac{a}{b}, \quad \text{where } a \in \mathbb{Z}, \quad b \in \mathbb{N} $$
In other words, **rational numbers** are numbers that can be written as the ratio of two integers, where the denominator is not zero.

Rational numbers include:
- All **integers**, as any integer can be written as a fraction (e.g., $5 = \frac{5}{1}$).
- All **common fractions**.
- All **finite and repeating decimals** (e.g., $0.3333\ldots = \frac{1}{3}$). However, **not all numbers are rational**. For example, $\pi$ and $\sqrt{2}$ are not rational because they cannot be represented as the ratio of two integers.

---

$\mathbb{R}$ — the set of real numbers. These are **all numbers that can be represented on the number line**. The set of real numbers includes:
- **All rational numbers** ($\mathbb{Q}$).
- **All irrational numbers** — numbers that **cannot be written as a fraction** $\frac{a}{b}$ (e.g., $\pi$, $e$, $\sqrt{2}$). Examples of real numbers: $$ \{-3, \quad 0, \quad \frac{4}{5}, \quad \sqrt{2}, \quad \pi, \quad e \}$$
Real numbers can be divided into **rational** and **irrational**:
- **Rational** — these are finite or repeating decimals.
- **Irrational** — these are infinite **non-repeating** decimals, for example: $$ \pi = 3.1415926535\ldots $$ $$ \sqrt{2} = 1.4142135623\ldots $$
The set **$\mathbb{R}$ is a continuous line of numbers**, unlike the discrete sets **$\mathbb{Z}$ and $\mathbb{N}$**.

---

$\mathbb{C}$ — the set of complex numbers.

Complex numbers are a **generalization** of real numbers $\mathbb{R}$. They are introduced to solve equations that have no solutions in $\mathbb{R}$. For example, the equation:
$$ x^2 + 1 = 0 $$
has no real roots because **no number** squared gives a negative value. Complex numbers can be useful in a number of number theory problems, but we will not delve into them for now.

---

### Some Useful Notations

| Notation              | Description                                                   |
| --------------------- | ------------------------------------------------------------- |
| $[x]$                 | Integer part of $x$ (the largest integer not exceeding $x$)   |
| $\lbrace x \rbrace$   | Fractional part of $x$: $\lbrace x \rbrace = x − [x]$         |
| $n!$                  | Factorial: $n! = 1 \cdot 2 \cdot \dots \cdot n$               |
| $\{x_n\}$             | Sequence $x_1, x_2, \dots, x_n$                               |
| $b \mid a$            | $b$ divides $a$                                               |
| $a ~~ \vdots ~~ b$    | $a$ is a multiple of $b$                                      |
| $a \equiv b \pmod{m}$ | $a$ is congruent to $b$ modulo $m$                            |
| $a \perp b$           | $a$ and $b$ are coprime                                       |

---

### **Congruence of Numbers**

If $m > 1$ and $(a - b) ~ \vdots ~ m$, then **$a$ and $b$ are congruent modulo $m$**.

Congruence is written as:
$$
a \equiv b \pmod{m}
$$

If the value of the modulus is clear from the context, the parentheses with the modulus are **usually omitted**.

Using the notation $a \equiv b \pmod{m}$ instead of the expression $(a - b) ~ \vdots ~ m$ turns out to be a **very convenient and powerful tool** in various problems, because **congruences** can be handled almost like **ordinary equalities**:

- **Addition**: if $a \equiv b \pmod{m}$ and $c \equiv d \pmod{m}$, then
  $$
  (a + c) \equiv (b + d) \pmod{m}
  $$

- **Subtraction**:
  $$
  (a - c) \equiv (b - d) \pmod{m}
  $$

- **Multiplication**:
  $$
  (a \cdot c) \equiv (b \cdot d) \pmod{m}
  $$

In some cases, it is possible to **divide** by a number if it is coprime with $m$.
But be especially careful when dividing!

