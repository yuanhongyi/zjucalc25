
# 函数极限、连续函数、函数的导数

## 基础回顾

### 函数极限

**1. 函数极限定义: $\varepsilon - \delta$ 语言**



**定义 2.1.1** 设 $f: D \to \mathbb{R}$, $D$ 是 $\mathbb{R}$ 的子集且包含 $x_0$ 的某去心邻域, 如果存在 $A \in \mathbb{R}$, 使得对于任意的 $\varepsilon > 0$, $\exists \delta > 0$, 当 $x \in \mathring{U}(x_0, \delta) \cap D$ 时, 有

$$|f(x) - A| < \varepsilon,$$

就称当 $x$ 趋于 $x_0$ 时, $f(x)$ 趋于 $A$, 记为

$$ \lim\limits_{x \to x_0} f(x) = A \quad \text{或者} \quad f(x) \to A, x \to x_0. $$

此时称 $A$ 是 $f$ 在 $x_0$ 处的极限, 如果不存在满足要求的 $A$, 就称 $f$ 在 $x_0$ 处的极限不存在.

> **【注1】** 定义 2.1.1 中我们不要求 $f$ 在 $x_0$ 处有定义, 即使 $f$ 在 $x_0$ 处有定义, 极限 $A$ 也不一定与 $f(x_0)$ 相等.

> **【注2】** 定义 2.1.1 中, “当 $x \in \mathring{U}(x_0, \delta) \cap D$ 时” 可写为 “在 $D$ 内当 $0 < |x - x_0| < \delta$ 时”.

*   单侧极限, 无穷处的极限

**2. 归结原理/海涅定理: 建立数列极限与函数极限的关系**

**定理 2.1.5 (归结原理)** 设 $f: D \subset \mathbb{R} \to \mathbb{R}$, $\mathring{U}(x_0) \subset D$, 则 $\lim\limits_{x \to x_0} f(x) = A$ 的充要条件是: 对于任意满足 $\lim\limits_{n \to \infty} x_n = x_0$, $x_n \neq x_0, n=1,2,3,...$ 的数列 $\{x_n\}$, 其对应的函数值数列 $\{f(x_n)\}$ 均有 $\lim\limits_{n \to \infty} f(x_n) = A$.

**3. 性质: 唯一性, 局部有界性, 局部保号性, 四则运算(类比数列极限性质)**

**4. 两个重要极限**

*   $\lim\limits_{x \to 0} \dfrac{\sin x}{x} = 1$

*   $\lim\limits_{x \to \infty} (1 + \frac{1}{x})^x = e$ 或者 $\lim\limits_{x \to 0} (1+x)^{\frac{1}{x}} = e$

---

### **函数连续性**

**1. 函数在某点连续**

**定义 2.2.1** 设 $f: D \subset \mathbb{R} \to \mathbb{R}$, $D$ 包含 $x_0$ 的某个邻域, 如果

$$ \lim\limits_{x \to x_0} f(x) = f(x_0), $$

就称 $f$ 在 $x_0$ 处连续.

$f$ 在 $x_0$ 处连续也可以用 “$\varepsilon - \delta$” 语言表述如下:

$$ \forall \varepsilon > 0, \exists \delta > 0, \text{当} |x-x_0| < \delta \text{时, 有} |f(x) - f(x_0)| < \varepsilon. $$


**2. 函数在某点的连续性对加减法, 乘法封闭, 除法要求分母不为0**

**3. 复合函数, 反函数的连续性**

**定理 2.2.7 (复合函数的连续性)** 设 $y=f(x)$ 在 $x_0$ 处连续, $y_0 = f(x_0)$, $z=g(y)$ 在 $y_0$ 处连续, 则复合函数 $z=g(f(x))$ 在 $x_0$ 处连续.

**4. 间断点的定义**

连续要求函数值存在并且等于在该点的左右极限.

**定义 2.2.12**

(1)**第一类间断点** 

