# 极限

## 核心考点

（1）定义

（2）性质

（3）计算

（4）应用

## 一、极限的定义

### 1. 函数极限

$\lim\limits_{x \to x_0}f(x)=A \Leftto \forall \varepsilon > 0, \exist \delta > 0$，当$0 < |x-x_0| < \delta$ 时，有 $|f(x)-A| < \varepsilon$。

### 2. 数列极限

$\lim\limits_{x \to x_0}x_n=A \Leftto \forall \varepsilon > 0, \exist N > 0$，当$n > N$ 时，有 $|x_n-A| < \varepsilon$。

---

<div style='color: #2b73af'>

【例】以下三个命题：

①若数列$\{u_n\}$收敛于$A$，则其任意子数列$\{u_{n_{i}}\}$必定收敛于$A$；

②若单调数列$\{x_n\}$的某一子数列$\{x_{n_{i}}\}$收敛于$A$，则该数列必定收敛于$A$；

③若数列$\{x_{2n}\}$与$\{x_{2n+1}\}$都收敛于$A$，则数列$\{x_n\}$必定收敛于$A$。

正确的个数为（  ）

</div>

- [ ] <font style='color: #2b73af'>A.0</font>
- [ ] <font style='color: #2b73af'>B.1</font>
- [ ] <font style='color: #2b73af'>C.2</font>
- [x] <font style='color: #2b73af'>D.3</font>

## 二、极限的性质

### 1. 唯一性

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

---

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

### 2. 局部有界性

> 若$\lim \limits_{x \to x_0}f(x)=A$，则$\exist M>0,\delta>0$，当$0<|x-x_0|< \delta$时，恒有$|f(x)|<M$。

【证】$\forall \varepsilon > 0, \exist \delta > 0$，当$0 < |x-x_0| < \delta$ 时，有 $|f(x)-A| < \varepsilon$

故$|f(x)|=|f(x)-A+A| \leqslant |f(x)-A|+|A|$

取$\varepsilon=2019$（任意大于0的数均可）

∴$|f(x)| \leqslant 2019+|A|$

令$M=2019+|A|$，则

$|f(X)| < M$

---

<div style='color: #2b73af'>

【例】$f(x)=\frac{|x|\sin(x+2)}{x(x-1)(x-2)^2}$，在（  ）内有界。

</div>

- [x] <font style='color: #2b73af'>A.(-1,0)</font>
- [ ] <font style='color: #2b73af'>B.(0,1)</font>
- [ ] <font style='color: #2b73af'>C.(1,2)</font>
- [ ] <font style='color: #2b73af'>D.(2,3)</font>

【分析】对每个答案区间的左端点的+、右端点的-极限进行判断，若存在、且区间内函数连续，则为所求答案。

<font style='color: #cf455c'>【求解方法】</font>讨论$f(x)$在指定区间$I$上的有界性，方法如下：

①理论：连续函数在闭区间内必有界；

②若$I$为$(a,b)$，则当一下三个条件均成立时，$f(x)$有界

&emsp;A.$\lim \limits_{x \to a^+}f(x)$存在；

&emsp;B.$\lim \limits_{x \to b^-}f(x)$存在；

&emsp;C.$f(x)$在$(a,b)$内连续；


### 3. 局部保号性

若$\lim \limits_{x \to x_0}f(x)=A>0$，则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)>0$;

若$\lim \limits_{x \to x_0}f(x)=A<0$，则存在$\delta>0$，当$0<|x-x_0|<\delta$时，$f(x)<0$。

---

<div style='color: #2b73af'>

【例】设$\lim \limits_{x \to 0}f(x)=f(0)$，且$\lim \limits_{x \to 0}\frac{f(x)}{1-\cos x}=-2$，则$x=0$是___。

</div>

- [x] <font style='color: #2b73af'>A.极大值点</font>
- [ ] <font style='color: #2b73af'>B.极小值点</font>
- [ ] <font style='color: #2b73af'>C.非极值点</font>
- [ ] <font style='color: #2b73af'>D.无法判断</font>

