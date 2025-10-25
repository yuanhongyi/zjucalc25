# 25-26微甲期中模拟试卷

1.求极限：

$$
\lim\limits_{x \to 0} \frac{(1 - \cos x)(e^{x^2} - 1)(e^x + 1)}{\ln(x + \sqrt{1 + x^2}) \cdot \arctan x \cdot \tan x}
$$

$\because x \to 0$ 时, $x \sim \tan x \sim \arctan x \sim \ln(x + \sqrt{1 + x^2})$, $1 - \cos x \sim \dfrac{1}{2}x^2$, $e^{x^2} - 1 \sim x^2$

$$
\begin{align*}
& \lim\limits_{x \to 0} \frac{(1 - \cos x)(e^{x^2} - 1)(e^x + 1)}{\ln(x + \sqrt{1 + x^2}) \cdot \arctan x \cdot \tan x} \\
=\ & \lim\limits_{x \to 0} \frac{2 \cdot \frac{1}{2}x^2 \cdot x^2}{x \cdot x \cdot x} \\
=\ & 0,
\end{align*}
$$

---

2.用定义证明：若数列$\{a_n\}$单调递增且无上界，则$\lim\limits_{n \to \infty} a_n = +\infty$


**证明：**

要证明 $\lim\limits_{n \to \infty} a_n = +\infty$，根据极限的定义，即需证明：对任意给定的正数 $M$，总存在正整数 $N$，使得当 $n > N$ 时，恒有 $a_n > M$。

1.  **任取 $M > 0$**。

2.  由于数列 $\{a_n\}$ 无上界，因此对于这个给定的 $M$，在数列中必定存在某一项 $a_N$，使得 **$a_N > M$**。

3.  又因为数列 $\{a_n\}$ 是单调递增的，所以对于任何 $n > N$，都有 **$a_n \ge a_N$**。

4.  综合以上两点，当 $n > N$ 时，恒有 $a_n \ge a_N > M$，即 $a_n > M$。

因此，对于任意 $M > 0$，都存在一个正整数 $N$，使得当 $n > N$ 时 $a_n > M$ 成立。根据定义，$\lim\limits_{n \to \infty} a_n = +\infty$。

---


3. 已知函数 $f(x)$ 在 $x_0$ 处可导，且 $f(x_0) \neq 0$，求极限：
$$
\lim\limits_{n \to +\infty} \left( \frac{f(x_0 + \frac{1}{n})}{f(x_0)} \right)^n
$$

**解答：**

$$
\begin{align*}
\text{原式} &= \lim\limits_{n \to +\infty} \exp\left[ n \ln\left(\frac{f(x_0 + \frac{1}{n})}{f(x_0)}\right) \right] \\
&= \exp\left[ \lim\limits_{n \to +\infty} n \ln\left(1 + \frac{f(x_0 + \frac{1}{n}) - f(x_0)}{f(x_0)}\right) \right]
\end{align*}
$$

由于当 $u \to 0$ 时，$\ln(1+u) \sim u$，且当 $n \to +\infty$ 时，$\frac{f(x_0 + \frac{1}{n}) - f(x_0)}{f(x_0)} \to 0$，故：

$$
\begin{align*}
\text{原式} &= \exp\left[ \lim\limits_{n \to +\infty} n \cdot \frac{f(x_0 + \frac{1}{n}) - f(x_0)}{f(x_0)} \right] \\
&= \exp\left[ \frac{1}{f(x_0)} \lim\limits_{n \to +\infty} \frac{f(x_0 + \frac{1}{n}) - f(x_0)}{\frac{1}{n}} \right]
\end{align*}
$$

根据导数的定义，$\lim\limits_{h \to 0} \frac{f(x_0 + h) - f(x_0)}{h} = f'(x_0)$，令 $h = \frac{1}{n}$，则：

$$
\text{原式} = \exp\left[ \frac{1}{f(x_0)} \cdot f'(x_0) \right] = e^{\frac{f'(x_0)}{f(x_0)}}
$$

---


4.求下面的极限

$$
\lim\limits_{n \to \infty} \left( \frac{e}{e^n + 1^2} + \frac{e^2}{e^n + 2^2} + \dots + \frac{e^n}{e^n + n^2} \right)
$$

**解答**

使用夹逼准则