如果左极限 $\lim\limits_{x \to x_0^-} f(x)$ 和右极限 $\lim\limits_{x \to x_0^+} f(x)$ 都存在但 $f$ 在 $x_0$ 处不连续, 就称 $x_0$ 是 $f$ 的**第一类间断点**. 特别地, 如果左极限和右极限都存在但不相等, 就称 $x_0$ 是 $f$ 的**跳跃间断点**; 如果极限 $\lim\limits_{x \to x_0} f(x)$ 存在, 但极限值不等于 $f(x_0)$ 或者 $f$ 在 $x_0$ 处没有定义, 就称 $x_0$ 是 $f$ 的**可去间断点**.

(2)**第二类间断点** 

如果 $f$ 在 $x_0$ 处的左极限和右极限至少有一个不存在, 就称 $x_0$ 是 $f$ 的**第二类间断点**.

**5. 函数在一个区间上连续, 一致连续性**

**定义 2.2.9** 设 $f: [a,b] \to \mathbb{R}$ ($a<b$). 如果 $f$ 在开区间 $(a,b)$ 内连续, 在 $a$ 处右连续, 在 $b$ 处左连续, 就称 $f$ 在闭区间 $[a,b]$ 上连续.



**定义 2.2.14** 设函数 $f: I \to \mathbb{R}$, 如果 $\forall \varepsilon > 0$, $\exists \delta > 0$, 使得 $\forall x_1, x_2 \in I$, 当 $|x_1 - x_2| < \delta$ 时, 都有 $|f(x_1) - f(x_2)| < \varepsilon$, 就称函数 $f$ 在区间 $I$ 上是**一致连续**的.



从一致连续的定义可以看出, 若 $f$ 在区间 $I$ 上一致连续, 则 $f$ 在区间 $I$ 上一定是连续的, 而反之不然.



*   一致连续的几何意义?



> **【思考】**:

> *   连续函数 $\pm$ 连续函数一定是连续函数

> *   不连续函数 $\pm$ 不连续函数可能是不连续函数, 也可能是连续函数.

>     $f(x) = \mathrm{sgn}(x), g(x) = -\mathrm{sgn}(x)$

> *   连续函数 $\pm$ 不连续函数一定是不连续函数(反证法)

> *   连续 $\times$ 不连续可能是连续, 可能是不连续

>     $f(x) = |x|, g(x) = \mathrm{sgn}(x)$

---

### **无穷小和无穷大**

1.  低阶无穷小, 同阶无穷小, 等价无穷小, 高阶无穷小

2.  一个性质: 有界量 $\times$ 无穷小 = 无穷小

3.  有限个无穷小相加还是无穷小(无限个不一定)

4.  常见的等价无穷小 ($x \to 0$):

    *   (1) $\sin x \sim x, \quad 1 - \cos x \sim \dfrac{1}{2}x^2, \quad \tan x \sim x$;
    *   (2) $\ln(1+x) \sim x$;
    *   (3) $e^x - 1 \sim x$;
    *   (4) $(1+x)^\alpha - 1 \sim \alpha x$;
    *   (5) $\arcsin x \sim x, \quad \arctan x \sim x$.
    *   (6) $\tan x - \sin x \sim \dfrac{1}{2}x^3$
    *   (7) $x - \sin x \sim \dfrac{1}{6}x^3$(你能不用泰勒公式、洛必达法则证明吗)

    这一部分与后面泰勒公式联系很紧密（实则为带peano余项的一阶Taylor公式）.


---

### **闭区间上的连续函数**



1.  有界, 存在最值

2.  零点存在定理 $\Rightarrow$ 介值定理

---

### **函数的导数**

**1. 某点导数的定义:**

$$ f'(x_0) = \lim\limits_{x \to x_0} \frac{f(x) - f(x_0)}{x - x_0} \quad \text{或者} \quad f'(x_0) = \lim\limits_{\Delta x \to 0} \frac{f(x_0 + \Delta x) - f(x_0)}{\Delta x} $$

**2. 导函数:**

$$ f'(x) = \lim\limits_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x} $$

**3. 单侧导数:** $f'_+(x_0), f'_-(x_0)$, 实际为导数定义变成单侧极限

**4. 可导性与连续性的关系: 可导必连续, 连续不一定可导**