【分析】$f(0)=\lim \limits_{x \to 0}f(x)=\lim \limits_{x \to 0} \frac{f(x)}{1-\cos x}(1-\cos x)=-2 \times 0=0$

∵$\lim \limits_{x \to 0} \frac{f(x)}{1-\cos x} = -2 <0$

∴$\frac{f(x)}{1-\cos x}  <0$

又$1-\cos x>0$

∴$f(x)<0$

∴$x=0$是极大值点

## 三、计算

1.函数极限（常规考法）

2.数列极限（一般为非常规考法、重点题、压轴题）

### 1. 函数极限的计算

#### （1）七种未定式（分三组）：

&emsp;A、$\frac00,\frac\infty\infty,\infty \cdot 0,$

&emsp;B、$\infty-\infty,$

&emsp;C、$\infty^0，0^0,1^\infty$

#### （2）计算工具：

&emsp;**A、洛必达法则：**

&emsp;&emsp;若$\lim f(x)=0(\infty), \lim g(x)=0(\infty)$，且$\lim \frac{f'(x)}{g'(x)}$存在，则$\lim \frac{f(x)}{g(x)}=\lim \frac{f'(x)}{g'(x)}$

&emsp;**B、等价无穷小替换：（$x \to 0$时）**

&emsp;&emsp;$\sin x \sim \tan x \sim \arcsin x \sim \arctan x \sim e^x-1 \sim \ln(1+x) \sim x$

&emsp;&emsp;$(1+x)^a-1 \sim ax$

&emsp;&emsp;$1-\cos x \sim \frac12 $

&emsp;&emsp;$a^x-1 \sim x\ln a$

&emsp;&emsp;$x-\sin x \sim \frac16x^3$

&emsp;&emsp;$x+\sin x \sim 2x$

&emsp;&emsp;$x^2-\sin ^2 x \sim \frac13 x^4$

&emsp;&emsp;$\tan x-x \sim \frac13 x^3$

&emsp;**C、重要极限：**

&emsp;&emsp;$\lim \limits_{x \to 0}  \frac{\sin x}{x}=1$

&emsp;&emsp;$\lim \limits_{x \to 0}(1+x)^{\frac1x}=e$

#### （3）计算方法：

<font style='color:#cf455c; font-weight:bold'>1、对于A类未定式:

1）、（$\frac00$）见式先化简：

&emsp;①恒等变形

&emsp;&emsp;A、见根号差，用有理化；

&emsp;&emsp;B、提公因式；

&emsp;&emsp;C、凑补法：+a-a、\*a/a；

&emsp;②等价无穷小替换

&emsp;③及时提出极限不为0的因式

2）、（$\infty \cdot 0$）转化为（$\infty \cdot \frac{1}{\frac{1}{0}}$或$0 \cdot \frac{1}{\frac{1}{\infty}}$）

&emsp;&emsp;原则：将简单因式放在分母（如$x^a,e^{ax}$）,复杂因式如（$\ln x, \arcsin x$等）
</font>

<div style='color: #2b73af'>

【例1】$\lim \limits_{x \to 0} \frac{\sqrt{1+\tan x}-\sqrt{1+\sin x}}{x \sqrt{1+\sin ^{2} x}-x}\left(\frac{0}{0}\right)$

【解】

原式

$=\lim \limits_{x \to 0} \frac{\tan x - \sin x}{x(\sqrt{1+\sin ^2x}-1)} \cdot \frac1{\sqrt{1+ \tan x}+\sqrt{1+\sin x}}$

$=\frac12 \lim \limits_{x \to 0} \frac{\tan x - \sin x}{x(\sqrt{1+\sin ^2x}-1)}$<font style='color:#4d4d4d'>（$\lim \limits_{x \to 0}\frac1{\sqrt{1+ \tan x}+\sqrt{1+\sin x}}=\frac12$）</font>

$=\frac12\lim \limits_{x \to 0}\frac{\tan x - \sin x}{x\cdot\frac12 \sin ^2x}$<font style='color:#4d4d4d'>（等价无穷小替换：$(1+t)^a-1 \sim at(t=\sin ^2x)$）</font>

