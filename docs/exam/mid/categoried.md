# 2021-2024期中考试题分类整理

[TOC]

## 数列(函数)极限, 函数极限定义

!!! Tips
    
    抓住定义, 掌握简单的放缩技巧


**24.2. 用数列极限定义证明 $\lim\limits_{n\to\infty} \dfrac{a^n}{n!} = 0$, 其中 $a$ 是常数.**

**解:**

令$k = [|a|]+1>a,n>k$时

$\dfrac{a^n}{n!} = \dfrac{a\cdot a \cdots a}{1\cdot 2 \cdots k}\cdot\dfrac{a\cdots a}{(k+1)\cdots n}$

$=\dfrac{a^k}{k!}\dfrac{a}{k+1}\dfrac{a}{k+2}\cdots\dfrac{a}{n}<\dfrac{a^{k+1}}{k!}\dfrac{1}{n}$

则对于任意 $\varepsilon > 0$, 取 $N = \max\{\left[ \frac{a^{k+1}}{k! \varepsilon} \right] + 1,k\}$.

当 $n > N$ 时,

$$
\left| \frac{a^n}{n!} - 0 \right| < \frac{a^{k+1}}{k!} \frac{1}{n} < \frac{a^{k+1}}{k!} \frac{1}{N} < \varepsilon
$$

从而有 $\lim\limits_{n\to\infty} \dfrac{a^n}{n!} = 0$.

---

**24.12. 写出无穷大量 $\lim\limits_{x\to 0^+} f(x) = +\infty$ 的定义, 并举例说明无界量不一定是无穷大量.**

**解:**

**定义:** 对任意 $M > 0$, $\exists \delta > 0$, 当 $0 < x < \delta$ 时, 有 $|f(x)| > M$, 则称 $\lim\limits_{x\to 0^+} f(x) = +\infty$.

**举例:**

取 $f(x) = \frac{1}{x} \sin \frac{1}{x}$.

则当 $x_n = \frac{1}{2n\pi + \frac{\pi}{2}}$ 时, $f(x_n) = 2n\pi + \frac{\pi}{2}$.

当 $n \to +\infty$ 时, $x_n \to 0$, 有 $f(x_n) \to +\infty$.

为无界量.

但对 $y_n = \frac{1}{2n\pi}$, $f(y_n) = 0$.

当 $n \to +\infty$ 时有 $f(y_n) = 0$.

则不为无穷大量.

即 $\frac{1}{x} \sin \frac{1}{x}$ 在 $x \to 0^+$ 时为无界量但不为无穷大量.

---

**23.1. 叙述函数极限 $\lim\limits_{x \to x_0} f(x) = A \in \mathbb{R}$ 的 “$\varepsilon-\delta$” 定义, 并利用 “$\varepsilon-\delta$” 语言证明: $\lim\limits_{x\to 1} \dfrac{x+2}{2x+1} = 1$.**

**解:**

**定义:** 已知 $f(x)$ 在 $D \subset \mathbb{R}$ 内有定义, 且 $x_0$ 包含于 $D$ 的某去心邻域. 对任意 $\varepsilon > 0$, $\exists \delta > 0$, 对 $x \in \mathring{U}(x_0, \delta) \cap D$ ($\mathring{U}(x_0, \delta)$ 为去心邻域), 均有 $|f(x)-A| < \varepsilon$ 成立, 则 $\lim\limits_{x \to x_0} f(x) = A$.

**证明:**

此时

$$
\left| \frac{x+2}{2x+1} - 1 \right| = \left| \frac{(x+2)-(2x+1)}{2x+1} \right| = \left| \frac{1-x}{2x+1} \right| = \frac{|x-1|}{|2x+1|}
$$

不妨设 $|x-1|<1$ 成立, 则此时有 $0 < x < 2$ 成立.

因此 $|2x+1|>1$, 则 $\frac{1}{|2x+1|} < 1$. 对任意 $\varepsilon > 0$, 取 $\delta = \min(1, \varepsilon)$. 当 $0 < |x-1| < \delta$ 时, 有

$$
\left| \frac{x+2}{2x+1} - 1 \right| = \frac{|x-1|}{|2x+1|} < |x-1| < \delta \le \varepsilon \text{ 成立.}
$$

因此 $\lim\limits_{x\to 1} \dfrac{x+2}{2x+1} = 1$.

---

**22.1. 叙述数列极限 $\lim\limits_{n\to\infty} a_n = A \in \mathbb{R}$ 的 “$\varepsilon-N$” 定义, 并利用 “$\varepsilon-N$” 语言证明: $\lim\limits_{n\to\infty} \dfrac{2n^2-n+1}{n^2+2} = 2$.**

**解:**

**定义:** 若存在 $A \in \mathbb{R}$, 对 $\forall \varepsilon > 0$, $\exists N \in \mathbb{Z}_+$, 当 $n > N$ 时均有 $|a_n - A| < \varepsilon$ 成立, 则称 $\{a_n\}$ 收敛于 A, 记为 $\lim\limits_{n\to\infty} a_n = A$.

**证明:**

由于

$$
\left| \frac{2n^2-n+1}{n^2+2} - 2 \right| = \left| \frac{(2n^2-n+1) - 2(n^2+2)}{n^2+2} \right| = \left| \frac{-n-3}{n^2+2} \right| = \frac{n+3}{n^2+2}
$$

$$
< \frac{n+3n}{n^2} = \frac{4n}{n^2} = \frac{4}{n}
$$

且对 $n \ge 1$, 有 $3 \le 3n$ 成立, 即有

$$
\left| \frac{2n^2-n+1}{n^2+2} - 2 \right| < \frac{n+3n}{n^2+2} < \frac{4n}{n^2} = \frac{4}{n}
$$

对 $\forall \varepsilon > 0$, 取 $N = [\frac{4}{\varepsilon}] + 1$, 则当 $n > N$ 时, 有

$$
\left| \frac{2n^2-n+1}{n^2+2} - 2 \right| < \frac{4}{n} < \frac{4}{N} < \varepsilon \text{ 成立.}
$$

因此有 $\lim\limits_{n\to\infty} \dfrac{2n^2-n+1}{n^2+2} = 2$.

## 求极限

!!! Tips
    包括基本类型的识别和处理技巧, 正确运用等价无穷小, 根式处理手法, 求和类型处理手法


**24.1. 计算极限 $\lim\limits_{x\to 0} \dfrac{e - e^{\cos x} - x^3 \sin\frac{1}{x}}{(\sqrt{1+x^2} - 1) \cos x}$**

**解:**

$$
\lim\limits_{x\to 0} \frac{e - e^{\cos x} - x^3 \sin\frac{1}{x}}{(\sqrt{1+x^2} - 1) \cos x} = \lim\limits_{x\to 0} \frac{e - e^{\cos x} - x^3 \sin\frac{1}{x}}{\frac{1}{2}x^2 \cdot 1}
$$

$$
= \lim\limits_{x\to 0} \frac{e(1-e^{\cos x-1})}{ \frac{1}{2}x^2} - \lim\limits_{x\to 0} \frac{x^3 \sin\frac{1}{x}}{\frac{1}{2}x^2}
$$

$$
= \lim\limits_{x\to 0} \frac{e(-(\cos x-1))}{\frac{1}{2}x^2} - \lim\limits_{x\to 0} 2x \sin\frac{1}{x}
$$

$$
= \lim\limits_{x\to 0} \frac{e(1-\cos x)}{\frac{1}{2}x^2} - 0 = \lim\limits_{x\to 0} \frac{e \cdot \frac{1}{2}x^2}{\frac{1}{2}x^2} = e
$$

---

**24.3. 计算极限 $\lim\limits_{x\to\infty} \left(2e^{\frac{x}{x^2+1}} - 1\right)^x$**

**解:**

$$
\lim\limits_{x\to\infty} \left(2e^{\frac{x}{x^2+1}} - 1\right)^x = \lim\limits_{x\to\infty} e^{x \ln\left(2e^{\frac{x}{x^2+1}} - 1\right)}
$$

$$
= \lim\limits_{x\to\infty} e^{x \ln\left(1 + 2e^{\frac{x}{x^2+1}} - 2\right)} = e^{\lim\limits_{x\to\infty} x \left(2e^{\frac{x}{x^2+1}} - 2\right)}
$$

$$
= e^{\lim\limits_{x\to\infty} 2x \left(e^{\frac{x}{x^2+1}} - 1\right)} = e^{\lim\limits_{x\to\infty} 2x \cdot \frac{x}{x^2+1}} = e^{\lim\limits_{x\to\infty} \frac{2x^2}{x^2+1}} = e^2
$$

---

**24.4. 计算极限 $\lim\limits_{n\to\infty} \left(\frac{1}{n^2+2n+1} + \frac{2}{n^2+2n+2} + \dots + \frac{n}{n^2+2n+n}\right)$**

**解:**

设 $S_n = \frac{1}{n^2+2n+1} + \frac{2}{n^2+2n+2} + \dots + \frac{n}{n^2+2n+n}$.

下界:

$$
S_n > \frac{1}{n^2+2n+n} + \frac{2}{n^2+2n+n} + \dots + \frac{n}{n^2+2n+n} = \frac{1+2+\dots+n}{n^2+3n} = \frac{\frac{n(n+1)}{2}}{n^2+3n} = \frac{n+1}{2(n+3)}
$$

上界:

$$
S_n < \frac{1}{n^2+2n+1} + \frac{2}{n^2+2n+1} + \dots + \frac{n}{n^2+2n+1} < \frac{1+2+\dots+n}{n^2+2n} = \frac{\frac{n(n+1)}{2}}{n(n+2)} = \frac{n+1}{2(n+2)}
$$

又

