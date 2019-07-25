# 极限

## 1. 极限的定义

$\lim\limits_{x \to x_0}f(x)=A \Leftrightarrow \forall \varepsilon > 0, \exist \delta > 0$，当$0 < |x-x_0| < \delta$ 时，有 $|f(x)-A| < \varepsilon$。

## 2. 极限的性质

1. **唯一性**

    > 如果$\lim \limits_{x \to x_0}f(x)=A, \lim \limits_{x \to x_0}f(x)=B$，那么$A=B$。
    
【证】（反证法）

假设$\lim \limits_{x \to x_0}f(x)=B,A \ne B$，且$A>B$，则

$\forall \varepsilon > 0, \exist \delta_1 > 0$，当$0 < |x-x_0| < \delta_1$ 时，$|f(x)-A| < \varepsilon$

$\forall \varepsilon > 0, \exist \delta_2 > 0$，当$0 < |x-x_0| < \delta_2$ 时，$|f(x)-A| < \varepsilon$

取$\delta = min\{\delta_1, \delta_2\}$，则

$$A - \varepsilon < f(x) < A + \varepsilon \\ B - \varepsilon < f(x) < B + \varepsilon$$

取 $\varepsilon=\frac{A-B}{2}$,则

$$\frac{A+B}{2} < f(x) < \frac{3A-B}{2} \\ \frac{3B-A}{2} < f(x) < \frac{A+B}{2}$$

所以 $\frac{3A-B}{2} = \frac{3B-A}{2}$,得$A=B$,这与假设$A \ne B$相违背，所以假设不成立，故A唯一。

<div style='color: #2b73af'>

【例】设$a$为常数，$I= \lim \limits_{x \to 0}(\frac{e^{\frac{1}{x}}-\pi}{e^{\frac{2}{x}}+1} + a\arctan \frac{1}{x})$存在，求 $a,I$。

<details>
<summary style='color: red'>点击查看答案</summary>

【分析】

从$x \to 0$来看，应从$x \to 0^+$，$x \to 0^-$两个方面来分析；
① $x \to 0^+$时，
$$\lim \limits_{x \to 0^+}(\frac{e^{\frac{1}{x}}-\pi}{e^{\frac{2}{x}}+1} + a\arctan \frac{1}{x})=a\frac{\pi}{2}$$

② $x \to 0^-$时，
$$\lim \limits_{x \to 0^-}(\frac{e^{\frac{1}{x}}-\pi}{e^{\frac{2}{x}}+1} + a\arctan \frac{1}{x})=-\pi-a\frac{\pi}{2}$$

∴ $a\frac{\pi}{2}=-\pi-a\frac{\pi}{2}$

∴ $a=-1,  I=-\pi/2$

</details>
</div>

2. **局部有界性**



3. **局部保号性**