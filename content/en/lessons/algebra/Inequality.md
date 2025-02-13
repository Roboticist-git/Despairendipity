---
title: "Inequalities: Basic Properties and Examples"
date: 2025-02-09
---

# Part I.

This is the first topic we will discuss. Many people struggle with solving inequality problems, and some find it difficult to understand why one quantity is greater than another. However, inequalities are encountered in real life, making this topic essential.

## Basic Properties

$$
\begin{cases}
a < b \\[10pt]
b < c
\end{cases}
\quad \implies \quad a < c \tag{1}
$$

$$
a < b \implies a \pm m < b \pm m \tag{2}
$$

$$
a < b \quad\iff\quad -a > -b \tag{3}
$$

![](/data/lineX.svg)

From (3), we can see that the distance (interval length) from $-a$ to 0 and from 0 to $a$ is the same. Therefore, **we can say** that regardless of the sign of the numbers, the distance itself is **always non-negative**. In the real world, the distance between two objects either exists or does not; it cannot be negative. This leads to the concept of absolute value, which represents the strict difference between objects—how much one entity lags behind or surpasses another. (More on absolute value in a separate article.)

![](/data/animation.gif)

### Additional Properties Derived from (3)

$$
\begin{cases}
a < b \\[10pt]
c > 0
\end{cases}
\quad \implies \quad a \cdot c < b \cdot c \tag{4}
$$

$$
\begin{cases}
a < b \\[10pt]
c < 0
\end{cases}
\quad \implies \quad a \cdot c > b \cdot c \tag{5}
$$

## Some Examples

### 1. $x^{2} - x - 1 > 0$

Before solving, let’s agree that this inequality can be represented **as a function satisfying this inequality**, namely:

$$
f(x) = y = x^{2} - x - 1 > 0 \quad \implies \quad y > 0
$$

*Solution*:  
Find the roots of the **equation** $x^{2} - x - 1 = 0$ and determine the region on the coordinate plane where the function $f(x)=x^{2} - x - 1$ is above the $Ox$ axis.

$$
x^{2} - x - 1 > 0
$$

$$
D = (-1)^{2} - 4\cdot 1 \cdot (-1) = 1 + 4 = 5
$$

$$
\begin{cases}
x_{1} = \frac{-(-1) - \sqrt{5}}{2} = \frac{1 - \sqrt{5}}{2} \\[10pt]
x_{2} = \frac{-(-1) + \sqrt{5}}{2} = \frac{1 + \sqrt{5}}{2}
\end{cases}
$$

$$
(x - x_{1})\cdot (x - x_{2}) > 0 \quad \implies \quad \left(x - \frac{1+\sqrt{5}}{2}\right) \cdot \left(x - \frac{1-\sqrt{5}}{2}\right) > 0
$$

Drawing:

![](/data/StaticParabola_ManimCE_v0.19.0.png)

Finally, the solution for this inequality consists of the intervals on the $Ox$ axis where the curve ({{< color "yellow" >}}colored{{< /color >}} branches of the parabola) is above the axis:

$$
x \in (-\infty; x_{1}) \cup (x_{2}; +\infty)
\quad \implies \quad
\boxed{x \in \left(-\infty; \frac{1-\sqrt{5}}{2}\right) \cup \left(\frac{1+\sqrt{5}}{2}; +\infty\right)}
$$