$$
\lim\limits_{n\to\infty} \frac{n+1}{2(n+3)} = \lim\limits_{n\to\infty} \frac{n+1}{2(n+2)} = \frac{1}{2}
$$

由夹逼准则 (Squeeze Theorem) 可知,

$$
\lim\limits_{n\to\infty} S_n = \frac{1}{2}
$$

---

**23.2. 计算极限 $\lim\limits_{x\to 0} [\sqrt{\cos\ln(1-2x)}]^{\frac{1}{x^2}}$**

**解:**

$$
\lim\limits_{x\to 0} [\cos\ln(1-2x)]^{\frac{1}{2x^2}} = \lim\limits_{x\to 0} e^{\frac{1}{2x^2} \ln[\cos\ln(1-2x)]}
$$

考虑指数部分:

$$
\lim\limits_{x\to 0} \frac{\ln[1+(\cos\ln(1-2x)-1)]}{2x^2} = \lim\limits_{x\to 0} \frac{\cos\ln(1-2x)-1}{2x^2}
$$

$$
= \lim\limits_{x\to 0} \frac{-\frac{1}{2}[\ln(1-2x)]^2}{2x^2} = \lim\limits_{x\to 0} \frac{-\frac{1}{2}(-2x)^2}{2x^2} = \lim\limits_{x\to 0} \frac{-2x^2}{2x^2} = -1
$$

则原极限 $= e^{-1}$.

---

**23.3. 计算极限 $\lim\limits_{x\to 0} \dfrac{\sqrt{1+3x^3}-1+x^4\cos\frac{1}{x}}{\ln(1+2x) \cdot \tan^2 x}$**

**解:**

$$
\lim\limits_{x\to 0} \frac{\sqrt{1+3x^3}-1+x^4\cos\frac{1}{x}}{\ln(1+2x) \cdot \tan^2 x} = \lim\limits_{x\to 0} \frac{\frac{1}{2}(3x^3)+o(x^3)+x^4\cos\frac{1}{x}}{(2x) \cdot x^2}
$$

$$
= \lim\limits_{x\to 0} \frac{\frac{3}{2}x^3}{2x^3} + \lim\limits_{x\to 0} \frac{x^4\cos\frac{1}{x}}{2x^3} = \frac{3}{4} + \lim\limits_{x\to 0} \frac{1}{2}x\cos\frac{1}{x} = \frac{3}{4} + 0 = \frac{3}{4}
$$

---

**23.4. 当 $x\to 1$ 时, $1-\dfrac{m}{1+x+x^2+\dots+x^{m-1}}$ 是 $(x-1)$ 的等价无穷小量 ($m \in \mathbb{N}$), 求常数 m 的值**

**解：**

根据等价无穷小量的定义，有：

$$ \lim_{x\to 1} \frac{1-\frac{m}{1+x+x^2+\dots+x^{m-1}}}{x-1} = 1 $$

对极限表达式的左边进行化简：

$$ \begin{aligned} \text{左边} &= \lim_{x\to 1} \frac{\frac{(1+x+x^2+\dots+x^{m-1})-m}{1+x+x^2+\dots+x^{m-1}}}{x-1} \\ &= \lim_{x\to 1} \frac{1+x+x^2+\dots+x^{m-1}-m}{(x-1)(1+x+x^2+\dots+x^{m-1})} \\ &= \lim_{x\to 1} \frac{(x-1)+(x^2-1)+\dots+(x^{m-1}-1)}{(x-1)(1+x+x^2+\dots+x^{m-1})} \\ &= \lim_{x\to 1} \frac{(x-1)[1+(x+1)+(x^2+x+1)+\dots+(x^{m-2}+\dots+1)]}{(x-1)(1+x+x^2+\dots+x^{m-1})} \\ &= \lim_{x\to 1} \frac{1+(x+1)+(x^2+x+1)+\dots+(x^{m-2}+\dots+1)}{1+x+x^2+\dots+x^{m-1}} \\ &= \frac{1+2+3+\dots+(m-1)}{1+1+1+\dots+1} \\ &= \frac{\frac{(m-1)m}{2}}{m} \\ &= \frac{m-1}{2} \end{aligned} $$

因为该极限值为 1，所以：

$$ \frac{m-1}{2} = 1 $$

解得：$m = 3$

---

**23.5. 计算极限 $\lim\limits_{n\to\infty} \left(\frac{1}{n^2+1+\sin 1} + \frac{2}{n^2+1+\sin 2} + \dots + \frac{n}{n^2+1+\sin n}\right)$**

**解:**

对任意正整数 $i, 1 \le i \le n$, 有 $n^2 \le n^2+1+\sin i \le n^2+2$ 成立.因此

$$
\frac{1}{n^2+2} \le \frac{1}{n^2+1+\sin i} \le \frac{1}{n^2}
$$

设 $S_n = \sum_{i=1}^n \frac{i}{n^2+1+\sin i}$

下界:

$$
S_n = \sum_{i=1}^n \frac{i}{n^2+1+\sin i} \ge \sum_{i=1}^n \frac{i}{n^2+2} = \frac{1}{n^2+2} \sum_{i=1}^n i = \frac{n(n+1)}{2(n^2+2)}
$$

上界:

$$
S_n = \sum_{i=1}^n \frac{i}{n^2+1+\sin i} \le \sum_{i=1}^n \frac{i}{n^2} = \frac{1}{n^2} \sum_{i=1}^n i = \frac{n(n+1)}{2n^2} = \frac{n+1}{2n}
$$

又 $\lim\limits_{n\to\infty} \frac{n(n+1)}{2(n^2+2)} = \frac{1}{2}$, $\lim\limits_{n\to\infty} \frac{n+1}{2n} = \frac{1}{2}$.

利用夹逼准则,

$$
\lim\limits_{n\to\infty} S_n = \frac{1}{2}
$$

---

**22.2. 计算极限 $\lim\limits_{x\to 0} (e^{2x} - \arctan x)^{\csc x}$**

**解:**

原式 $= \lim\limits_{x\to 0} e^{\csc x \ln(e^{2x} - \arctan x)} = e^{\lim\limits_{x\to 0} \frac{\ln(e^{2x} - \arctan x)}{\sin x}}$

考虑指数部分:

$$
\lim\limits_{x\to 0} \frac{\ln(1+e^{2x} - 1 - \arctan x)}{\sin x} = \lim\limits_{x\to 0} \frac{e^{2x} - 1 - \arctan x}{x}
$$

($e^{2x}-1-\arctan x \to 0, \arctan x \to 0$)

$$
= \lim\limits_{x\to 0} \frac{e^{2x}-1}{x} - \lim\limits_{x\to 0} \frac{\arctan x}{x} = 2 - 1 = 1
$$

从而原极限 $= e^1 = e$.

---

**22.3. 计算极限 $\lim\limits_{x\to \frac{2\pi}{3}} \frac{1+2\cos x}{3x-2\pi}$**

**解:**

令 $t = x - \frac{2\pi}{3}$, 则 $x = t + \frac{2\pi}{3}$. 当 $x \to \frac{2\pi}{3}$ 时, $t \to 0$.

$$
\lim\limits_{t\to 0} \frac{1+2\cos(t+\frac{2\pi}{3})}{3t} = \lim\limits_{t\to 0} \frac{1+2(\cos t \cos\frac{2\pi}{3} - \sin t \sin\frac{2\pi}{3})}{3t}
$$

$$
= \lim\limits_{t\to 0} \frac{1+2(-\frac{1}{2}\cos t - \frac{\sqrt{3}}{2}\sin t)}{3t} = \lim\limits_{t\to 0} \frac{1-\cos t - \sqrt{3}\sin t}{3t}
$$

$$
= \lim\limits_{t\to 0} \frac{1-\cos t}{3t} - \lim\limits_{t\to 0} \frac{\sqrt{3}\sin t}{3t} = \lim\limits_{t\to 0} \frac{\frac{1}{2}t^2}{3t} - \frac{\sqrt{3}}{3} = 0 - \frac{\sqrt{3}}{3} = -\frac{\sqrt{3}}{3}
$$

---

**22.4. 计算极限 $\lim\limits_{x\to -\infty} x(\sqrt{x^2+6x-1}+x+3)$**

**解:**

$$
\lim\limits_{x\to -\infty} \frac{x(\sqrt{x^2+6x-1}+(x+3))(\sqrt{x^2+6x-1}-(x+3))}{\sqrt{x^2+6x-1}-(x+3)}
$$

$$
= \lim\limits_{x\to -\infty} \frac{x((x^2+6x-1)-(x^2+6x+9))}{\sqrt{x^2+6x-1}-x-3} = \lim\limits_{x\to -\infty} \frac{-10x}{-x\sqrt{1+\frac{6}{x}-\frac{1}{x^2}}-x-3}
$$

(注意 $x<0$, $\sqrt{x^2}=-x$)

$$
= \lim\limits_{x\to -\infty} \frac{-10}{-\sqrt{1+\frac{6}{x}-\frac{1}{x^2}}-1-\frac{3}{x}} = \frac{-10}{-\sqrt{1}-1-0} = \frac{-10}{-2} = 5
$$

---

**22.5. 计算极限 $\lim\limits_{n\to\infty} \left(\frac{1^2}{\sqrt{n^6+1+1}} + \frac{2^2}{\sqrt{n^6+2+\frac{1}{2}}} + \dots + \frac{n^2}{\sqrt{n^6+n+\frac{1}{n}}}\right)$**

**解:**

由于 $S_n = \sum_{k=1}^n \frac{k^2}{\sqrt{n^6+k+\frac{1}{k}}}$

上界:

$$
S_n < \sum_{k=1}^n \frac{k^2}{\sqrt{n^6}} = \frac{1}{n^3} \sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}{6n^3}
$$

下界:

