1. 设\( f(x) = \ln\left(x + \sqrt{x^2 + 2024^2}\right) - \ln(2024) \)，则\( f(x) \)是

单选题

- A. 偶函数
- B. 奇函数
- C. 非奇非偶函数
- D. 周期函数
- E. 若其他选项均不能选，就选此项.

**答案：B**

---

2. 下述关于极限计算正确的是

单选题(10分)

- A. \( \lim\limits_{x \to +\infty} (1 + x)^{\frac{1}{x}} = \text{e} \)
- B. \( \lim\limits_{x \to +\infty} (1 + 2x)^{\frac{1}{x}} = \text{e}^2 \)
- C. \( \lim\limits_{x \to +\infty} \left(1 - \frac{1}{x}\right)^{2x} = \text{e}^2 \)
- D. \( \lim\limits_{x \to +\infty} \left(1 + \frac{2}{x}\right)^{x} = \text{e}^2 \)
- E. 若其他选项均不能选，就选此项.

**答案：D**

---

3. 函数\( f(x) = |x - 1|^{\frac{1}{x(x - 2)}} \)的第一类间断点的个数为

单选题(10分)

- A. 3
- B. 2
- C. 1
- D. 0
- E. 若其他选项均不能选，就选此项.

**答案：B**

分析：$x = 0,2$均为第一类间断点

$f(x) = e^{\frac{\ln|x-1|}{x(x-2)} },x\to1,f(x)\to+\infty$

$x = 1$是第二类间断点

---

4. 已知数列$\{a_n\}$（$a_n \in \mathbb{R}, a_n \neq 0$），若$\{a_n\}$发散，则：

单选题(10分)

- A. 数列$\{a_n + \frac{2}{a_n}\}$发散；
- B. 数列$\{a_n - \frac{1}{a_n}\}$发散；
- C. 数列$\{2^{a_n} + 2^{-a_n}\}$发散；
- D. 数列$\{2^{a_n} - 2^{-a_n}\}$发散；
- E. 若其他选项均不能选，就选此项。

**答案：D**

**选项A**反例：$a_n = \begin{cases} 2, & n\text{奇} \\ 1, & n\text{偶} \end{cases}$，$\{a_n\}$发散，但$a_n + \dfrac{2}{a_n} \equiv 3$（收敛），故A错。

**选项B**反例：$a_n = \begin{cases} 1, & n\text{奇} \\ -1, & n\text{偶} \end{cases}$，$\{a_n\}$发散，但$a_n - \dfrac{1}{a_n} \equiv 0$（收敛），故B错。

**选项C**反例：$a_n = \begin{cases} 1, & n\text{奇} \\ -1, & n\text{偶} \end{cases}$，$\{a_n\}$发散，但$2^{a_n} + 2^{-a_n} \equiv \dfrac{5}{2}$（收敛），故C错。

**选项D**反证：若$\{2^{a_n} - 2^{-a_n}\}$收敛，由$2^x$严格单调连续，得$\{a_n\}$收敛，与“$\{a_n\}$发散”矛盾，故D正确。

综上，**A、B、C错误，D正确**。

!!! Tips
    本题来说，画出$f(x)$的图像，若$f(x)$与某个水平线有两个交点，就可以举出反例

!!! Tips
    选项D的分析用到了**严格单调连续函数的保敛性**：
    若函数$f(x)$是**严格单调且连续**的，则：<br>
        若数列$\{x_n\}$收敛，则$\{f(x_n)\}$必收敛；<br>
        反之，若$\{f(x_n)\}$收敛，则$\{x_n\}$必收敛（考虑反函数$f^{-1}$单调连续）。



---

5. 当\( x \to 1 \)时，\(\alpha(x) = 1 + \cos \pi x\)与\(\beta(x) = A(x - 1)^n\)为等价无穷小量，则

单选题(10分)

- A. \( A = \frac{\pi}{2}, n = 2 \);
- B. \( A = -\frac{\pi}{2}, n = 2 \);
- C. \( A = \frac{\pi^2}{2}, n = 2 \);
- D. \( A = -\frac{\pi^2}{2}, n = 2 \);
- E. 若其他选项均不能选，就选此项.

**答案: C**

令$t = x-1\to0$

$1+\cos(\pi t+\pi) = 1-\cos(\pi t)\sim \dfrac{1}{2}(\pi t)^2\sim At^n$



---

6. \( \lim\limits_{x \to +\infty} x \left( \sqrt[3]{x^3 + x} - \sqrt[3]{x^3 - 5x} \right) = \)

单选题(10分)

- A. \( \frac{1}{3} \)
- B. \( \frac{2}{3} \)
- C. \( 2 \)
- D. 不存在
- E. 若其他选项均不能选，就选此项

**答案：C**

$\lim\limits_{x\to+\infty}x^2\left[\left(1+\dfrac{1}{x^2}\right)^{\frac{1}{3}}-1\right] - \lim\limits_{x\to+\infty}x^2\left[\left(1-\dfrac{5}{x^2}\right)^{\frac{1}{3}}-1\right]$

利用$(1+t)^\alpha-1\sim \alpha t(t\to0)$

原式 $=\dfrac{1}{3} - (-\dfrac{5}{3}) = 2$

---

7. 设\(\alpha(x) = \dfrac{8 - x}{4 + x}\)，\(\beta(x) = 2 - \sqrt[3]{x}\)，当\(x \to 8\)时，下列陈述正确的是

单选题(10分)