**5. 常见函数的导数, 导数四则运算, 复合函数求导: 和高中学的一样**

**6. 反函数的导数:** $\dfrac{\mathrm{d}x}{\mathrm{d}y} = \dfrac{1}{\frac{\mathrm{d}y}{\mathrm{d}x}}$

**8. 隐函数求导:** 方程两边对 $x$ 同时求导, 注意把 $y$ 看作 $x$ 的函数

**9. 参数方程求导:**

$$ \begin{cases} x = a(t) \\ y = b(t) \end{cases} \quad \implies \quad \frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t} = \frac{b'(t)}{a'(t)} $$

**10. 极坐标求导:**

$r = \rho(\theta) \implies x = r \cos\theta, y = r \sin\theta \Rightarrow$ 参数方程求导

**11. 高阶导数, 莱布尼兹公式, 参数方程求二阶导数**

设函数 $u(x)$ 和 $v(x)$ 都具有 $n$ 阶导数，则它们的乘积 $(uv)$ 的 $n$ 阶导数为：

$$ (uv)^{(n)} = \sum_{k=0}^{n} C_n^k u^{(k)} v^{(n-k)} $$

**12. 微分:** $\mathrm{d}y = f'(x)\mathrm{d}x$ 或者 $\mathrm{d}f(x) = f'(x)\mathrm{d}x$

---

## **习题选讲**


**$1^\infty$**

**取对数或者指数恒等变形**

**7. 已知 $\lim\limits_{x \to \infty} \left(\frac{x+a}{x-a}\right)^x = 2$, 试求常数 $a$ 的值。**

**解:** 由题可知

$$ \lim\limits_{x \to \infty} \left(\frac{x+a}{x-a}\right)^x = \lim\limits_{x \to \infty} \left(1 + \frac{2a}{x-a}\right)^x = \lim\limits_{x \to \infty} \left[ \left(1 + \frac{2a}{x-a}\right)^{\frac{x-a}{2a}} \right]^{\frac{2ax}{x-a}} = e^{\lim\limits_{x\to\infty} \frac{2ax}{x-a}} = e^{2a} $$

故 $e^{2a} = 2$, 解得 $a = \frac{\ln 2}{2}$.



**10. 求极限 $\lim\limits_{n\to\infty} (1+x)(1+x^2)\cdots(1+x^{2^n})$ 的值。**

**解:**

当 $x=-1$ 时有 $1+x=0$, 则原极限为 $0$.

当 $x=1$ 时有 $(1+x)(1+x^2)\cdots = 2 \times 2 \times \cdots \times 2 = 2^{n+1}$, $\lim\limits_{n\to\infty} 2^{n+1} = +\infty$.

即当 $x=1$ 时, 极限不存在.

此时考虑 $|x| \neq 1$ 时, 则有

$$ \begin{aligned} (1+x)(1+x^2)\cdots(1+x^{2^n}) &= \frac{(1-x)(1+x)(1+x^2)\cdots(1+x^{2^n})}{1-x} \\ &= \frac{(1-x^2)(1+x^2)\cdots(1+x^{2^n})}{1-x} \\ &= \frac{1-x^{2^{n+1}}}{1-x} \end{aligned} $$

此时只需考察 $\lim\limits_{n\to\infty} x^{2^{n+1}}$.

容易知道, $|x|<1$ 时有 $\lim\limits_{n\to\infty} x^{2^{n+1}} = 0$; $|x|>1$ 时 $\lim\limits_{n\to\infty} x^{2^{n+1}}$ 不存在.

则 $|x|<1$ 时有:

$$ \lim\limits_{n\to\infty} (1+x)(1+x^2)\cdots(1+x^{2^n}) = \lim\limits_{n\to\infty} \frac{1-x^{2^{n+1}}}{1-x} = \frac{1-0}{1-x} = \frac{1}{1-x} $$

综上, $x=-1$ 时原极限值为 $0$; $-1<x<1$ 时原极限值为 $\frac{1}{1-x}$; $|x| \ge 1$ 时原极限不存在.