$$
S_n > \sum_{k=1}^n \frac{k^2}{\sqrt{n^6+n+1}} = \frac{1}{\sqrt{n^6+n+1}} \sum_{k=1}^n k^2 = \frac{n(n+1)(2n+1)}{6\sqrt{n^6+n+1}}
$$

又因为

$$
\lim\limits_{n\to\infty} \frac{n(n+1)(2n+1)}{6n^3} = \frac{2}{6} = \frac{1}{3}
$$

$$
\lim\limits_{n\to\infty} \frac{n(n+1)(2n+1)}{6\sqrt{n^6+n+1}} = \lim\limits_{n\to\infty} \frac{2n^3}{6n^3} = \frac{1}{3}
$$

从而由夹逼定理, 原极限 $= \frac{1}{3}$.

---

**21.1. 求极限 $\lim\limits_{x\to 0} \dfrac{x \arcsin x \arctan x}{(\sqrt{\cos x}-1)\ln(1+x)}$**

**解:**

$$
\lim\limits_{x\to 0} \frac{x \cdot x \cdot x}{(\cos x-1)\ln(1+x)} \cdot (\sqrt{\cos x}+1) = \lim\limits_{x\to 0} \frac{x^3}{(-\frac{1}{2}x^2) \cdot x} \cdot 2 = -4
$$

---

**21.2. 已知 $\lim\limits_{x\to\infty} (\sqrt{x^2-x+1}-ax-b)=0$, 求常数 a, b.**

由题可知

$$ b = \lim_{x\to -\infty} (\sqrt{x^2-x+1} - ax) $$

令 $t = \dfrac{1}{x}$，则当 $x \to -\infty$ 时, $t \to 0^-$

$$ \begin{aligned} b &= \lim_{t\to 0^-} (\sqrt{\frac{1}{t^2}-\frac{1}{t}+1} - \frac{a}{t}) \\ &= \lim_{t\to 0^-} (\frac{\sqrt{1-t+t^2}}{\sqrt{t^2}} - \frac{a}{t}) \\ &= \lim_{t\to 0^-} (\frac{\sqrt{1-t+t^2}}{-t} - \frac{a}{t}) \\ &= \lim_{t\to 0^-} \frac{-\sqrt{1-t+t^2}-a}{t} \end{aligned} $$

因为极限存在，所以分母趋于 0 时，分子也必须趋于 0。


则应有 $\lim_{t\to 0^-} (-\sqrt{1-t+t^2}-a) = 0$ 成立。

$$ a = \lim_{t\to 0^-} (-\sqrt{1-t+t^2}) = -1 $$

从而，

$$ \begin{aligned} b &= \lim_{t\to 0^-} \frac{1-\sqrt{1-t+t^2}}{t} \\ &= \lim_{t\to 0^-} \frac{(1-\sqrt{1-t+t^2})(1+\sqrt{1-t+t^2})}{t(1+\sqrt{1-t+t^2})} \\ &= \lim_{t\to 0^-} \frac{1-(1-t+t^2)}{t(1+\sqrt{1-t+t^2})} \\ &= \lim_{t\to 0^-} \frac{t-t^2}{t(1+\sqrt{1-t+t^2})} \\ &= \lim_{t\to 0^-} \frac{1-t}{1+\sqrt{1-t+t^2}} \\ &= \frac{1-0}{1+\sqrt{1}} = \frac{1}{2} \end{aligned} $$

综上， $a = -1$, $b = \dfrac{1}{2}$.

---

**22.3. 设 a, b, c 为正数, 求下列极限 $\lim\limits_{x\to 0} \left(\dfrac{a^{x+1}+b^{x+1}+c^{x+1}}{a+b+c}\right)^{\frac{1}{x}}$**

**解:**

原式 $= \lim\limits_{x\to 0} e^{\frac{1}{x} \ln\left(\frac{a^{x+1}+b^{x+1}+c^{x+1}}{a+b+c}\right)}$

考虑指数部分:

$$
\lim\limits_{x\to 0} \frac{1}{x} \ln\left(1 + \frac{a \cdot a^x + b \cdot b^x + c \cdot c^x - (a+b+c)}{a+b+c}\right)
$$

$$
= \lim\limits_{x\to 0} \frac{1}{x} \frac{a(a^x-1)+b(b^x-1)+c(c^x-1)}{a+b+c}
$$

$$
= \frac{1}{a+b+c} \lim\limits_{x\to 0} \left(a\frac{a^x-1}{x} + b\frac{b^x-1}{x} + c\frac{c^x-1}{x}\right)
$$

$$
= \frac{a\ln a + b\ln b + c\ln c}{a+b+c} = \frac{\ln(a^a b^b c^c)}{a+b+c}
$$

原极限 $= e^{\frac{\ln(a^a b^b c^c)}{a+b+c}} = (a^a b^b c^c)^{\frac{1}{a+b+c}}$.

---

**22.4. 求极限 $\lim\limits_{x\to +\infty} \sqrt[3]{x^3+x^2+1} - \sqrt{x^2+x+1}$**

$$ \begin{aligned} &= (t=\frac{1}{x}) \lim_{t\to 0^+} (\sqrt[3]{\frac{1}{t^3}+\frac{1}{t^2}+1} - \sqrt{\frac{1}{t^2}+\frac{1}{t}+1}) \\ &= \lim_{t\to 0^+} (\frac{\sqrt[3]{1+t+t^3}}{t} - \frac{\sqrt{1+t+t^2}}{t}) \\ &= \lim_{t\to 0^+} \frac{\sqrt[3]{1+t+t^3}-1}{t} + \lim_{t\to 0^+} \frac{1-\sqrt{1+t+t^2}}{t} \\ &= \lim_{t\to 0^+} \frac{1+t+t^3-1}{t((\sqrt[3]{1+t+t^3})^2 + \sqrt[3]{1+t+t^3} + 1)} + \lim_{t\to 0^+} \frac{1-(1+t+t^2)}{t(1+\sqrt{1+t+t^2})} \\ &= \lim_{t\to 0^+} \frac{t+t^3}{3t} + \lim_{t\to 0^+} \frac{-t-t^2}{2t} \\ &= \frac{1}{3} - \frac{1}{2} = -\frac{1}{6} \end{aligned} $$

---


**22.11. 求极限 $\lim\limits_{x\to 0} \left(\dfrac{2+e^{\frac{1}{x}}}{\cos x+e^{\frac{1}{x}}} + \dfrac{\sin x}{|x|}\right)$**

有绝对值, 为了去绝对值分两侧考虑

$$ \begin{aligned} & \lim_{x\to 0^+} \frac{2+e^{\frac{1}{x}}}{\cos x+e^{\frac{2}{x}}} + \frac{\sin x}{x} \quad (\text{此时} \lim_{x\to 0^+} e^{\frac{1}{x}} = +\infty) \\ &= \lim_{x\to 0^+} \frac{2e^{-\frac{2}{x}}+e^{-\frac{1}{x}}}{(\cos x)e^{-\frac{2}{x}}+1} + 1 \\ &= \frac{0+0}{1 \cdot 0+1} + 1 = 1 \end{aligned} $$

而

$$ \begin{aligned} & \lim_{x\to 0^-} \frac{2+e^{\frac{1}{x}}}{\cos x+e^{\frac{2}{x}}} - \frac{\sin x}{x} \quad (\lim_{x\to 0^-} e^{\frac{1}{x}} = 0) \\ &= \lim_{x\to 0^-} \frac{2+0}{1+0} - \lim_{x\to 0^-} \frac{\sin x}{x} \\ &= 2 - 1 = 1 \end{aligned} $$

则$\lim\limits_{x\to 0}\left(\dfrac{2+e^{\frac{1}{x}}}{\cos x+e^{\frac{2}{x}}} + \dfrac{\sin x}{|x|}\right) = 1$

## 函数连续性和间断点

!!! Tips
    关注函数分子本身的间断点, 让分母为 0 的点

---

**24.5. 指出函数 $f(x) = \begin{cases} e^{\frac{1}{x-1}}, & x > 0, \\ \ln(1+x), & -1 < x \le 0 \end{cases}$ 的间断点, 并判断其类型.**

**解:** 可能的间断点为 $0$ 和 $1$.

**在 x=0 处:**

$f(0) = \ln(1+0) = 0$.

$\lim\limits_{x\to 0^-} f(x) = \lim\limits_{x\to 0^-} \ln(1+x) = 0$.

$\lim\limits_{x\to 0^+} f(x) = \lim\limits_{x\to 0^+} e^{\frac{1}{x-1}} = e^{-1} = \frac{1}{e}$.

因为 $\lim\limits_{x\to 0^-} f(x) \neq \lim\limits_{x\to 0^+} f(x)$, 则 $x=0$ 是 $f(x)$ 的跳跃间断点 (第一类).

**在 x=1 处:**

$f(x)$ 在 $x=1$ 无定义.

$\lim\limits_{x\to 1^-} f(x) = \lim\limits_{x\to 1^-} e^{\frac{1}{x-1}} = 0$.

$\lim\limits_{x\to 1^+} f(x) = \lim\limits_{x\to 1^+} e^{\frac{1}{x-1}} = +\infty$.

因为右极限为无穷大, 则 $x=1$ 是 $f(x)$ 的第二类间断点 (无穷间断点).

> 间断点考虑的是函数在去心邻域有定义，而在$x = -1$ 处,左侧函数没定义, 所以不考虑-1是否为间断点.

---

**22.12. 已知 $f(x) = \dfrac{1}{e^{\frac{\sin \pi x}{x-1}} - 1} \quad (-1 < x < 2)$, 试判断 $f(x)$ 的间断点并据理说明间断点的类型。**

考虑所有无定义点, 即分母为0处, 有