- A. \(\alpha(x)\)与\(\beta(x)\)为同阶非等价无穷小量；
- B. \(\alpha(x)\)与\(\beta(x)\)为等价无穷小量；
- C. \(\alpha(x)\)是比\(\beta(x)\)更高阶的无穷小量；
- D. \(\alpha(x)\)是比\(\beta(x)\)更低阶的无穷小量；
- E. 若其他选项均不能选，就选此项。

**答案：B**


\(x\to8\), \(\alpha(x) \to 0\), \(\beta(x) \to 0\)

\(\lim\limits_{x \to 8} \dfrac{\alpha(x)}{\beta(x)} = \lim\limits_{x \to 8} \dfrac{\frac{8 - x}{4 + x}}{2 - \sqrt[3]{x}} = \lim\limits_{x \to 8} \dfrac{(8 - x)(2^2 + 2\sqrt[3]{x} + \sqrt[3]{x^2})}{(4 + x)(8 - x)} = 1\)


---

8. 设\( f(x) = \lim\limits_{n \to +\infty} \dfrac{1 + x}{1 + x^{2n}} \)，则：\( f(x) \)

单选题

- A. 没有间断点
- B. 有间断点 \( x = -1 \)
- C. 有间断点 \( x = 0 \)
- D. 有间断点 \( x = 1 \)
- E. 若其他选项均不能选，就选此项

**答案：D**

$x>1,f(x) = 0$

$f(1) = 1$

$-1<x<1,f(x) = 1+x$

$f(-1) = 0$

$x<-1,f(x) = 0$

所以$x = 1$是跳跃间断点


---


9. 设$f(x)$在$\mathbb{R}$上严格单调有界，$\{x_n\}$为实数列，则下列陈述错误的是

多选题(10分)

- A. 若$\{x_n\}$收敛，则$\{f(x_n)\}$必收敛；
- B. 若$\{x_n\}$单调，则$\{f(x_n)\}$必收敛；
- C. 若$\{f(x_n)\}$收敛，则$\{x_n\}$必收敛；
- D. 若$\{f(x_n)\}$单调，则$\{x_n\}$必收敛；
- E. 若其他选项均不能选，就选此项.

**答案：ACD**

解析：

对于A，举反例$f(x) = \begin{cases}
    \arctan x +1(x\ge0) \\
    \arctan x(x\lt0)
\end{cases}, x_n = \dfrac{(-1)^n}{n}$

$f(x)$在数列收敛点处为跳跃间断点即可。

对于B，证明：

由于$f(x)$单调，$x_n$也单调，所以$f(x_n)$单调
由于$f(x)$有界，所以$f(x_n)$有界
根据单调有界定理，即证。

对于C、D：举反例$f(x) = \arctan x, x_n = n$

---

10. 下列陈述正确的是

多选题(10分)

- A. 实数列\(\{a_n\}\)收敛当且仅当\(\forall \varepsilon > 0\)及\(\forall p \in \mathbb{N}_+\)，\(\exists N > 0\)，当\(n > N\)时，有\(|a_{n+p} - a_n| < \varepsilon\)．
- B. 对实数列\(\{a_n\}\)，若\(\{a_n^2\}\)收敛，则\(\{a_n\}\)必收敛；
- C. 对实数列\(\{a_n\}\)，若\(\{a_n^3\}\)收敛，则\(\{a_n\}\)必收敛；
- D. 若有界实数列\(\{a_n\}\)发散，则存在\(\{a_n\}\)的两个收敛子列，且其极限不等．
- E. 若其他选项均不能选，就选此项．

**答案：CD**

解析：

**A顺序有误**。反例：\( a_n = \sum_{k=1}^n \frac{1}{k} \) **调和级数发散**

\( \forall p \in \mathbb{N}_+ \)，\( |a_{n+p} - a_n| = \sum_{k=n+1}^{n+p} \frac{1}{k} < p \cdot \frac{1}{n+1} \)
取 \( N = \left[ \frac{p}{\varepsilon} \right] \)，\( |a_{n+p} - a_n| < \frac{p}{\varepsilon} = \varepsilon \) 


B：\( a_n = (-1)^n \)

C：\( \lim\limits_{n \to \infty} a_n^3 = a^3 \implies \lim\limits_{n \to \infty} a_n = a \)

D：定义


---

## 其他年份第1次小测零散收集

下列陈述**不正确**的是

- A. 若正项数列 $\{a_n\}, \{b_n\}$ 均发散，则 $\{a_n b_n\}$ 必发散
- B. 若数列 $\{a_n\}$ 收敛，$\{b_n\}$ 发散，则 $\{a_n b_n\}$ 必发散
- C. 若数列 $\{a_n\}$ 收敛，$\{b_n\}$ 发散，则 $\{a_n + b_n\}$ 必发散
- D. 若数列 $\{a_n\}$ 满足 $\lim_{n \to +\infty} |a_{n+1} - a_n| = 0$，则数列 $\{a_n\}$ 必收敛

**ABD**

---

设 $f(x)$ 在 $x=2$ 处连续，且 $\lim\limits_{x \to 2} \frac{f(x)}{x-2} = 2$，则 $\lim\limits_{x \to 0} \frac{f(e^{x^2} + \cos 2x)}{\ln(1+x^2)} = \underline{\hspace{2cm}}$.

- A. -2
- B. -1
- C. 2
- D. 1

令$f(x) = 2(x-2)$容易得到答案为**A**


[22-23年的小测pdf](../pdf/quiz1/1.md)