# 期中模拟试题

1. 计算极限

$$ \lim\limits_{x \to \frac{\pi}{6}} \dfrac{1-2\sin{x}}{6x-\pi} $$

!!! Answer
    令 $t=x-\dfrac{\pi}{6}$，原式 $= \lim\limits_{t \to 0} \dfrac{1-2\sin(t+\frac{\pi}{6})}{6t} = \lim\limits_{t \to 0} \dfrac{(1-\cos{t})-\sqrt{3}\sin{t}}{6t} = -\dfrac{\sqrt{3}}{6}$

---

2. 用定义证明：若数列 $\{a_n\}$ 单调递增且无上界，则 $\lim\limits_{n \to \infty} a_n = +\infty$

!!! Answer
    要证明 $\lim\limits_{n \to \infty} a_n = +\infty$，根据极限的定义，即需证明：对任意给定的正数 $M$，总存在正整数 $N$，使得当 $n>N$ 时，恒有 $a_n > M$。

    任取 $M > 0$。由于数列 $\{a_n\}$ 无上界，因此对于这个给定的 $M$，在数列中必定存在某一项 $a_N$，使得 $a_N > M$。

    又因为数列 $\{a_n\}$ 是单调递增的，所以对于任何 $n > N$，都有 $a_n \ge a_N$。

    综合以上两点，当 $n>N$ 时，恒有 $a_n \ge a_N > M$，即 $a_n > M$。

    因此，对于任意 $M > 0$，都存在一个正整数 $N$，使得当 $n>N$ 时 $a_n > M$ 成立。根据定义，$\lim\limits_{n \to \infty} a_n = +\infty$

---

3. 计算极限
    
$$ \lim\limits_{x \to 0} \left( \dfrac{e^{-x} + \cos{\sqrt{\frac{x}{1+x}}}}{2} \right)^{\frac{1}{\tan{x}}} $$

!!! Answer
    $$ = \lim\limits_{x \to 0} e^{\frac{1}{\tan{x}} \ln\left(1 + \frac{e^{-x}-1}{2} + \frac{\cos\sqrt{\frac{x}{1+x}}-1}{2}\right)} = \lim\limits_{x \to 0} e^{\frac{1}{\tan{x}} \left(\frac{e^{-x}-1}{2} + \frac{\cos\sqrt{\frac{x}{1+x}}-1}{2}\right)} $$

    $$ = \lim\limits_{x \to 0} e^{\frac{1}{x} \left(\frac{-x}{2} + \frac{-\frac{1}{2}(\frac{x}{1+x})}{2}\right)} = \lim\limits_{x \to 0} e^{-\frac{1}{2} - \frac{1}{4(1+x)}} = e^{-\frac{1}{2} - \frac{1}{4}} = e^{-\frac{3}{4}} $$

---

4. 计算极限

$$ \lim\limits_{n \to \infty} \dfrac{1!+2!+3!+\dots+n!}{n!} $$

!!! Answer

    解：对前 $n-2$ 项放缩 $1!+2!+\dots+(n-2)! \le (n-2) \cdot (n-2)! < (n-1)!$

    $$ 1!+2!+\dots+n! = 1!+2!+\dots+(n-2)! + (n-1)! + n! $$

    $$< (n-1)! + (n-1)! + n! = 2(n-1)! + n!$$

    $$ \therefore 1 < \text{原式} < \dfrac{2(n-1)!+n!}{n!} $$

    由夹逼定理知该极限为 $1$

---

5. 设 $y=y(x)$ 由 $x^2+y^2+y=e^{x-y}$ 确定，且 $y(0)=0$，求 $y'(0), y''(0)$。