$$ \begin{cases} x-1=0 \\ e^{\frac{\sin \pi x}{x-1}}-1=0 \text{ 且 } x-1 \ne 0 \end{cases} $$

对 $e^{\frac{\sin \pi x}{x-1}}-1=0$, 有 $\frac{\sin \pi x}{x-1}=0$, 对 $-1 < x < 2$ 解得 $x=0$。

考虑 $x=0$ 时, 则 $x \to 0$ 有 $e^{\frac{\sin \pi x}{x-1}} - 1 \to 0$, 从而 $f(x) \to \infty$。

则 $x=0$ 为第二类间断点。

再考虑 $x=1$ 时, 由于
$$ \begin{aligned} \lim_{x\to 1} \frac{\sin \pi x}{x-1} &\xrightarrow{t=x-1} \lim_{t\to 0} \frac{\sin[\pi(t+1)]}{t} \\ &= \lim_{t\to 0} \frac{-\sin \pi t}{t} = -\pi \end{aligned} $$
则
$$ \lim_{x\to 1} f(x) = \lim_{x\to 1} \frac{1}{e^{\frac{\sin \pi x}{x-1}}-1} = \frac{1}{e^{-\pi}-1} $$
则 $x=1$ 为可去间断点。

综上, $f(x)$ 有可去间断点 $x=1$, 第二类间断点 $x=0$。


---

**21.9. 设函数 $f(x) = e^{\frac{x}{x-1}} - 1$，求函数 $\frac{1}{f(x)}$ 的间断点，并判断它们的类型。**

考虑间断点即考虑 $\frac{1}{f(x)}$ 没有定义的点。

① 当 $f(x)$ 无定义时，$x-1=0$, $x=1$。
   
而对 $x \to 1^+$, 有 $\frac{x}{x-1} \to +\infty$, $f(x) \to +\infty$
    
则 $\lim\limits_{x\to 1^+} \frac{1}{f(x)} = 0$
    
$x \to 1^-$ 时, $\frac{x}{x-1} \to -\infty$, $f(x) \to -1$
    
则 $\lim\limits_{x\to 1^-} \frac{1}{f(x)} = -1$
    
$0 \ne -1$, 则 $x=1$ 为跳跃间断点；
    
② 当 $f(x)=0$ 时，同样 $\frac{1}{f(x)}$ 无定义
    
此时 $e^{\frac{x}{x-1}}-1=0$ 解得 $x=0$。
    
而 $x \to 0$ 时, $f(x) \to 0$,
    
$\lim\limits_{x\to 0} \frac{1}{f(x)}$ 不存在, 则 $x=0$ 为第二类间断点。
    
综上, $\frac{1}{f(x)}$ 的间断点为 $x=0$ (第二类间断点) 和 $x=1$ (跳跃间断点)。


## 利用导数的定义计算 分段函数可导性讨论


---

**24.10. 试确定常数 a,b 的值, 使函数 $f(x) = \begin{cases} 1 + \ln(1-2x), & x \le 0, \\ a+be^x, & x > 0 \end{cases}$ 在 $x=0$ 处可导, 并求此时导函数 $f'(x)$(吉米多维奇高数174)**

要使 $f(x)$ 在 $x=0$ 处可导,必有 $f(x)$ 在 $x=0$ 处连续,即 $\lim\limits_{x \to 0^+} f(x) = \lim\limits_{x \to 0^-} f(x) = f(0) = 1$，得 $a+b=1$

$f'_{-}(0) = \lim\limits_{x \to 0^-} \dfrac{f(x)-f(0)}{x} = \lim\limits_{x \to 0^-} \dfrac{1+\ln(1-2x)-1}{x} = -2$

$f'_{+}(0) = \lim\limits_{x \to 0^+} \dfrac{f(x)-f(0)}{x} = \lim\limits_{x \to 0^+} \dfrac{a+be^x-(a+b)}{x} = \lim\limits_{x \to 0^+} \dfrac{b(e^x-1)}{x} = b$

所以 $b=-2$, 于是 $a=3$, 且有 $f'(0)=-2$

$f'(x) = \begin{cases} -\dfrac{2}{1-2x}, & x \le 0, \\ -2e^x, & x>0. \end{cases}$

---

**24.11. 设函数 $f(x) = x^2 D(x)$, 其中 $D(x) = \begin{cases} 1, & x \text{是有理数} \\ 0, & x \text{是无理数} \end{cases}$, 试讨论函数 $f(x), x \in (-\infty, +\infty)$ 的连续性和可导性; 若可导, 求其导数.**

**解:**

先考虑连续性

当$x\to0$时，$D(x)$有界而$x^2$为无穷小

所以$\lim\limits_{x\to0} f(x) = \lim\limits_{x\to0} x^2 \cdot D(x) = 0$.**且 $f(0)=0$, 从而 $f(x)$ 在 $x=0$ 处连续.**

在 $x=x_0$ 处, $x_0 \neq 0$ 时,

$x$ 为有理数时, $\lim\limits_{x\to x_0} f(x) = \lim\limits_{x\to x_0} x^2 \cdot 1 = x_0^2$.

$x$ 为无理数时, $\lim\limits_{x\to x_0} f(x) = \lim\limits_{x\to x_0} x^2 \cdot 0 = 0$.

**二者不相等, 故 $f(x)$ 在 $x=x_0, x_0 \neq 0$ 处不连续.**

因此考虑 $f(x)$ 在 $x=0$ 处是否可导.

$f'(0) = \lim\limits_{x\to0} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to0} \frac{x^2 \cdot D(x) - 0}{x-0} = \lim\limits_{x\to0} x \cdot D(x) = 0$.

**综上, $f(x)$ 在 $x=0$ 处连续且可导, $f'(0)=0$.**

**在 $x \in (-\infty,0) \cup (0, +\infty)$ 上 $f(x)$ 不连续, 也不可导.**


---

**23.9. 设 $f(x) = \begin{cases} x^2 \sin\dfrac{1}{x} + e^{2x}, & (x < 0) \\ ax + b, & (x \ge 0) \end{cases}$**

(1) 求常数 a,b 的值使 $f(x)$ 在 $x=0$ 处可导; 

(2) 计算 $f'(x)$ ($x \in \mathbb{R}$). 

(3) 试问 $f''(0)$ 是否存在? 为什么?


**解:**

**1)** $f(x)$ 在 $x=0$ 处可导则首先要在 $x=0$ 处连续.

$$
\lim\limits_{x\to 0^-} f(x) = \lim\limits_{x\to 0^-} (x^2 \sin\frac{1}{x} + e^{2x}) = 0 + e^0 = 1
$$

且 $f(0)=b$. 由连续知 $\lim\limits_{x\to 0^-} f(x) = f(0)$, 从而 $b=1$.

又因为

$$
f'_-(0) = \lim\limits_{x\to 0^-} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to 0^-} \frac{x^2 \sin\frac{1}{x} + e^{2x} - 1}{x} = \lim\limits_{x\to 0^-} x\sin\frac{1}{x} + \lim\limits_{x\to 0^-} \frac{e^{2x}-1}{x} = 0+2 = 2
$$

$$
f'_+(0) = \lim\limits_{x\to 0^+} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to 0^+} \frac{ax+b-1}{x} = \lim\limits_{x\to 0^+} \frac{ax}{x} = a
$$

利用可导则 $f'_-(0) = f'_+(0)$, 则 $a=2$. 综上, $a=2, b=1$.

**2)**

$x<0$ 时, $f'(x) = 2x\sin\frac{1}{x} + x^2 \cdot \cos\frac{1}{x} \cdot (-\frac{1}{x^2}) + 2e^{2x} = 2x\sin\frac{1}{x} - \cos\frac{1}{x} + 2e^{2x}$.

$x>0$ 时, $f'(x) = a = 2$.

$x=0$ 时由(1), $f'(0) = 2$.

综上, $f'(x) = \begin{cases} 2x\sin\frac{1}{x} - \cos\frac{1}{x} + 2e^{2x}, & x < 0 \\ 2, & x \ge 0 \end{cases}$

**3)**

由题, $\lim\limits_{x\to 0^-} 2x\sin\frac{1}{x} = 0$, $\lim\limits_{x\to 0^-} 2e^{2x} = 2$, 而 $\lim\limits_{x\to 0^-} \cos\frac{1}{x}$ 不存在.

则 $\lim\limits_{x\to 0^-} f'(x)$ 不存在.

因此 $f'(x)$ 在 $x=0$ 处不连续, 从而 $f'(x)$ 在 $x=0$ 处不可导, 即 $f''(0)$ 不存在.

---

**22.6. 已知 $f(x) = \lim\limits_{n\to\infty} \frac{2xe^{n(x-1)} + ax^2 + b}{e^{n(x-1)}+1}$ 在 $\mathbb{R}$ 上可导, 求常数 a, b 的值.**

由于 $x>1$ 时, $n(x-1) \to +\infty$, 有 $e^{n(x-1)} \to +\infty$.
此时

$$
f(x) = \lim\limits_{n\to\infty} \frac{2x e^{n(x-1)} + ax^2+b}{e^{n(x-1)}+1} = \lim\limits_{n\to\infty} \frac{2x + (ax^2+b)/e^{n(x-1)}}{1+1/e^{n(x-1)}} = 2x
$$

$x<1$ 时, $n(x-1) \to -\infty$, 有 $e^{n(x-1)} \to 0$.

此时

$$
f(x) = \lim\limits_{n\to\infty} \frac{2x e^{n(x-1)} + ax^2+b}{e^{n(x-1)}+1} = ax^2+b
$$

而

$$
f(1) = \lim\limits_{n\to\infty} \frac{2e^0+a+b}{e^0+1} = \frac{2+a+b}{2}
$$

则有

$$
f(x) = \begin{cases} 2x, & x>1 \\ \frac{a+b+2}{2}, & x=1 \\ ax^2+b, & x<1 \end{cases}
$$

