---
title: "不等式: 基本的な性質と例"
date: 2025-02-09
---

# 第1部

これは最初のテーマです。不等式の問題を解く際に、多くの人が困難に直面します。ある数が別の数より大きい理由を理解するのが難しい人もいます。しかし、現実世界では誰もが不等式に直面するため、このトピックは重要です。

## 基本的な性質

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

なお、(3) より、$-a$ から 0 までの距離と、0 から $a$ までの距離は等しいことがわかります。したがって、**符号に関係なく、距離は常に非負の量である** と言えます。現実世界では、2つの物体の間の距離は「存在する」か「存在しない」かのどちらかであり、負の距離は存在しません。このため、**絶対値** という概念が導入されます。これは、ある値が他の値とどれだけ離れているか、またはどれだけ上回っているかを示すものです。（絶対値については別の記事で詳しく説明します。）

![](/data/animation.gif)

### (3) から導かれる追加の性質

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

## いくつかの例

### 1. $x^{2} - x - 1 > 0$

解く前に、この不等式を **この不等式を満たす関数として表現できる** ことを確認しておきましょう。

$$
f(x) = y = x^{2} - x - 1 > 0 \quad \implies \quad y > 0
$$

*解答*:  
方程式 $x^{2} - x - 1 = 0$ の解を求め、関数 $f(x)=x^{2} - x - 1$ のグラフが $Ox$ 軸より上にある領域を特定します。

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

図を描きます:

![](/data/StaticParabola_ManimCE_v0.19.0.png)

最後に、この不等式の解を求めます。これは、グラフの曲線 ({{< color "yellow" >}}色付きの{{< /color >}}放物線の枝) が $Ox$ 軸の上にある領域です。

$$
x \in (-\infty; x_{1}) \cup (x_{2}; +\infty)
\quad \implies \quad
\boxed{x \in \left(-\infty; \frac{1-\sqrt{5}}{2}\right) \cup \left(\frac{1+\sqrt{5}}{2}; +\infty\right)}
$$