令 $S_n = \sum\limits_{k=1}^{n} \frac{e^k}{e^n + k^2}$。

$$
\sum\limits_{k=1}^{n} \frac{e^k}{e^n + n^2} \le S_n \le \sum\limits_{k=1}^{n} \frac{e^k}{e^n + 1^2}
$$

$$
\begin{align*}
\lim\limits_{n \to \infty} \frac{1}{e^n + 1} \sum\limits_{k=1}^{n} e^k &= \lim\limits_{n \to \infty} \frac{1}{e^n + 1} \cdot \frac{e(e^n - 1)}{e - 1} \\
&= \frac{e}{e-1} \lim\limits_{n \to \infty} \frac{e^n - 1}{e^n + 1} \\
&= \frac{e}{e-1} \lim\limits_{n \to \infty} \frac{1 - e^{-n}}{1 + e^{-n}} \\
&= \frac{e}{e-1}
\end{align*}
$$

$$
\begin{align*}
\lim\limits_{n \to \infty} \frac{1}{e^n + n^2} \sum\limits_{k=1}^{n} e^k &= \lim\limits_{n \to \infty} \frac{1}{e^n + n^2} \cdot \frac{e(e^n - 1)}{e - 1} \\
&= \frac{e}{e-1} \lim\limits_{n \to \infty} \frac{e^n - 1}{e^n + n^2} \\
&= \frac{e}{e-1} \lim\limits_{n \to \infty} \frac{1 - e^{-n}}{1 + n^2e^{-n}} \\
&= \frac{e}{e-1}
\end{align*}
$$

根据夹逼准则，

$$
\lim\limits_{n \to \infty} S_n = \frac{e}{e-1}
$$

---


5.**求函数 $f(x) = (1 + x)^{\frac{x}{\tan(x - \frac{\pi}{4})}}$ 在区间 $(0, 2\pi)$ 内的间断点，并判断其类型。**

$f(x) = e^{\frac{x \ln(1+x)}{\tan(x - \pi/4)}}$。

对于 $x = \frac{3\pi}{4}$ 和 $x = \frac{7\pi}{4}$，当 $x$ 趋于这两个值时，$\tan(x - \frac{\pi}{4})$ 趋于 $\infty$，因此指数 $\frac{x \ln(1+x)}{\tan(x - \pi/4)} \to 0$。所以 $\lim\limits_{x \to 3\pi/4} f(x) = e^0 = 1$ 且 $\lim\limits_{x \to 7\pi/4} f(x) = e^0 = 1$。由于左右极限存在且相等，这两个是可去间断点。

对于 $x = \frac{\pi}{4}$ 和 $x = \frac{5\pi}{4}$，当 $x$ 趋于这两个值时，$\tan(x - \frac{\pi}{4}) \to 0$，而分子 $x \ln(1+x)$ 是一个确定的非零值。因此指数的绝对值趋于 $\infty$，这意味着 $\lim\limits_{x \to \pi/4} f(x)$ 和 $\lim\limits_{x \to 5\pi/4} f(x)$ 至少有一个左右极限是 $\infty$ 或 $0$，极限不存在。所以这两个是无穷间断点，属于第二类间断点。

综上：

$f(x)$ 的间断点有 $x = \frac{\pi}{4}, \frac{3\pi}{4}, \frac{5\pi}{4}, \frac{7\pi}{4}$，其中：

- $x = \frac{\pi}{4}, \frac{5\pi}{4}$ 是 $f(x)$ 的第二类间断点（无穷间断点）。
- $x = \frac{3\pi}{4}, \frac{7\pi}{4}$ 是 $f(x)$ 的可去间断点。
  


---


6.设函数 $f(x) = \begin{cases} \ln\sqrt{x}, & x \ge 1, \\ 2x-1, & x < 1, \end{cases}$， 设 $y = f(f(x))$， 求 $\frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{x=e}$.


**解答：**
$y = f(f(x)) \Rightarrow y=f(u), u=f(x)$

$$
\begin{align*}
\frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{x=e} &= f'(u)f'(x)\bigg|_{x=e} = f'(f(e)) \cdot f'(e) \\
&= f'\left(\frac{1}{2}\right) \cdot f'(e) = 2 \cdot \frac{1}{2e} \\
&= \frac{1}{e}
\end{align*}
$$

---