!!! Tips
    实际上本题乘积恰好等于**$1+x+x^2+\dots+x^{2^{n+1}-1}$ 等比数列求和**，蕴含了二进制与母函数的背景。


**根号常用手法: 有理化, 看作分数指数幂**

**$\lim\limits_{x\to+\infty} (\sin\sqrt{x^2+1} - \sin x)$**

$$ \begin{aligned} \lim\limits_{x\to+\infty} (\sin\sqrt{x^2+1} - \sin x) &= \lim\limits_{x\to+\infty} 2\cos\frac{\sqrt{x^2+1}+x}{2} \sin\frac{\sqrt{x^2+1}-x}{2} \\ &= \lim\limits_{x\to+\infty} 2\cos\frac{\sqrt{x^2+1}+x}{2} \sin\frac{1}{2(\sqrt{x^2+1}+x)} \end{aligned} $$

因为 $\cos\frac{\sqrt{x^2+1}+x}{2}$ 有界, 而 $\lim\limits_{x\to+\infty} \sin\frac{1}{2(\sqrt{x^2+1}+x)} = \sin 0 = 0$.

所以原极限 = 0.



---



**45. 当 $x \to 0^+$ 时, 求下列无穷小量关于 $x$ 的无穷小阶数.**

(1) $\sqrt{x+\sqrt{x+\sqrt{x}}}$; 

(2) $x^2\sin^{\frac{1}{k}}x$, $k$ 为正整数; 

(3) $\ln(1+x)-\ln(1-x)$; 

(4) $\sqrt{1+\tan x} - \sqrt{1+\sin x}$;



**(4) 设阶数为 $\alpha$, 则应有 $\lim\limits_{x\to 0^+} \frac{\sqrt{1+\tan x} - \sqrt{1+\sin x}}{x^\alpha} \neq 0$.**

又因为

$$ \begin{aligned} \lim\limits_{x\to 0^+} \frac{\sqrt{1+\tan x} - \sqrt{1+\sin x}}{x^\alpha} &= \lim\limits_{x\to 0^+} \frac{(1+\tan x) - (1+\sin x)}{x^\alpha(\sqrt{1+\tan x} + \sqrt{1+\sin x})} \\ &= \lim\limits_{x\to 0^+} \frac{\tan x - \sin x}{2x^\alpha} \\ &= \lim\limits_{x\to 0^+} \frac{\sin x(1-\cos x)}{2x^\alpha \cos x} \\ &= \lim\limits_{x\to 0^+} \frac{x \cdot \frac{1}{2}x^2}{2x^\alpha} = \lim\limits_{x\to 0^+} \frac{1}{4} x^{3-\alpha} \end{aligned} $$

上述极限若不为 $0$ 且存在, 则只能有 $3-\alpha=0$, 解得 $\alpha=3$.

故无穷小量 $\sqrt{1+\tan x} - \sqrt{1+\sin x}$ 关于 $x$ 的无穷小阶数为 $3$.



---

**介值定理**



**60. 设 $f(x)$ 在闭区间 $[a,b]$ 上连续, 试证:**

**(1) 若 $\alpha_1, \alpha_2$ 是满足 $\alpha_1 + \alpha_2 = 1$ 的正实数, 则至少存在一点 $\xi \in [a,b]$, 使得 $\alpha_1 f(a) + \alpha_2 f(b) = f(\xi)$;**

**(2) 对任意正实数 $k_1, k_2$, 至少存在一点 $\eta \in [a,b]$, 使得 $k_1 f(a) + k_2 f(b) = (k_1+k_2)f(\eta)$.**



**证明:**

(1) 由最大值最小值定理, 则 $f(x)$ 在闭区间 $[a,b]$ 上有最值, 设最大值为 $M$, 最小值为 $m$.

则此时有 $m \le f(a) \le M, m \le f(b) \le M$ 成立.

由 $\alpha_1, \alpha_2 > 0$ 从而有 $\alpha_1 m \le \alpha_1 f(a) \le \alpha_1 M, \alpha_2 m \le \alpha_2 f(b) \le \alpha_2 M$ 成立.