又 $f(x)$ 在 $x=1$ 处可导, 则 $f(x)$ 在 $x=1$ 处连续.

此时有 $\lim\limits_{x\to 1^-} f(x) = \lim\limits_{x\to 1^+} f(x) = f(1)$.

$\lim\limits_{x\to 1^-} (ax^2+b) = a+b$, $\lim\limits_{x\to 1^+} 2x=2$.

则有 $\frac{a+b+2}{2} = a+b = 2$.

又由可导则应有 $f'_-(1) = f'_+(1)$.

$$
f'_-(1) = \lim\limits_{x\to 1^-} \frac{f(x)-f(1)}{x-1} = \lim\limits_{x\to 1^-} \frac{ax^2+b-2}{x-1} = \lim\limits_{x\to 1^-} \frac{a(x^2-1)+(a+b-2)}{x-1} = \lim\limits_{x\to 1^-} a(x+1) = 2a
$$

$$
f'_+(1) = \lim\limits_{x\to 1^+} \frac{f(x)-f(1)}{x-1} = \lim\limits_{x\to 1^+} \frac{2x-2}{x-1} = 2
$$

从而有 $2a=2$, 即 $a=1$. 因此 $b=2-a=1$.

---

**21.5. 定义函数 $f(x)$ 在 $x=0$ 处的值, 使其在 $x=0$ 处连续, 并讨论在 $x=0$ 处是否可导, 其中 $f(x)=(1+\sin^2\frac{1}{x})^x$.**


**解:**

对 $\lim\limits_{x\to 0} f(x) = \lim\limits_{x\to 0} (1+\sin^2\frac{1}{x})^x = \lim\limits_{x\to 0} e^{x \ln(1+\sin^2\frac{1}{x})}$.

由于 $\sin^2\frac{1}{x} \in[0,1]$, 则 $\ln(1+\sin^2\frac{1}{x}) \in [0, \ln 2]$.

从而 $0 \le x \ln(1+\sin^2\frac{1}{x}) \le x\ln 2$ (for $x>0$).

又 $\lim\limits_{x\to 0} x\ln 2 = 0$. 由夹逼准则, $\lim\limits_{x\to 0} x\ln(1+\sin^2\frac{1}{x})=0$.

从而 $\lim\limits_{x\to 0} f(x) = e^0 = 1$.

因此定义 $f(0)=1$, 则 $f(x)$ 在 $x=0$ 处连续.

再讨论可导性, 考虑 $\lim\limits_{x\to 0} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to 0} \frac{(1+\sin^2\frac{1}{x})^x - 1}{x}$.

$$
= \lim\limits_{x\to 0} \frac{e^{x \ln(1+\sin^2\frac{1}{x})} - 1}{x} = \lim\limits_{x\to 0} \frac{x \ln(1+\sin^2\frac{1}{x})}{x}
$$

(分子部分 $\to 0$, 利用 $e^u-1 \sim u$)

$$
= \lim\limits_{x\to 0} \ln(1+\sin^2\frac{1}{x})
$$

对 $n \to \infty$, 当 $x_n = \frac{1}{n\pi}$ 时, $\sin^2\frac{1}{x_n}=0$, $\ln(1+\sin^2\frac{1}{x_n})=\ln 1 = 0$.

当 $x_n = \frac{1}{(n+\frac{1}{2})\pi}$ 时, $\sin^2\frac{1}{x_n}=1$, $\ln(1+\sin^2\frac{1}{x_n})=\ln 2$.

根据**归结原理的逆否命题**知道，$\lim\limits_{x\to 0} \ln(1+\sin^2\frac{1}{x})$ 不存在.

则 $f(x)$ 在 $x=0$ 处不可导.



## 计算题: 直接求导, 隐函数求导, 参数方程求导, 极坐标求导 | 求微分

!!! Tips
    每年必考, 计算量可能有点大

---

**24.6. 设函数 $y = x^2 e^{\sin^2\frac{1}{x}}$, 求 $\dfrac{\mathrm{d}y}{\mathrm{d}x}$.**

**解:**

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = 2x e^{\sin^2\frac{1}{x}} + x^2 e^{\sin^2\frac{1}{x}} \cdot \left(2\sin\frac{1}{x}\cos\frac{1}{x}\right) \cdot \left(-\frac{1}{x^2}\right)
$$

$$
= e^{\sin^2\frac{1}{x}} (2x - \sin\frac{2}{x})
$$

---

**24.7. 设函数 $y=y(x)$ 由方程 $\ln(x^2+y) = x^3y+\sin x$ 确定, 求 $\mathrm{d}y\big|_{x=0}$.**

**解:**

代入 $x=0$, 则 $\ln y = 0+0=0$, 所以 $y=1$.

对方程两边同时对 x 求导有

$$
\frac{1}{x^2+y}(2x+y') = 3x^2y+x^3y'+\cos x
$$

代入 $x=0, y=1$, 则 $\frac{1}{0+1}(0+y') = 0+0+\cos 0 = 1$.

$y'|_{x=0} = 1$, 则 $\mathrm{d}y|_{x=0} = 1 \cdot \mathrm{d}x = \mathrm{d}x$.

---

**24.8. 求极坐标系下曲线 $r = e^\theta$ 在点 $(r, \theta) = (e^{\pi/2}, \pi/2)$ 处在直角坐标系下的切线方程.**

**解:**

由题 $\begin{cases} x = r\cos\theta = e^\theta \cos\theta \\ y = r\sin\theta = e^\theta \sin\theta \end{cases}$

则

$$
\frac{\mathrm{d}x}{\mathrm{d}\theta} = e^\theta \cos\theta + e^\theta(-\sin\theta) = e^\theta(\cos\theta-\sin\theta)
$$

$$
\frac{\mathrm{d}y}{\mathrm{d}\theta} = e^\theta \sin\theta + e^\theta \cos\theta = e^\theta(\sin\theta+\cos\theta)
$$

所以

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y/\mathrm{d}\theta}{\mathrm{d}x/\mathrm{d}\theta} = \frac{e^\theta(\sin\theta+\cos\theta)}{e^\theta(\cos\theta-\sin\theta)} = \frac{\sin\theta+\cos\theta}{\cos\theta-\sin\theta}
$$

在 $\theta = \pi/2$ 处切线斜率 $k = \frac{\mathrm{d}y}{\mathrm{d}x}|_{\theta=\pi/2} = \frac{1+0}{0-1} = -1$.

又 $\theta=\pi/2$ 时 $x=0, y=e^{\pi/2}$, 即切点直角坐标 $(0, e^{\pi/2})$.

所以切线方程为 $y - e^{\pi/2} = -1(x-0)$, 即 $y = -x+e^{\pi/2}$.


---

**23.6. 设函数 $y=y(x)$ 是由方程 $x^2+y=\tan(x-y)$ 所确定, 且 $y(0)=0$. 求 $y'(0)$ 和 $y''(0)$.**

**解:**
对 $x^2+y=\tan(x-y)$, 方程两边同时对 $x$ 求导有

$$
2x+y' = \sec^2(x-y) \cdot (1-y') \quad \cdots ①
$$

代入 $x=y=0$, 有 $0+y' = \sec^2(0) (1-y')$, 有 $y'=1-y'$, $2y'=1$, $y'=\frac{1}{2}$. 即 $y'(0)=\frac{1}{2}$.

对 ① 式两边再对 $x$ 求导有

$$
2+y'' = 2\sec(x-y) \cdot (\sec(x-y)\tan(x-y)) \cdot (1-y')^2 + \sec^2(x-y) \cdot (-y'')
$$

代入 $x=y=0, y'=\frac{1}{2}$, 有

$$
2+y'' = 2\sec^2(0)\tan(0)(1-\frac{1}{2})^2 + \sec^2(0)(-y'') = 0 - y''
$$

$2+y'' = -y'' \implies 2y''=-2 \implies y''=-1$. 即 $y''(0)=-1$.

---

23.7. 已知 $y = x \ln (x + \sqrt{x^2+1}) - \sqrt{x^2+1}$，求 $\dfrac{\mathrm{d}y}{\mathrm{d}x}, \dfrac{\mathrm{d}^2y}{\mathrm{d}x^2}$.

$$ \begin{aligned} \frac{\mathrm{d}y}{\mathrm{d}x} &= \ln(x+\sqrt{x^2+1}) + x \cdot \frac{1+\frac{2x}{2\sqrt{x^2+1}}}{x+\sqrt{x^2+1}} - \frac{2x}{2\sqrt{x^2+1}} \\ &= \ln(x+\sqrt{x^2+1}) + x \cdot \frac{\frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}}}{(x+\sqrt{x^2+1})} - \frac{x}{\sqrt{x^2+1}} \\ &= \ln(x+\sqrt{x^2+1}) + \frac{x}{\sqrt{x^2+1}} - \frac{x}{\sqrt{x^2+1}} = \ln(x+\sqrt{x^2+1}) \end{aligned} $$

$$ \frac{\mathrm{d}^2y}{\mathrm{d}x^2} = \frac{1}{x+\sqrt{x^2+1}} \cdot (1+\frac{2x}{2\sqrt{x^2+1}}) = \frac{1}{x+\sqrt{x^2+1}} \cdot \frac{\sqrt{x^2+1}+x}{\sqrt{x^2+1}} = \frac{1}{\sqrt{x^2+1}} $$


---

23.8. 设 $y = \arctan \dfrac{x+1}{x-1} + \ln \sqrt{1+x^2}$，求 $\mathrm{d}y$ 与 $\mathrm{d}y\big|_{x=3}$.