7.设 $y = y(x)$ 是由方程 $xy + e^y = x + 1$ 确定的隐函数，求 $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}\bigg|_{x=0}$.


**【解】** 将 $x = 0$ 代入方程 $xy + e^y = x + 1$, 解得 $y=0$.
对对方程 $xy + e^y = x + 1$ 两边关于 $x$ 求导得

$$
y + x \frac{\mathrm{d}y}{\mathrm{d}x} + e^y \frac{\mathrm{d}y}{\mathrm{d}x} = 1,
$$

将 $x = 0, y=0$ 代入上式得 $\frac{\mathrm{d}y}{\mathrm{d}x}\bigg|_{x=0} = 1$,

对上式两边再关于 $x$ 求导得

$$
\frac{\mathrm{d}y}{\mathrm{d}x} + \frac{\mathrm{d}y}{\mathrm{d}x} + x \frac{\mathrm{d}^2 y}{\mathrm{d}x^2} + e^y \cdot \left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)^2 + e^y \frac{\mathrm{d}^2 y}{\mathrm{d}x^2} = 0,
$$
将 $x=0, y=0, \frac{\mathrm{d}y}{\mathrm{d}x} = 1$ 代入上式得 $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}\bigg|_{x=0} = -3$.


---


8.设函数 $y = y(x)$ 由参数方程 $\begin{cases} x = t - \ln(1+t), \\ y = t^3 + t^2 \end{cases}$ 所确定, 求 $\frac{\mathrm{d}^2 y}{\mathrm{d}x^2}$.


**【解析】**

$$
\frac{\mathrm{d}y}{\mathrm{d}x} = \frac{\mathrm{d}y/\mathrm{d}t}{\mathrm{d}x/\mathrm{d}t} = \frac{3t^2 + 2t}{t/(1+t)} = \frac{t(3t+2)(1+t)}{t} = (3t+2)(1+t) = 3t^2+5t+2
$$

$$
\frac{\mathrm{d}^2 y}{\mathrm{d}x^2} = \frac{\frac{\mathrm{d}}{\mathrm{d}t}\left(\frac{\mathrm{d}y}{\mathrm{d}x}\right)}{\frac{\mathrm{d}x}{\mathrm{d}t}} = \frac{\frac{\mathrm{d}}{\mathrm{d}t}(3t^2+5t+2)}{t/(1+t)} = \frac{6t+5}{t/(1+t)} = \frac{(6t+5)(1+t)}{t}
$$

---

9.试确定常数 $a, b$ 的值，使函数 $f(x) = \begin{cases} 1 + \ln(1-2x), & x \le 0, \\ a+be^x, & x > 0, \end{cases}$ 在 $x=0$ 处可导，并求出此时的 $f'(x)$.


要使 $f(x)$ 在 $x=0$ 处可导,必有 $f(x)$ 在 $x=0$ 处连续,即 $\lim\limits_{x \to 0^+} f(x) = \lim\limits_{x \to 0^-} f(x) = f(0) = 1$，得 $a+b=1$

$f'_{-}(0) = \lim\limits_{x \to 0^-} \dfrac{f(x)-f(0)}{x} = \lim\limits_{x \to 0^-} \dfrac{1+\ln(1-2x)-1}{x} = -2$

$f'_{+}(0) = \lim\limits_{x \to 0^+} \dfrac{f(x)-f(0)}{x} = \lim\limits_{x \to 0^+} \dfrac{a+be^x-(a+b)}{x} = \lim\limits_{x \to 0^+} \dfrac{b(e^x-1)}{x} = b$

所以 $b=-2$, 于是 $a=3$, 且有 $f'(0)=-2$

$f'(x) = \begin{cases} -\dfrac{2}{1-2x}, & x \le 0, \\ -2e^x, & x>0. \end{cases}$

---


10.设函数 $f(x) = \begin{cases} |x|^\alpha \sin\frac{1}{x}, & x \neq 0, \\ 0, & x = 0, \end{cases}$ 试问: 当实数 $\alpha$ 满足什么条件时,

(1) $f(x)$ 在点 $x=0$ 连续?

(2) $f(x)$ 在点 $x=0$ 可导?

(3) $f(x)$ 可导, 且导函数 $f'(x)$ 在点 $x=0$ 处连续?

