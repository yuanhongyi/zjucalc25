### **期中Tips**



**求极限的, 先判断大致类型**



**2. 计算极限 $\lim\limits_{x \to 0} \left[ \sqrt{\cos\ln(1-2x)} \right]^{\frac{1}{x^2}}$.**

**3. 计算极限 $\lim\limits_{x \to 0} \frac{\sqrt{1+3x^3}-1+x^4\cos\frac{1}{x}}{\ln(1+2x)\tan^2 x}$.**



**喜欢考根式**

**$\lim\limits_{x \to -\infty} x(\sqrt{x^2+6x-1}+x+3)$**

令 $t=-x \to +\infty$

$$ \lim\limits_{t \to +\infty} -t(\sqrt{t^2-6t-1}-t+3) = \lim\limits_{t \to +\infty} -t \frac{(t^2-6t-1)-(t-3)^2}{\sqrt{t^2-6t-1}+t-3} = \lim\limits_{t \to +\infty} -t \frac{-10}{\sqrt{t^2-6t-1}+t-3} = 5 $$



**$\lim\limits_{x \to \infty} \sqrt{x^2-x+1}-ax-b=0$, 求 $a,b$.**



**倒代换, $t=1/x$**



**每年都考一个夹逼定理**



**5. 计算极限 $\lim\limits_{n \to \infty} \left( \frac{1}{n^2+1+\sin 1} + \frac{2}{n^2+1+\sin 2} + \dots + \frac{n}{n^2+1+\sin n} \right)$.**



**换元让无穷小变得更加清楚**

**$\lim\limits_{x \to a} \frac{\tan x - \tan a}{x-a}$**

解: 令 $t=x-a$, 则

$$ \lim\limits_{t\to 0} \frac{\tan(t+a)-\tan a}{t} = \lim\limits_{t\to 0} \frac{\frac{\tan t + \tan a}{1-\tan t \tan a} - \tan a}{t} = \lim\limits_{t\to 0} \frac{\tan t(1+\tan^2 a)}{t(1-\tan t \tan a)} = 1+\tan^2 a $$



**类似地: 当 $x \to 1$ 时, $1 - \frac{m}{1+x+x^2+\dots+x^{m-1}}$ 是 $(x-1)$ 的等价无穷小, 求 $m$.**

解:

设 $g(x) = 1 - \frac{m}{1+x+x^2+\dots+x^{m-1}}$. 我们需要 $\lim\limits_{x\to 1} \frac{g(x)}{x-1} = 1$.

$$ \lim\limits_{x\to 1} \frac{1}{x-1} \left(1 - \frac{m(x-1)}{x^m-1}\right) = \lim\limits_{x\to 1} \frac{x^m-1-m(x-1)}{(x-1)(x^m-1)} $$

应用洛必达法则:

$$ \lim\limits_{x\to 1} \frac{mx^{m-1}-m}{(x^m-1)+m x^{m-1}(x-1)} = \lim\limits_{x\to 1} \frac{m(m-1)x^{m-2}}{mx^{m-1}+m(m-1)x^{m-2}(x-1)+mx^{m-1}} = \frac{m(m-1)}{2m} = \frac{m-1}{2} $$

令 $\frac{m-1}{2}=1 \implies m-1=2 \implies m=3$. ($m>0$).



---

**单调有界基本功不能忘**



**$a_1=3, 2a_{n+1}=a_n+\frac{6}{a_n+1} \quad (n \ge 1)$**

**(1) 证明 $a_n$ 收敛。(2) 求 $\lim\limits_{n\to+\infty} a_n$.**

分析: 若极限存在为 A, 则 $2A = A+\frac{6}{A+1} \Rightarrow A^2+A-6=0 \Rightarrow A=2$ (A>0).

$$ 2(a_{n+1}-2) = a_n-2 + \frac{6}{a_n+1}-2 = \frac{(a_n-2)(a_n+1)+6-2(a_n+1)}{a_n+1} = \frac{(a_n-2)(a_n-1)}{a_n+1} $$

$a_1>2 \Rightarrow a_n>2, \forall n \in N^+$.

$0 < a_{n+1}-2 = \frac{(a_n-2)(a_n-1)}{2(a_n+1)} < \frac{1}{2}(a_n-2) < \dots < (\frac{1}{2})^n(a_1-2)$.

由夹逼定理知 $\lim\limits_{n\to\infty}(a_{n+1}-2)=0$, 故 $\lim\limits_{n\to\infty} a_n = 2$.



**$0<x_1<3, x_{n+1}=\sqrt{x_n(3-x_n)}$, 证明 $x_n$ 有限并求出极限**

$0 < x_{n+1} = \sqrt{x_n(3-x_n)} \le \frac{x_n+(3-x_n)}{2} = \frac{3}{2}$ (AM-GM), $\forall n$.

$\frac{x_{n+1}}{x_n} = \sqrt{\frac{3-x_n}{x_n}}$. 若 $x_n < 3/2$, 则 $3-x_n > x_n \implies$ 增. 若 $x_n > 3/2 \implies$ 减.



**$f_n(x)=x+x^2+\dots+x^n-1$**

**(1) 证明 $f_n(x)$ 有唯一正根 $x_n$。(2) 证明 $x_n$ 收敛并求极限。**

$f_n(0)=-1<0, f_n(1)=n-1 \ge 0$. $f_n(x)$ 单调递增. 故唯一正根 $x_n \in (0,1]$.

我们要研究一些 $x_n$ 的性质.

$f_n(x_n)=0$. $f_{n+1}(x) = f_n(x)+x^{n+1}$.

$f_{n+1}(x_n) = f_n(x_n) + x_n^{n+1} = x_n^{n+1} > 0$.

$f_{n+1}(x_{n+1})=0$.

因为 $f_{n+1}(x)$ 单调递增, 故 $x_n > x_{n+1}$.

$\{x_n\}$ 单调递减有下界 0, 故收敛. 设极限为 $A$.

$f_n(x_n) = \frac{x_n(1-x_n^n)}{1-x_n}-1=0$.

因为 $0<x_n<1$, $\lim\limits_{n\to\infty} x_n^n=0$.

两边取极限: $\frac{A(1-0)}{1-A}-1=0 \implies A=1-A \implies 2A=1 \implies A=1/2$.