因此 $m = (\alpha_1+\alpha_2)m \le \alpha_1 f(a) + \alpha_2 f(b) \le (\alpha_1+\alpha_2)M = M$.

由介值定理, 至少存在一点 $\xi \in [a,b]$, 使得 $f(\xi) = \alpha_1 f(a) + \alpha_2 f(b)$.



(2) 由最大值最小值定理, 则 $f(x)$ 在闭区间 $[a,b]$ 上有最值, 设最大值为 $M$, 最小值为 $m$.

则此时有 $m \le f(a) \le M, m \le f(b) \le M$ 成立.

由 $k_1, k_2 > 0$ 从而有 $k_1 m \le k_1 f(a) \le k_1 M, k_2 m \le k_2 f(b) \le k_2 M$ 成立.

因此 $(k_1+k_2)m \le k_1 f(a) + k_2 f(b) \le (k_1+k_2)M$.

从而转换可得 $m \le \frac{k_1 f(a) + k_2 f(b)}{k_1+k_2} \le M$.

由介值定理, 至少存在一点 $\eta \in [a,b]$, 使得 $f(\eta) = \frac{k_1 f(a) + k_2 f(b)}{k_1+k_2}$, 即 $k_1 f(a) + k_2 f(b) = f(\eta)(k_1+k_2)$.



---



**63. 设 $f(x)$ 在 $(a,b)$ 内连续, $a < x_1 < x_2 < \dots < x_n < b$, 试证在 $(a,b)$ 内至少存在一点 $\xi$, 使**

$$ f(\xi) = \frac{2}{n(n+1)}[f(x_1) + 2f(x_2) + \dots + nf(x_n)]. $$

**证明:** 由最大值最小值定理, 则 $f(x)$ 在闭区间 $[x_1, x_n]$ 上有最值, 设最大值为 $M$, 最小值为 $m$.

则对 $i=1,2,\dots,n$, 均有 $m \le f(x_i) \le M$ 成立, 因此

$$ \frac{2}{n(n+1)}(m+2m+\dots+nm) \le \frac{2}{n(n+1)}[f(x_1) + 2f(x_2) + \dots + nf(x_n)] \le \frac{2}{n(n+1)}(M+2M+\dots+nM). $$

又

$$ \frac{2}{n(n+1)}(m+2m+\dots+nm) = \frac{2m}{n(n+1)}\frac{n(n+1)}{2} = m, $$

$$ \frac{2}{n(n+1)}(M+2M+\dots+nM) = \frac{2M}{n(n+1)}\frac{n(n+1)}{2} = M. $$

则有 $m \le \frac{2}{n(n+1)}[f(x_1) + \dots + nf(x_n)] \le M$ 成立.

由介值定理, 在 $[x_1, x_n]$ 内至少有一点 $\xi$, 使得 $f(\xi) = \frac{2}{n(n+1)}[f(x_1) + \dots + nf(x_n)]$.

且此时有 $\xi \in [x_1, x_n] \subset (a,b)$, 即 $\xi$ 必在 $(a,b)$ 内.



---

### **导数**



**基本的求导不再强调, 把定义公式往里面套就行**



**11. 设 $\phi(0)=\phi'(0)=0, f(x) = \begin{cases} \phi(x)\sin\frac{1}{x}, & x \neq 0, \\ 0, & x=0, \end{cases}$ 试求 $f'(0)$.**

**解:**

$$ f'(0) = \lim\limits_{x\to 0} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to 0} \frac{\phi(x)\sin\frac{1}{x}-0}{x} = \lim\limits_{x\to 0} \frac{\phi(x)}{x}\sin\frac{1}{x} $$

又因为 $\phi(0)=0$, 且 $\phi'(0) = \lim\limits_{x\to 0} \frac{\phi(x)-\phi(0)}{x-0} = \lim\limits_{x\to 0} \frac{\phi(x)}{x} = 0$,

所以 $\lim\limits_{x\to 0} \frac{\phi(x)}{x}$ 是一个**无穷小**量, 而 $\sin\frac{1}{x}$ 是一个**有界**量.