**解:**
(1) $f(x)$ 在 $x=0$ 处连续即 $\lim\limits_{x \to 0} f(x) = f(0) = 0$.

又 $-|x|^\alpha \le |x|^\alpha \sin\frac{1}{x} \le |x|^\alpha$, 且 $\alpha > 0$ 时有 $\lim\limits_{x \to 0} |x|^\alpha = 0$.

则此时 $\lim\limits_{x \to 0} f(x) = \lim\limits_{x \to 0} |x|^\alpha \sin\frac{1}{x} = 0 = f(0)$.

而当 $\alpha \le 0$ 时 $\lim\limits_{x \to 0} |x|^\alpha$ 不存在, 从而 $\lim\limits_{x \to 0} f(x)$ 不存在.

**因此可知, $\alpha > 0$ 时 $f(x)$ 在 $x=0$ 处连续.**

(2) $f(x)$ 在 $x=0$ 处可导, 即 $f'(0) = \lim\limits_{x \to 0} \frac{f(x)-f(0)}{x-0}$ 存在, 且此时有 $f'(0) = f'_{+}(0) = f'_{-}(0)$ 成立.

又 $f'_{+}(0) = \lim\limits_{x \to 0^+} \frac{f(x)-f(0)}{x-0} = \lim\limits_{x \to 0^+} \frac{|x|^\alpha \sin\frac{1}{x}}{x} = \lim\limits_{x \to 0^+} x^{\alpha-1} \sin\frac{1}{x}$.

类比 (1) 可知, $\alpha - 1 > 0$ 时, $f'_{+}(0) = \lim\limits_{x \to 0^+} x^{\alpha-1} \sin\frac{1}{x} = 0$, 而当 $\alpha - 1 \le 0$ 时上述极限不存在.

**因此 $\alpha > 1$ 时 $f(x)$ 在 $x=0$ 处可导.**

(3) $f'(x)$ 在 $x=0$ 处连续, 则必有 $f(x)$ 在 $x=0$ 处可导, 由 (2) 则 $\alpha > 1$.

此时再考虑导函数:
$$
f'(x) = \begin{cases} \alpha x^{\alpha-1} \sin\frac{1}{x} - x^{\alpha-2} \cos\frac{1}{x}, & x>0, \\ 0, & x=0, \\ -\alpha (-x)^{\alpha-1} \sin\frac{1}{x} - (-x)^{\alpha-2} \cos\frac{1}{x}, & x<0. \end{cases}
$$
由于 $\alpha > 1$ 时 $\lim\limits_{x \to 0} \alpha |x|^{\alpha-1} \sin\frac{1}{x} = 0$, 则只需考察 $\lim\limits_{x \to 0} -|x|^{\alpha-2} \cos\frac{1}{x}$ 即可.

类似地, $-|x|^{\alpha-2} \le -|x|^{\alpha-2} \cos\frac{1}{x} \le |x|^{\alpha-2}$, 从而 $\alpha-2 > 0$ 时应有 $\lim\limits_{x \to 0} |x|^{\alpha-2} \cos\frac{1}{x} = 0$.

此时有 $\lim\limits_{x \to 0} f'(x) = \lim\limits_{x \to 0^+} f'(x) = 0 = f'(0)$.

且当 $\alpha-2 \le 0$ 时 $\lim\limits_{x \to 0} |x|^{\alpha-2} \cos\frac{1}{x}$ 不存在.

**因此 $\alpha > 2$ 时 $f'(x)$ 在 $x=0$ 处连续.**

---

11.证明费马定理：

**设函数 $f(x)$ 在点 $x_0$ 的某邻域 $U(x_0)$ 内有定义，并且在 $x_0$ 处可导。如果 $f(x)$ 在 $x_0$ 处取得极大值，那么 $f'(x_0) = 0$。**


**证明：**

根据定义，存在 $x_0$ 的一个邻域，对该邻域内的任意 $x$，都有 $f(x) \le f(x_0)$。

因此，当 $x > x_0$ 时，差商 $\frac{f(x)-f(x_0)}{x-x_0} \le 0$；而当 $x < x_0$ 时，该差商 $\frac{f(x)-f(x_0)}{x-x_0} \ge 0$。

由极限的保号性可知 $f'_+(x_0) = \lim\limits_{x \to x_0^+} \frac{f(x)-f(x_0)}{x-x_0} \le 0$，$f'_-(x_0) = \lim\limits_{x \to x_0^-} \frac{f(x)-f(x_0)}{x-x_0} \ge 0$。