$$ \begin{aligned} y' = \frac{\mathrm{d}y}{\mathrm{d}x} &= \frac{1}{1+(\frac{x+1}{x-1})^2} \cdot \frac{(x-1)\cdot 1 - (x+1)\cdot 1}{(x-1)^2} + \frac{1}{\sqrt{1+x^2}} \cdot \frac{2x}{2\sqrt{1+x^2}} \\ &= \frac{-2}{(x-1)^2+(x+1)^2} + \frac{x}{1+x^2} = \frac{-2}{2x^2+2} + \frac{x}{1+x^2} = \frac{x-1}{1+x^2} \end{aligned} $$

因此 $\mathrm{d}y = \dfrac{x-1}{1+x^2}\mathrm{d}x$, $\mathrm{d}y\big|_{x=3} = \dfrac{3-1}{1+3^2}\mathrm{d}x = \dfrac{1}{5}\mathrm{d}x$



---

23.11.  设函数 $y=y(x)$ 由参数方程 $\begin{cases} x = t - \sin t, \\ y = 1 - \cos t \end{cases}$ 所确定.

   (1) 试求曲线 $y=y(x)$ 在 $t=\dfrac{\pi}{2}$ 处的切线方程； (2) 计算 $y''(x)$.

(1) 由参数方程, $\dfrac{\mathrm{d}x}{\mathrm{d}t} = 1-\cos t, \dfrac{\mathrm{d}y}{\mathrm{d}t} = \sin t$.

则 $\dfrac{\mathrm{d}y}{\mathrm{d}x} = \dfrac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t} = \dfrac{\sin t}{1-\cos t}$. 

代入 $t=\dfrac{\pi}{2}$, 有 $\left.\dfrac{\mathrm{d}y}{\mathrm{d}x}\right|_{t=\frac{\pi}{2}} = \dfrac{\sin\frac{\pi}{2}}{1-\cos\frac{\pi}{2}} = \dfrac{1}{1-0} = 1$.

即切线斜率为 1. 又 $t=\dfrac{\pi}{2}$ 时 $x = \dfrac{\pi}{2}-\sin\dfrac{\pi}{2} = \dfrac{\pi}{2}-1$, $y=1-\cos\dfrac{\pi}{2}=1$.

从而在 $t=\dfrac{\pi}{2}$ 处切线方程为 $y-1=1\cdot(x-(\dfrac{\pi}{2}-1))$, 即 $x-y-\dfrac{\pi}{2}+2=0$.

(2) 因为 $\dfrac{\mathrm{d}}{\mathrm{d}t}(\dfrac{\mathrm{d}y}{\mathrm{d}x}) = \dfrac{\cos t(1-\cos t) - \sin t \cdot \sin t}{(1-\cos t)^2} = \dfrac{\cos t - (\cos^2 t + \sin^2 t)}{(1-\cos t)^2} = \dfrac{\cos t - 1}{(\cos t - 1)^2} = \dfrac{1}{\cos t - 1}$.

则 $y''(x) = \dfrac{\mathrm{d}^2y}{\mathrm{d}x^2} = \dfrac{\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\mathrm{d}y}{\mathrm{d}x})}{\frac{\mathrm{d}x}{\mathrm{d}t}} = \dfrac{\frac{1}{\cos t-1}}{1-\cos t} = -\dfrac{1}{(1-\cos t)^2}$.

---


**22.7. 已知 $y = \dfrac{x}{2}\sqrt{a^2-x^2} + \dfrac{a^2}{2}\arcsin\dfrac{x}{a}$ (a>0为实常数), 求 $\dfrac{\mathrm{d}y}{\mathrm{d}x}$.**

**解:**

$$
y' = \frac{1}{2}\sqrt{a^2-x^2} - \frac{x^2}{2\sqrt{a^2-x^2}} + \frac{a^2}{2\sqrt{a^2-x^2}}
$$

$$
= \frac{(a^2-x^2) - x^2 + a^2}{2\sqrt{a^2-x^2}} = \frac{2a^2-2x^2}{2\sqrt{a^2-x^2}} = \sqrt{a^2-x^2}
$$

---

**8. 设 $y = f(x)$ 是由方程 $e^{x+y} - 2xy = e$ 所确定的隐函数.**

**(1) 求 $f'(0)$; (2) 计算 $\lim\limits_{x\to 0} \dfrac{(y-1)\sin(ex)}{\sqrt{1+2x^2}-1}$.**

**解:**
**(1)** 对等式 $e^{x+y} - 2xy = e$, 代入 $x=0$ 则 $e^y = e$, 所以 $y=1$.

再对该等式两端对 $x$ 求导有:$e^{x+y}(1+y') - 2(y+xy') = 0$.

代入 $x=0, y=1$, 有 $e(1+y') - 2(1) = 0$, 解得 $y' = \frac{2}{e}-1$.

即 $f'(0) = \frac{2}{e}-1$.

**(2)**

$$
\lim\limits_{x\to 0} \frac{(y-1)\sin(ex)}{\sqrt{1+2x^2}-1} = \lim\limits_{x\to 0} \frac{(y-1) \cdot ex}{\frac{1}{2}(2x^2)} = \lim\limits_{x\to 0} e \frac{y-1}{x}
$$

又因为 $f'(0) = \lim\limits_{x\to 0} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x\to 0} \frac{y-1}{x}$.

则原极限 $= e \cdot f'(0) = e(\frac{2}{e}-1) = 2-e$.

---

**22.9. 已知 $\begin{cases} x = \ln(t + \sqrt{1+t^2}) \\ y = \sqrt{1+t^2} \end{cases}$, 求 $\dfrac{\mathrm{d}y}{\mathrm{d}x}, \dfrac{\mathrm{d}^2y}{\mathrm{d}x^2}$.**

**解:**

由 $x = \ln(t + \sqrt{1+t^2})$, 有 $\dfrac{\mathrm{d}x}{\mathrm{d}t} = \dfrac{1}{\sqrt{1+t^2}}$.

由 $y = \sqrt{1+t^2}$, 有 $\dfrac{\mathrm{d}y}{\mathrm{d}t} = \dfrac{t}{\sqrt{1+t^2}}$.则

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t} = \frac{t/\sqrt{1+t^2}}{1/\sqrt{1+t^2}} = t
$$


$$
\frac{\mathrm{d}^2y}{\mathrm{d}x^2} = \frac{\mathrm{d}}{\mathrm{d}x}(\dfrac{\mathrm{d}y}{\mathrm{d}x}) = \frac{1}{\mathrm{d}x/\mathrm{d}t} = \frac{1}{1/\sqrt{1+t^2}} = \sqrt{1+t^2}
$$

---

**22.10. 曲线 C 的极坐标方程为 $r=e^\theta+\theta$, 求曲线 C 在 $\theta=\frac{\pi}{2}$ 处的切线方程.**

**解:**
利用极坐标方程, 结合极坐标与直角坐标变换公式 $\begin{cases} x=r\cos\theta \\ y=r\sin\theta \end{cases}$.

则曲线C的参数方程为 $\begin{cases} x=(e^\theta+\theta)\cos\theta \\ y=(e^\theta+\theta)\sin\theta \end{cases}$.

从而

$$
\frac{\mathrm{d}y}{\mathrm{d}\theta} = (e^\theta+1)\sin\theta + (e^\theta+\theta)\cos\theta
$$

$$
\frac{\mathrm{d}x}{\mathrm{d}\theta} = (e^\theta+1)\cos\theta - (e^\theta+\theta)\sin\theta
$$

有

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{(e^\theta+1)\sin\theta + (e^\theta+\theta)\cos\theta}{(e^\theta+1)\cos\theta - (e^\theta+\theta)\sin\theta}
$$

在 $\theta=\frac{\pi}{2}$ 处, 切线斜率 $k = \frac{\mathrm{d}y}{\mathrm{d}x}|_{\theta=\pi/2} = \frac{(e^{\pi/2}+1)\sin\frac{\pi}{2} + (e^{\pi/2}+\frac{\pi}{2})\cos\frac{\pi}{2}}{(e^{\pi/2}+1)\cos\frac{\pi}{2} - (e^{\pi/2}+\frac{\pi}{2})\sin\frac{\pi}{2}} = \frac{e^{\pi/2}+1}{-(e^{\pi/2}+\frac{\pi}{2})}$.

且此时 $x = (e^{\pi/2}+\frac{\pi}{2})\cos\frac{\pi}{2}=0$, $y = (e^{\pi/2}+\frac{\pi}{2})\sin\frac{\pi}{2} = e^{\pi/2}+\frac{\pi}{2}$.

从而切线方程为 $y-(e^{\pi/2}+\frac{\pi}{2}) = -\frac{e^{\pi/2}+1}{e^{\pi/2}+\frac{\pi}{2}} x$.

---

**21.6. 设 $y = \dfrac{x^3}{2(x-1)^2}$, 求 $y', y''$.**

**解:**

$$
y' = \frac{1}{2} \frac{3x^2(x-1)^2 - x^3 \cdot 2(x-1)}{(x-1)^4} = \frac{1}{2} \frac{3x^2(x-1) - 2x^3}{(x-1)^3} = \frac{3x^3-3x^2-2x^3}{2(x-1)^3} = \frac{x^3-3x^2}{2(x-1)^3}
$$

$$
y'' = \frac{1}{2} \frac{(3x^2-6x)(x-1)^3 - (x^3-3x^2) \cdot 3(x-1)^2}{(x-1)^6} = \frac{1}{2} \frac{(3x^2-6x)(x-1) - 3(x^3-3x^2)}{(x-1)^4}
$$

$$
= \frac{1}{2} \frac{(3x^3-3x^2-6x^2+6x) - (3x^3-9x^2)}{(x-1)^4} = \frac{1}{2} \frac{3x^3-9x^2+6x-3x^3+9x^2}{(x-1)^4} = \frac{3x}{(x-1)^4}
$$