!!! Answer
    解：等式两端对 $x$ 求导

    $$ 2x + 2y \cdot y' + y' = e^{x-y}(1-y') \quad \text{①} $$

    将 $x=0, y=0$ 代入得 $y' = 1-y' \implies y'(0) = \dfrac{1}{2}$

    ① 式再对 $x$ 求导，

    $$ 2+2y'y'+2yy''+y'' = e^{x-y}(1-y')^2 - e^{x-y}y'' $$

    代入 $x=0, y=0, y'=\dfrac{1}{2}$ 得

    $$ 2+2(\frac{1}{2})^2+y'' = (1-\frac{1}{2})^2 - y'' \implies 2+\frac{1}{2}+y'' = \frac{1}{4}-y'' \implies y''(0)=-\frac{9}{8} $$


---

6. 设函数 $f(x) = \begin{cases} \ln{\sqrt{x}}, & x \ge 1 \\ 2x-1, & x < 1 \end{cases}$，设 $y=f(f(x))$，求 $\left. \dfrac{\mathrm{d}y}{\mathrm{d}x} \right|_{x=e}$

!!! Answer
    解答：$y=f(f(x)) \implies y=f(u), u=f(x)$

    $$ \left. \dfrac{\mathrm{d}y}{\mathrm{d}x} \right|_{x=e} = f'(u)f'(x)|_{x=e} = f'(f(e)) \cdot f'(e) $$

    $$ = f'(\frac{1}{2}) \cdot f'(e) = 2 \cdot \dfrac{1}{2e} = \dfrac{1}{e} $$


---


7. 曲线$C$的参数方程为： $\begin{cases} x = t + \sin{t} \\ y = t - \cos{t} \end{cases}$ (1) 求 $t=0$ 处的切线方程 (2) 求 $y''(x)$ 的参数表达式。

!!! Answer
    $$ \dfrac{\mathrm{d}y}{\mathrm{d}x} = \dfrac{\frac{\mathrm{d}y}{\mathrm{d}t}}{\frac{\mathrm{d}x}{\mathrm{d}t}} = \dfrac{1+\sin{t}}{1+\cos{t}} $$

    (1) $\left. \dfrac{\mathrm{d}y}{\mathrm{d}x} \right|_{t=0} = \dfrac{1}{2}$。当 $t=0$ 时，$(x,y)=(0,-1)$。

    切线方程 $y+1 = \dfrac{1}{2}x$

    (2)

    $$ \dfrac{\mathrm{d}^2y}{\mathrm{d}x^2} = \dfrac{\frac{\mathrm{d}}{\mathrm{d}t}(\frac{\mathrm{d}y}{\mathrm{d}x})}{\frac{\mathrm{d}x}{\mathrm{d}t}} = \dfrac{\frac{\cos{t}(1+\cos{t})-(1+\sin{t})(-\sin{t})}{(1+\cos{t})^2}}{1+\cos{t}} =  \dfrac{1+\sin{t}+\cos{t}}{(1+\cos{t})^3} $$

---

8. 极坐标系下曲线 $C:r = 1+\theta e^{-\theta}$，求 $\theta=0$ 处在直角坐标系下的切线方程

!!! Answer
    $\begin{cases} x = r\cos{\theta} = (1+\theta e^{-\theta})\cos{\theta} \\ y = r\sin{\theta} = (1+\theta e^{-\theta})\sin{\theta} \end{cases}$

    $\theta=0 \implies r=1 \implies$ 切点为 $(1,0)$

    $$ \dfrac{\mathrm{d}x}{\mathrm{d}\theta} = (e^{-\theta}-\theta e^{-\theta})\cos{\theta} - (1+\theta e^{-\theta})\sin{\theta} $$

    $$ \dfrac{\mathrm{d}y}{\mathrm{d}\theta} = (e^{-\theta}-\theta e^{-\theta})\sin{\theta} + (1+\theta e^{-\theta})\cos{\theta} $$

    $$ \therefore \dfrac{\mathrm{d}y}{\mathrm{d}x} = \left. \dfrac{\frac{\mathrm{d}y}{\mathrm{d}\theta}}{\frac{\mathrm{d}x}{\mathrm{d}\theta}} \right|_{\theta=0} = \dfrac{1}{1} = 1 $$
    $\therefore$ 切线方程： $y-0=1(x-1) \implies y=x-1$

---

9. 设$y = \dfrac{1+x}{\sqrt{1-x}}$，求 $y^{(100)}$

!!! Answer
    解：$y = \dfrac{1+x}{\sqrt{1-x}} = -\sqrt{1-x} + \dfrac{2}{\sqrt{1-x}} = -(1-x)^{\frac{1}{2}} + 2(1-x)^{-\frac{1}{2}}$

    $$ y^{(n)} = -(\frac{1}{2})(-\frac{1}{2})\dots(\frac{1}{2}-n+1)(1-x)^{\frac{1}{2}-n}(-1)^n + 2(-\frac{1}{2})\dots(-\frac{1}{2}-n+1)(1-x)^{-\frac{1}{2}-n}(-1)^n $$

    $$ = \dfrac{(2n-3)!!(4n-1-x)}{2^n(1-x)^{n+\frac{1}{2}}} $$

    $$ y^{(100)} = \dfrac{197!!(399-x)}{2^{100}(1-x)^{100}\sqrt{1-x}} \quad (x<1) $$


---


10. $f(x) = \begin{cases} x^3\sin{\dfrac{1}{x}} + e^{3x} & (x<0) \\ ax-b & (x \ge 0) \end{cases}$ 在 $x=0$ 处可导，求 $a,b$

!!! Answer

    $f(0^+) = -b$

    $f(0^-) = 0+e^0=1 \implies b=-1$

    $f(0) = a\times0-b = -b = 1$ (连续性)

    $f'_+(0) = \lim\limits_{x \to 0^+} \dfrac{ax+1-1}{x-0} = a$

    $f'_-(0) = \lim\limits_{x \to 0^-} \dfrac{x^3\sin{\dfrac{1}{x}}+e^{3x}-1}{x-0} = \lim\limits_{x\to 0^-} (x^2\sin{\dfrac{1}{x}} + \dfrac{e^{3x}-1}{x}) = 0+3 = 3$


    综上 $a=3, b=-1$

---

11. 求函数 $f(x) = \lim\limits_{n \to \infty} \dfrac{1+x}{1+x^{2n}}$ 的间断点。

!!! Answer
    $$ f(x) = \lim\limits_{n \to \infty} \dfrac{1+x}{1+x^{2n}} = \begin{cases} 1+x & |x|<1 \text{时} \\ 0 & |x|>1 \text{时} \\ 1 & |x|=1 \text{时} \end{cases} $$

    $$ \therefore f(x) = \begin{cases} 1+x & -1 < x < 1 \\ 0 & x<-1 \text{或} x>1 \\ 1 & x=1 \\ 0 & x=-1 \end{cases} $$

    $\therefore$ 间断点为 $x = 1$

---

12. (1) 求函数 $f(x) = x+\dfrac{4}{x^2}$ 在 $x>0$ 上的最小值。
(2) 设数列 $\{x_n\}$ 满足 $x_n>0$ 且 $x_n + \dfrac{4}{x_{n+1}^2} < 3$。证明 $\{x_n\}$ 收敛并求其极限。

!!! Answer
    (1)由基本不等式可以知道

    $$ f(x) = \dfrac{x}{2}+\dfrac{x}{2}+\dfrac{4}{x^2} \ge 3\sqrt{\dfrac{x}{2}\cdot\dfrac{x}{2}\cdot\dfrac{4}{x^2}} = 3\sqrt{1} = 3 $$

    当且仅当 $\dfrac{x}{2}=\dfrac{4}{x^2}$，即 $x=2$ 时， $f(x)=3$。

    (2) 证明收敛性并求极限

    ① 证明单调性

    由(1)知：$x_{n+1} + \dfrac{4}{x_{n+1}^2} \ge 3$，而已知 $x_n + \dfrac{4}{x_{n+1}^2} < 3$

    所以 $x_n < 3 - \dfrac{4}{x_{n+1}^2} \le x_{n+1}$，即 $x_{n+1} > x_n$，所以数列 $\{x_n\}$ 是单调递增的。

    ② 证明有界性

    $x_n < 3 - \dfrac{4}{x_{n+1}^2} < 3$，所以 $\{x_n\}$ 有上界3。

    **根据单调有界准则，$\{x_n\}$ 收敛。**

    设 $\lim\limits_{n \to \infty} x_n = L$。

    对不等式 $x_n + \dfrac{4}{x_{n+1}^2} < 3$ 两边取极限，得到 $L+\dfrac{4}{L^2} \le 3$

    而由第(1)问的结论可知，对于任意 $L>0$，必有 $L+\dfrac{4}{L^2} \ge 3$。

    所以 $L+\dfrac{4}{L^2} = 3$。

    整理该方程：$L^3 - 3L^2 + 4 = 0$。解得 $L=2$ 或 $L=-1$(舍去)

    因此，数列 $\{x_n\}$ 的极限是$\boxed{2}$。

---


13. 已知 $f(x)$ 在 $[a,b]$ 上连续，在 $(a,b)$ 内可导，$b>a>1$。证明：存在 $\xi, \eta \in (a,b)$，使

$$ f'(\eta) = \dfrac{b-a}{\eta(\ln b - \ln a)} f'(\xi) $$

!!! Answer
    解：

    令 $g(x) = \ln x$，在 $[a,b]$ 连续，$(a,b)$ 内可导。

    $g'(x) = (\ln x)' = \dfrac{1}{x} > 0$，$x \in (a,b) \subset (1, +\infty)$

    由拉格朗日中值定理，存在 $\xi \in (a,b)$，使得

    $$ f(b) - f(a) = f'(\xi)(b-a) \quad \cdots ① $$

    由柯西中值定理，存在 $\eta \in (a,b)$，使得

    $$ \dfrac{f'(\eta)}{g'(\eta)} = \dfrac{f(b)-f(a)}{g(b)-g(a)} \implies \dfrac{f'(\eta)}{\frac{1}{\eta}} = \dfrac{f(b)-f(a)}{\ln b - \ln a} \quad \cdots ② $$

    由 ①② 得

    $$ \eta f'(\eta) = \dfrac{f'(\xi)(b-a)}{\ln b - \ln a} $$

    $$ \implies f'(\eta) = \dfrac{b-a}{\eta(\ln b - \ln a)} f'(\xi) $$