所以$f'(x_0)=0$

---

12.

(1) 求函数 $f(x) = x + \dfrac{4}{x^2}$ 在 $x>0$ 上的最小值。

(2) 设数列 $\{x_n\}$ 满足 $x_n > 0$ 且 $x_n + \dfrac{4}{x_{n+1}^2} < 3$。证明 $\{x_n\}$ 收敛并求其极限。


**(1)**

由基本不等式可以知道

$f(x) = \dfrac{x}{2}+\dfrac{x}{2}+\dfrac{4}{x^2}\ge 3\sqrt[3]{1} = 3$

当且仅当 $x=2$ 时，$f(x) = 3$。

**(2) 证明收敛性并求极限**

**① 证明单调性**

由(1)知：$x_{n+1}+\dfrac{4}{x_{n+1}^2} \ge 3\gt x_n+\dfrac{4}{x_{n+1}^2}$

即$x_{n+1}>x_n$  所以数列 $\{x_n\}$ 是单调递增的。

**② 证明有界性**

$x_n < 3 - \dfrac{4}{x_{n+1}^2}<3$，所以$\{x_n\}$ 有上界 3。


根据单调有界准则，$\{x_n\}$ 收敛。

设 $\lim\limits_{n \to \infty} x_n = L$。

对不等式 $x_n + \frac{4}{x_{n+1}^2} < 3$ 两边取极限，得到：$L + \frac{4}{L^2} \le 3$

而由第 (1) 问的结论可知，对于任意 $L>0$，必有 $L + \frac{4}{L^2} \ge 3$。

所以 $L + \frac{4}{L^2} = 3$。

整理该方程：$L^3 - 3L^2 + 4 = 0$。解得 $L=2$ 或 $L=-1$(舍去)

因此，数列 $\{x_n\}$ 的极限是 2。

---

13.设函数 $f(x)$ 在 $[0, 1]$ 上单调可导，且 $f(0)=0, f(1)=1$.

(1) 证明：对于任意正整数 $n$，存在递增的一组数 $0 = x_0 < x_1 < \dots < x_{n-1} < x_n = 1$，使得 $f(x_i) = \dfrac{i}{n}$ 对 $i=0, 1, \dots, n$ 成立。

(2) 证明：存在 $n$ 个互不相同的 $\xi_i \in (0, 1)$，使得 $\sum\limits_{i=1}^{n} \dfrac{1}{f'(\xi_i)} = n$.

**【解析】**

(1)$x_0 = 0,x_1 = 1$显然符合条件，下面构造中间的点：

因为$0<\dfrac{1}{n}<1$，由介质定理知：存在$x_1\in(0,1)$使得$f(x_1) = \dfrac{1}{n}$

因为$\dfrac{1}{n}<\dfrac{2}{n}<1$，由介质定理知：存在$x_2\in(x_1,1)$使得$f(x_2) = \dfrac{2}{n}$

以此类推，存在$x_{n-1}\in(x_{n-2},1)$使得$f(x_{n-1}) = \dfrac{n-1}{n}$


(2)在 $n$ 个子区间 $[x_{i-1}, x_i]$ （其中 $i=1, 2, \dots, n$）上分别应用拉格朗日中值定理。

对于每一个子区间 $[x_{i-1}, x_i]$，都存在一点 $\xi_i \in (x_{i-1}, x_i)$，使得：

$$
f'(\xi_i) = \frac{f(x_i) - f(x_{i-1})}{x_i - x_{i-1}}
$$

因为 $f(x_i) = \dfrac{i}{n}$，我们有：
$$
f'(\xi_i) = \frac{\frac{i}{n} - \frac{i-1}{n}}{x_i - x_{i-1}} = \frac{1/n}{x_i - x_{i-1}}
$$

对上式两边取倒数，得到：

$$
\frac{1}{f'(\xi_i)} = \frac{x_i - x_{i-1}}{1/n} = n(x_i - x_{i-1})
$$

将这 $n$ 个等式相加：

$$
\sum\limits_{i=1}^{n} \frac{1}{f'(\xi_i)} = \sum\limits_{i=1}^{n} n(x_i - x_{i-1})= n (x_n - x_0) =n
$$