---

**21.7. 设函数 $y=y(x)$ 由方程 $\sin(xy) + \ln(y-x) = x$ 确定, 求 $y'(0), y''(0)$.**

**解:**
由 $\sin(xy) + \ln(y-x) = x$, 代入 $x=0$, 则 $0+\ln y=0 \implies y=1$.

再对该等式两边同时对 $x$ 求导, 有:

$$
\cos(xy) \cdot (y+xy') + \frac{y'-1}{y-x} = 1 \quad \cdots ①
$$

代入 $x=0, y=1$, 有 $\cos 0 \cdot (1) + \frac{y'-1}{1-0}=1$, 得此时 $y'=1$.


对 ① 式, 再对等式两边对 $x$ 求导, 有

$$
-\sin(xy)(y+xy')^2 + \cos(xy)(y'+y'+xy'') + \frac{y''(y-x)-(y'-1)^2}{(y-x)^2} = 0
$$

代入 $x=0, y=1, y'=1$ 有:

$$
-\sin 0 + \cos 0 (1+1+0) + \frac{y''(1-0) - (1-1)^2}{(1-0)^2} = 0\implies y''=-2
$$

故 $y'(0)=1, y''(0)=-2$.

---

**21.8. 设参数方程 $\begin{cases} x = \ln(1+t^2) \\ y = t - \arctan t \end{cases}$, 求 $\dfrac{\mathrm{d}y}{\mathrm{d}x}, \dfrac{\mathrm{d}^2y}{\mathrm{d}x^2}$.**

**解:**
有 $\dfrac{\mathrm{d}x}{\mathrm{d}t} = \dfrac{2t}{1+t^2}$, $\dfrac{\mathrm{d}y}{\mathrm{d}t} = 1 - \dfrac{1}{1+t^2} = \dfrac{t^2}{1+t^2}$.

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t} = \frac{t^2/(1+t^2)}{2t/(1+t^2)} = \frac{t}{2}
$$

则

$$
\frac{\mathrm{d}^2y}{\mathrm{d}x^2} = \frac{\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\mathrm{d}y}{\mathrm{d}x})}{\mathrm{d}x/\mathrm{d}t} = \frac{1/2}{2t/(1+t^2)} = \frac{1+t^2}{4t}
$$

---


## 计算题: 高阶导数: 莱布尼兹公式

!!! Tips
    每年必考, 计算量可能有点大

---

**24.9. 设函数 $y=e^x \sin x$, 证明 $y^{(n)} = 2^{\frac{n}{2}}e^x \sin(x+\dfrac{n\pi}{4})$.**

**解:用数学归纳法**

当 $n=1$ 时, $y' = e^x\cos x + e^x\sin x = \sqrt{2} e^x (\frac{1}{\sqrt{2}}\cos x + \frac{1}{\sqrt{2}}\sin x) = \sqrt{2} e^x \sin(x+\frac{\pi}{4}) = 2^{1/2} e^x \sin(x+\frac{\pi}{4})$. 成立.

假设 $n=k$ 时有 $y^{(k)} = 2^{k/2}e^x \sin(x+\frac{k\pi}{4})$ 成立.

对 $n=k+1$,

$$
y^{(k+1)} = \frac{\mathrm{d}}{\mathrm{d}x} y^{(k)} = 2^{k/2} [e^x \sin(x+\frac{k\pi}{4}) + e^x \cos(x+\frac{k\pi}{4})]
$$

$$
= 2^{k/2} e^x \sqrt{2} \sin((x+\frac{k\pi}{4})+\frac{\pi}{4}) = 2^{(k+1)/2} e^x \sin(x+\frac{(k+1)\pi}{4}).
$$

成立.因此 $y^{(n)} = 2^{n/2} e^x \sin(x+\dfrac{n\pi}{4})$.

---

**23.10. 已知 $f(x) = \dfrac{x}{\sqrt{1+x}}$, 求 $f^{(6)}(0)$.**


**10. 法① 利用 Leibniz 公式, $f(x) = x \cdot (1+x)^{-1/2}$**
由于

$$
[(1+x)^{-1/2}]^{(n)} = (-\frac{1}{2})(-\frac{3}{2})\cdots(-\frac{1}{2}-n+1)(1+x)^{-1/2-n} = (-1)^n \frac{(2n-1)!!}{2^n}(1+x)^{-\frac{2n+1}{2}}
$$

从而 $f^{(n)}(x) = \binom{n}{0} x \cdot [(1+x)^{-1/2}]^{(n)} + \binom{n}{1} (x)' \cdot [(1+x)^{-1/2}]^{(n-1)} + 0$

$$
f^{(n)}(x) = x[(1+x)^{-1/2}]^{(n)} + n[(1+x)^{-1/2}]^{(n-1)}
$$

代入 $n=6, x=0$

$$
f^{(6)}(0) = 0 + 6 \cdot [(1+x)^{-1/2}]^{(5)}|_{x=0}
$$

$$
[(1+x)^{-1/2}]^{(5)}|_{x=0} = (-1)^5 \frac{1 \cdot 3 \cdot 5 \cdot 7 \cdot 9}{2^5} (1)^{-\frac{11}{2}} = -\frac{945}{32}
$$

则 $f^{(6)}(0) = 6 \cdot (-\frac{945}{32}) = -\frac{2835}{16}$.

**法②, 对 $f(x)$ 进行变形, $f(x) = \frac{x+1-1}{\sqrt{1+x}} = \sqrt{1+x} - \frac{1}{\sqrt{1+x}} = (1+x)^{1/2} - (1+x)^{-1/2}$**

又

$$
[(1+x)^\alpha]^{(n)} = \alpha(\alpha-1)\cdots(\alpha-n+1)(1+x)^{\alpha-n}
$$

从而 $f^{(n)}(x) = [(1+x)^{1/2}]^{(n)} - [(1+x)^{-1/2}]^{(n)}$.

代入 $n=6, x=0$:

$$
[(1+x)^{1/2}]^{(6)}|_{x=0} = (\frac{1}{2})(-\frac{1}{2})(-\frac{3}{2})(-\frac{5}{2})(-\frac{7}{2})(-\frac{9}{2}) = -\frac{945}{64}
$$

$$
[(1+x)^{-1/2}]^{(6)}|_{x=0} = (-\frac{1}{2})(-\frac{3}{2})(-\frac{5}{2})(-\frac{7}{2})(-\frac{9}{2})(-\frac{11}{2}) = \frac{10395}{64}
$$

则 $f^{(6)}(0) = -\frac{945}{64} - \frac{10395}{64} = -\frac{11340}{64} = -\frac{2835}{16}$.

---

**22.11. 已知 $f(x)=\arctan x$, 求 $f^{(7)}(0)$.**

**解:**

对 $f(x)=\arctan x$, 有 $f'(x) = \frac{1}{1+x^2}$.

转化可得 $(1+x^2)f'(x)=1$, 对等式两边求 n 阶导, (n≥1).

由莱布尼兹公式, 有

$$
\binom{n}{0}(1+x^2)f^{(n+1)}(x) + \binom{n}{1}(2x)f^{(n)}(x) + \binom{n}{2}(2)f^{(n-1)}(x) + 0 = 0
$$

$$
(1+x^2)f^{(n+1)}(x) + 2nx f^{(n)}(x) + n(n-1)f^{(n-1)}(x) = 0
$$

此时令 $x=0$, 则对上式有

$$
f^{(n+1)}(0) + n(n-1)f^{(n-1)}(0) = 0 \quad (n\ge 1)
$$

逐项递推可得

$f^{(7)}(0) = -720f'(0) = -720$.

---

**21.10. 设 $f(x) = x\ln(1+x)$, 求 $f^{(100)}(x)$.**

**解:**
由莱布尼兹公式

$$
f^{(100)}(x) = \sum_{k=0}^{100} \binom{100}{k} [x]^{(100-k)} [\ln(1+x)]^{(k)}
$$

由于 $[x]^{(n)}$ 在 $n\ge 2$ 时为 0, 故只剩前两项:

$$
= \binom{100}{100} [x]^{(0)} [\ln(1+x)]^{(100)} + \binom{100}{99} [x]^{(1)} [\ln(1+x)]^{(99)}
$$

$$
= x [\ln(1+x)]^{(100)} + 100 [\ln(1+x)]^{(99)}
$$

$$
[\ln(1+x)]^{(k)} = (-1)^{k-1}(k-1)!(1+x)^{-k}
$$

$$
= x \left(\frac{(-1)^{99}99!}{(1+x)^{100}}\right) + 100 \left(\frac{(-1)^{98}98!}{(1+x)^{99}}\right)
$$

$$
= \frac{-99!x}{(1+x)^{100}} + \frac{100 \cdot 98!}{(1+x)^{99}} = \frac{-99 \cdot 98! x + 100 \cdot 98!(1+x)}{(1+x)^{100}}
$$

$$
= \frac{98!(-99x+100+100x)}{(1+x)^{100}} = \frac{98!(x+100)}{(1+x)^{100}}
$$


---

## 抽象函数导数计算证明

!!! Tips
    结合抽象函数运算性质和导数的定义去做

**21.13. 设函数 $f(x), g(x)$ 定义于 $\mathbb{R}$ 上, 且满足**

**(1) $f(x+y) = f(x)g(y) + f(y)g(x)$;**

**(2) $f(x), g(x)$ 在 $x=0$ 处可导;**

**(3) $f(0)=0, g(0)=1, f'(0)=1, g'(0)=0$.**

**证明: $f(x)$ 在 $\mathbb{R}$ 上可导, 且 $f'(x)=g(x)$.**

**抽象函数与导数结合, 扣住导函数的定义式即可, 基本上把条件和待证列出来关系就明晰了.**