$=\lim \limits_{x \to 0} \frac{ \tan x(1-\cos x)}{x\sin ^2x}=\lim \limits_{x \to 0} \frac{x \cdot \frac12x^2}{x \cdot x^2}=\frac12$

---

【例2】$\lim \limits_{x \to 0} \frac{\mathrm{e}^{x^{2}}-\mathrm{e}^{2-2 \cos x}}{x^{4}}\left(\frac{0}{0}\right)$

【解】

原式

$=\lim \limits_{x \to 0}\frac{e^{2-2\cos x}(e^{x^2-2+2\cos x}-1)}{x^4}$

$=\lim \limits_{x \to 0}\frac{e^{2-2\cos x}(x^2-2+2\cos x)}{x^4}$

$=\lim \limits_{x \to 0}\frac{x^2-2+2\cos x}{x^4}$

$=\lim \limits_{x \to 0}\frac{2x-2\sin x}{4x^3}$

$=\lim \limits_{x \to 0}\frac{2 \cdot \frac16 x^3}{4x^3}=\frac1{12}$

---

【例3】$\lim \limits_{x \to 1^{-}} \ln x \cdot \ln (1-x)$（$\infty \cdot 0$）

【解】

原式

$=\lim \limits_{x \to 1^-} \ln (1+x-1) \cdot \ln (1-x)$<font style='color:#4d4d4d'>（等价无穷小$\ln(1+t) \sim t$）</font>

$=\lim \limits_{x \to 1^-}(x-1) \ln (1-x)$

令$t=1-x$，则

原式

$=\lim \limits_{t \to 0^+}-t \ln t$

$=-\lim \limits_{t \to 0^+} \frac{\ln t}{\frac{1}{t}}$<font style='color:#4d4d4d'>（求导）</font>

$=-\lim \limits_{t \to 0^+} \frac{\frac1t}{-\frac{1}{t^2}}=\lim \limits_{t \to 0^+}t=0$

</div>

---

<font style='color:#cf455c; font-weight:bold'>2、对于B类未定式（$\infty-\infty$）:

1）、有分母，则通分为$\frac00$ 或 $\frac\infty\infty$；

2）、无分母，则创造分母（方法：令$x=\frac1t$）；

然后使用洛必达、等价无穷小等方法继续运算。

</font>

<div style='color: #2b73af'>

【例1】$\lim _{x \to 0}\left(\frac{e^{x}+x e^{x}}{e^{t}-1}-\frac{1}{x}\right)$

【解】

原式<font style='color:#4d4d4d'>（通分）</font>

$=\lim \limits_{x \to 0} \frac{xe^{x}+x^{2} e^{x}-e^{x}+1}{x(e^{x}-1)} (\frac{0}{0})$<font style='color:#4d4d4d'>（等价无穷小替换：$e^{x}-1 \sim x$）</font>

$=\lim \limits_{x \to 0} \frac{e^{x}(x^{2}+x-1)+1}{x\cdot x}$<font style='color:#4d4d4d'>（求导）</font>

$=\lim \limits_{x \to 0} \frac{e^{x}(x^{2}+3 x)}{2 x}$<font style='color:#4d4d4d'>（求导）</font>

$=\lim \limits_{x \to 0} \frac{e^{x}(x+3)}{2}$

$=\frac{3}{2}$

---

【例2】$\lim \limits_{x \to +\infty}\left[x^{2}\left(\mathrm{e}^{\frac{1}{x}}-1\right)-x\right]$

【解】令$x=\frac1t$，则

原式

$=\lim \limits_{t \to 0^+} \left[\frac{1}{t^{2}}\left(e^{t}-1\right)-\frac{1}{t}\right]$

$=\lim \limits_{t \to 0^{+}} \frac{e^{t}-1-t}{t^{2}}$

$=\lim \limits_{t \to 0^+} \frac{e^{t}-1}{2 t}$

$=\frac{1}{2}$

</div>

---

<font style='color:#cf455c; font-weight:bold'>3、对于C类未定式（$\infty^0，0^0,1^\infty$）:

使用公式：$U(x)^{V(x)}=e^{V(x) \cdot \ln U(x)}$

※ 当为$1^\infty$时：使用公式（$\lim U^V=e^{\lim V\cdot(U-1)}$）