由夹逼定理则有 $\lim\limits_{x\to 0} \frac{\phi(x)}{x}\sin\frac{1}{x} = 0$. 也即 $f'(0)=0$.



**分段函数的导数, 有可能要用连续性的条件, 常常要分别求出单侧导数**



**5. 设 $f(x) = \begin{cases} x^2, & x \le 1, \\ ax+b, & x>1, \end{cases}$ 试确定 $a,b$, 使 $f$ 在点 $x=1$ 处连续且可导.**


### **抽象函数导数**

**13. 设 $f(x)$ 的定义域为 $(-\infty, +\infty)$, 且对于任意的 $x$ 和 $h$ 均有**
$$ f(x+h) = f(x)f(h), \quad f(0) \neq 0, $$

**(1) 证明 $f(0) = 1$;**

**(2) 若 $f'(0)$ 存在, 证明 $f(x)$ 在任一点 $x$ 均可导, 且 $f'(x) = f(x)f'(0)$.**

**证明:**

(1) 令 $x=h=0$, 则由题意 $f(0+0) = f(0)f(0)$, 即 $f(0)^2 = f(0)$.

又因为 $f(0) \neq 0$, 两边同除以 $f(0)$ 则有 $f(0)=1$ 成立.

(2) 对任意 $x$, 由于 $f'(0)$ 存在, 根据导数定义和 (1) 的结论:

$$ f'(0) = \lim\limits_{\Delta x \to 0} \frac{f(\Delta x) - f(0)}{\Delta x} = \lim\limits_{\Delta x \to 0} \frac{f(\Delta x) - 1}{\Delta x} $$

现在我们来求 $f'(x)$:

$$ \begin{aligned} f'(x) &= \lim\limits_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x} \\ &= \lim\limits_{\Delta x \to 0} \frac{f(x)f(\Delta x) - f(x)}{\Delta x} \\ &= \lim\limits_{\Delta x \to 0} \frac{f(x)(f(\Delta x) - 1)}{\Delta x} \\ &= f(x) \lim\limits_{\Delta x \to 0} \frac{f(\Delta x) - 1}{\Delta x} \\ &= f(x)f'(0) \end{aligned} $$

从而对任意 $x$, $f'(x)$ 存在, 且 $f'(x) = f(x)f'(0)$.

---
**类似题:**

**13. 设函数 $f(x), g(x)$ 定义于 $\mathbb{R}$ 上, 且满足**

**(1) $f(x+y) = f(x)g(y) + f(y)g(x)$;**

**(2) $f(x), g(x)$ 在 $x=0$ 处可导;**

**(3) $f(0)=0, g(0)=1, f'(0)=1, g'(0)=0$.**

**证明: $f(x)$ 在 $\mathbb{R}$ 上可导, 且 $f'(x) = g(x)$.**

**证明思路:**

$$ \begin{aligned} f'(x) &= \lim\limits_{\Delta x \to 0} \frac{f(x + \Delta x) - f(x)}{\Delta x} \\ &= \lim\limits_{\Delta x \to 0} \frac{[f(x)g(\Delta x) + f(\Delta x)g(x)] - f(x)}{\Delta x} \\ &= \lim\limits_{\Delta x \to 0} \frac{f(x)(g(\Delta x) - 1) + f(\Delta x)g(x)}{\Delta x} \\ &= \lim\limits_{\Delta x \to 0} f(x)\frac{g(\Delta x) - 1}{\Delta x} + \lim\limits_{\Delta x \to 0} \frac{f(\Delta x)}{\Delta x}g(x) \\ &= f(x)\frac{g(\Delta x) - g(0)}{\Delta x} + \frac{f(\Delta x) - f(0)}{\Delta x}g(x) \\ &= f(x)g'(0) + f'(0)g(x) \\ &= f(x) \cdot 0 + 1 \cdot g(x) \\ &= g(x) \end{aligned} $$

---

**类似题**

**$f(x)$ 满足 $f(xy) = f(x)f(y)$, 且 $f'(1)$ 存在, 求 $f'(x)$ ($f \neq C, x \neq 0$)**