**13. 要证 $f(x)$ 可导, 即证 $\lim\limits_{\Delta x\to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x}$ 对 $x \in \mathbb{R}$ 均存在.**

由题, $f(x+\Delta x) = f(x)g(\Delta x) + f(\Delta x)g(x)$.

又 $f(x)$ 在 $x=0$ 处可导且 $f(0)=0, f'(0)=1$.

则 $\lim\limits_{\Delta x \to 0} \frac{f(\Delta x)-f(0)}{\Delta x} = \lim\limits_{\Delta x \to 0} \frac{f(\Delta x)}{\Delta x} = f'(0)=1$.

类似地, 由 $g(x)$ 在 $x=0$ 处可导, $g(0)=1, g'(0)=0$.

有 $\lim\limits_{\Delta x \to 0} \frac{g(\Delta x)-g(0)}{\Delta x} = \lim\limits_{\Delta x \to 0} \frac{g(\Delta x)-1}{\Delta x} = 0$.

则对 $\forall x \in \mathbb{R}$,

$$
\lim\limits_{\Delta x \to 0} f(x)\frac{g(\Delta x)-1}{\Delta x} = f(x) \lim\limits_{\Delta x \to 0} \frac{g(\Delta x)-1}{\Delta x} = 0
$$

$$
\lim\limits_{\Delta x \to 0} g(x)\frac{f(\Delta x)}{\Delta x} = g(x) \lim\limits_{\Delta x \to 0} \frac{f(\Delta x)}{\Delta x} = g(x)
$$

二者相加有

$$
\lim\limits_{\Delta x \to 0} \frac{f(x)(g(\Delta x)-1) + f(\Delta x)g(x)}{\Delta x} = g(x)
$$

$$
= \lim\limits_{\Delta x \to 0} \frac{f(x)g(\Delta x) + f(\Delta x)g(x) - f(x)}{\Delta x}
$$

$$
= \lim\limits_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x} = g(x)
$$

则 $f(x)$ 在 $\mathbb{R}$ 上可导, 又 $f'(x) = \lim\limits_{\Delta x \to 0} \frac{f(x+\Delta x)-f(x)}{\Delta x} = g(x)$.

则 $f'(x)=g(x)$.


## 大题: 递推数列题

!!! Tips
    主要侧重单调有界定理

---

**23.13. 设函数 $f_n(x) = x^n + x^{n-1} + \dots + x - 1 \quad (n \in \mathbb{N}^+)$.**

**(1) 证明方程 $f_n(x)=0$ 有唯一正根 $x_n$;**

**(2) 证明数列 $\{x_n\}$ 收敛并计算 $\lim\limits_{n\to\infty} x_n$.**

**（1）证明:**

$f_n(0) = -1<0， f_n(1) = n-1\ge0$  由零点存在性定理可知：

$\exists x_n \in (0,1)$ 使得 $f_n(x_n) = 0$

由$f_n(x)$的单调性可知，当$0<x<x_n$时，$f_n(x)<f_n(x_n) = 0$，当$x_n< x < 1$时，$0 = f_n(x_n) < f_n(x)$

所以$x_n$是$f_n(x)$在$(0,1)$的唯一正根

**(2)证明：**

$f_n(x_n) = 0 = f_{n+1}(x_{n+1}) = x_{n+1}^{n+1}+f_n(x_{n+1}) > f_n(x_{n+1})$

结合$f_n(x)$单调性$\implies x_n > x_{n+1} > 0$ 又 $x_n\in(0,1)$有上界$1$

依单调有界定理：$\{x_n\}$收敛

$f_n(x_n) = \dfrac{x_n(x_n^n-1)}{x_n-1}-1 = 0$

设$A = \lim\limits_{n\to\infty} x_n$ 由于$x_n\in(0,1)\implies x_n^n\to0(n\to+\infty)$

$\Rightarrow \dfrac{1-2A}{A-1} = 0$解得$A = \dfrac{1}{2}$



---

**22.14. 设数列 $\{a_n\}$ 满足: $a_1=3, a_{n+1} = \dfrac{1}{2}a_n + \dfrac{3}{a_n+1} \quad (n\ge 1)$.**

**(1) 证明数列 $\{a_n\}$ 收敛; (2) 计算 $\lim\limits_{n\to\infty} a_n$.**

>$分析：2A = A+\dfrac{6}{A+1} \Rightarrow A = 2(A>0)$

$2(a_{n+1}-2) = \dfrac{(a_n-2)(a_n-1)}{a_n+1}$

所以$a_{n+1}-2$和$a_n-2$符号相同 $\implies a_n-2$和$a_1-2$符号相同 

$\therefore a_1>2\Rightarrow a_n>2,\forall n\in N^+$

$\implies \dfrac{1}{2}\dfrac{a_n-1}{a_n+1} = \dfrac{1}{2}(1-\dfrac{2}{a_n+1})<\dfrac{1}{2}$

$\implies 0<a_{n+1}-2<\dfrac{1}{2}(a_n-2)<...<\dfrac{1}{2^n}(a_1-2)\to0(n\to+\infty)$

由夹逼定理可以知道，$\{a_n\}$ 收敛于$2$

---


**21.12. 设数列 $\{x_n\}$ 满足: $0 < x_1 < 3, x_{n+1} = \sqrt{x_n(3-x_n)}, n=1,2,\dots$.**

**试证: 此数列极限存在, 并求该极限.**

由基本不等式可以知道：

$\forall n\in\mathbb{N^+}, 0<x_{n+1} \le \dfrac{x_n+3-x_n}{2} = \dfrac{3}{2}$

$\dfrac{x_{n+1}}{x_n} = \sqrt{\dfrac{3-x_n}{x_n}} > 1(n\ge2)$所以$x_n$ 单调递增$(n\ge2)$

由单调有界定理知，$\{x_n\}$ 收敛

令$L = \lim\limits_{n\to\infty} x_n$

在递推公式中令$n\to+\infty$，有$L = \sqrt{L(3-L)}$

解得$L = \dfrac{3}{2}$

---

## 大题: 微分中值定理


---

**24.13. 已知函数 $f(x)$ 在 $[0,1]$ 上连续, 在 $(0,1)$ 内可导, 且$f(0)=0, f(1)=1$。证明:**

**(1) 存在 $c \in (0,1)$, 使得 $f(c)=1-c$;**

**(2) 存在两个不同的数 $\xi, \eta \in (0,1)$, 使得 $f'(\xi)f'(\eta)=1$.**

(1)略

(2)在$[0,c], [c,1]$上分别使用拉格朗日中值定理：

存在$\xi\in(0,c)$使$f(c)-f(0) = f(c) = 1-c = f'(\xi)c$

存在$\eta\in(c,1)$使$f(1)-f(c) = 1-f(c) = c = f'(\eta)(1-c)$

相乘即证

---

23.12. 设 $f(x)$ 在 $[0,1]$ 上连续，在 $(0, 1)$ 内可导，且 $f(0) = 0, f(1) = 1$.证明：

(1) $\exists c \in (0, 1)$ 使得 $f(c) = \frac{3}{2023}$;

(2) $\exists \xi \ne \eta \in (0, 1)$ 使得 $\frac{3}{f'(\xi)} + \frac{2020}{f'(\eta)} = 2023$.


**本题是一个双中值问题**

**(1)** 令 $g(x) = f(x) - \dfrac{3}{2023}$, 则 $g(0) = f(0) - \dfrac{3}{2023} = -\dfrac{3}{2023} < 0$.

$g(1) = f(1) - \dfrac{3}{2023} = 1 - \dfrac{3}{2023} > 0$, 则有 $g(0)g(1)<0$.

由零点存在定理, $\exists c \in (0,1)$ 使 $g(c)=0$.

即此时有 $f(c) - \dfrac{3}{2023} = 0$, 也即 $f(c) = \dfrac{3}{2023}$.

**(2)** 由拉格朗日中值定理,

$\exists \xi \in (0,c)$ 使 $f'(\xi) = \dfrac{f(c)-f(0)}{c-0} = \dfrac{3}{2023c}$.

$\exists \eta \in (c,1)$ 使 $f'(\eta) = \dfrac{f(1)-f(c)}{1-c} = \dfrac{1-3/2023}{1-c} = \dfrac{2020}{2023(1-c)}$.

则 $\dfrac{3}{f'(\xi)} = 2023c$, $\dfrac{2020}{f'(\eta)} = 2023(1-c)$.

因此 $\exists \xi \neq \eta \in (0,1)$, 使 $\dfrac{3}{f'(\xi)} + \dfrac{2020}{f'(\eta)} = 2023c + 2023(1-c) = 2023$ 成立.

---

**13. 叙述并证明 Rolle(罗尔)定理.**

**本题是定理叙述题, 需要同学们关注知识脉络, 熟悉知识体系**


**定理 4.1.3 (Rolle 罗尔定理)** 如果函数 f 满足:
(1) 在闭区间 $[a,b]$ 上连续;

(2) 在开区间 $(a,b)$ 内可导;

(3) $f(a) = f(b)$.

则至少存在一点 $\xi \in (a,b)$, 使得 $f'(\xi)=0$.


**证明:**

(a) 如果 $f$ 在 $[a,b]$ 上为常数, 则 $(a,b)$ 内的任何点 $\xi$ 都有 $f'(\xi)=0$.

(b) 如果 $f$ 在 $[a,b]$ 上不为常数, 则存在 $x_0 \in (a,b)$, 使得 $f(x_0) \neq f(a)$. 不妨设 $f(x_0) > f(a)$. 于是 $f(a)$ 和 $f(b)$ 都不是 $f$ 在 $[a,b]$ 上的最大值, 其最大值必定在区间 $(a,b)$ 的内部某点$x=\xi$ 取到, 那么由费马定理, 必有 $f'(\xi)=0$.