</font>

<div style='color: #2b73af'>

【例1】$\lim \limits_{x \to +\infty}\left(x+\sqrt{1+x^{2}}\right)^{\frac{1}{x}}(\infty^0)$

【解】

原式

$=\lim \limits_{x \to +\infty} e^{\frac{\ln(x+\sqrt{1+x^{2}})}{x}}$<font style='color:#4d4d4d'>（求导:$(\frac{\ln(x+\sqrt{1+x^{2}})}{x})'=\frac{1}{\sqrt{1+x^{2}}}$）</font>

$=e^{\lim \limits_{x \to +\infty} \frac{1}{\sqrt{1+x^{2}}}}$<font style='color:#4d4d4d'>（求导）</font>

$=e^0$

$=1$

---

【例2】$\lim \limits_{x \to \frac{\pi}{4}}(\tan x)^{\frac{1}{\cos x-\sin x}}\left(1^{\infty}\right)$

【解】使用公式（$\lim U^V=e^{\lim V\cdot(U-1)}$）

原式

$=e^{\lim \limits_{x \to \frac{\pi}{4}} {\frac{1}{\cos x-\sin x}}\cdot(\tan x-1)}$

$=e^{\lim \limits_{x \to \frac{\pi}{4}} {\frac{\tan x-1}{-\cos x(\tan x-1)}}}$

$=e^{\lim \limits_{x \to \frac{\pi}{4}} {\frac{1}{-\cos x}}}$

$=e^{-\sqrt2}$

</div>

### 2. 数列极限的计算

#### （1）若数列$\{x_n\}$易于连续化，则可转为函数极限计算

依据：若$\lim \limits_{x \to +\infty} f(x)=A$，则$\lim \limits_{n \to \infty} f(n)=A$。

---

<div style='color: #2b73af'>

【例1】$\lim\limits_{n \to \infty}\left(n \cdot \tan \frac{1}{n}\right)^{n^{2}}$

【解】

∵ $\lim\limits_{x \to +\infty}\left(x \cdot \tan \frac{1}{x}\right)^{x^{2}}(1^\infty)$

$=e^{\lim \limits_{x \to +\infty}x^2(x \tan \frac1x -1)}$

令$x=\frac1t$，则

$=e^{\lim \limits_{t \to 0^+}\frac1{t^2}(\frac1t \tan t-1)}$

$=e^{\lim \limits_{t \to 0^+}\frac1{t^2}\frac{\tan t-t}{t}}$<font style='color:#4d4d4d'>（等价无穷小替换：$\tan t-t \sim \frac13 t^3$）</font>

$=e^{\lim \limits_{t \to 0^+}\frac{\frac13 t^3}{t^3}}$

$=e^{\frac13}$

由归结定理得，原式$=e^{\frac13}$

</div>

#### （2）若数列$\{x_n\}$不易于连续化时，用“夹逼定理”（或定积分定义）

&emsp;**A、当分子分母同时变化时，只动分母，不动分子**

---

<div style='color: #2b73af'>

【例1】求$\lim _{n \rightarrow \infty}\left(\frac{1}{n^{2}+n+1}+\frac{2}{n^{2}+n+2}+\cdots+\frac{n}{n^{2}+n+n}\right)$

【解】

∵ $\lim\limits_{x \to +\infty}\left(x \cdot \tan \frac{1}{x}\right)^{x^{2}}(1^\infty)$

$=e^{\lim \limits_{x \to +\infty}x^2(x \tan \frac1x -1)}$

令$x=\frac1t$，则

$=e^{\lim \limits_{t \to 0^+}\frac1{t^2}(\frac1t \tan t-1)}$

$=e^{\lim \limits_{t \to 0^+}\frac1{t^2}\frac{\tan t-t}{t}}$<font style='color:#4d4d4d'>（等价无穷小替换：$\tan t-t \sim \frac13 t^3$）</font>

$=e^{\lim \limits_{t \to 0^+}\frac{\frac13 t^3}{t^3}}$

$=e^{\frac13}$

由归结定理得，原式$=e^{\frac13}$

</div>