## Taylor's Formula

若要证明的式子中含有高阶导数（如$f^{(4)}(\xi)$、$f^{(m)}(\xi)$等），一般要用带拉格朗日余项的泰勒公式：

### 有限区间在某点展开

$$
f(x)=f(x_{0})+f'(x_{0})(x - x_{0})+\dfrac{f^{\prime \prime}(x_{0})}{2!}(x - x_{0})^{2}+\cdots+\dfrac{f^{(n)}(\xi)}{(n)!}(x - x_{0})^{n}
$$

在选取展开点和被展开点时，总的思路是**选取导数值信息多的点作为$x_{0}$(在$x_0$处展开)**。当然，有时也会有其他展开方式，**如将两端点均在中点处展开、将中点分别在两个端点处展开、在任意点处展开等**，具体情况需具体分析。

**例题1** 设$f(x)$在$[-1,1]$三阶连续可导，$f(-1)=0$，$f'(0)=0$，$f(1)=1$，证：$\exists \xi \in(-1,1)$，s.t.$f^{\prime \prime \prime}(\xi)=3$。

!!! Proof

    $f(1)$， $f(-1)$ 分别在 0 处展开：

    $$
    f(1)=f(0)+f^{\prime}(0)+\dfrac{f^{\prime\prime}(0)}{2}+\dfrac{f^{\prime\prime\prime}(\xi_{1})}{6} \quad (0<\xi_{1}<1)
    $$

    $$
    f(-1)=f(0)-f^{\prime}(0)+\dfrac{f^{\prime\prime}(0)}{2}-\dfrac{f^{\prime\prime\prime}(\xi_{2})}{6} \quad (-1<\xi_{2}<0)
    $$

    两式相减得（已知 $f(1)=1, f(-1)=0, f'(0)=0$）：

    $$
    1 - 0 = \dfrac{f^{\prime\prime\prime}(\xi_{1}) + f^{\prime\prime\prime}(\xi_{2})}{6} \implies 3 = \dfrac{f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})}{2}
    $$

    由介值定理得 $\exists \xi \in (\xi_2, \xi_1) \subset (-1,1)$ s.t.

    $$
    f^{\prime\prime\prime}(\xi)=\dfrac{f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})}{2}
    $$

    得证 $f^{\prime\prime\prime}(\xi)=3$。

!!! Tip

    注1：介值定理小推论：$af(u)+bf(v) = (a+b)f(\eta)$

    注2：由达布定理可知，这里的“三阶连续可导”可弱化为“三阶可导”，部分题目有类似情况。

---

**例题2** 设$f(x)$在$[0,1]$二阶可导，$f(0)=f(1)=0$，$[f(x)]_{min}=-1$，证：$\exists \xi \in(0,1)$，s.t.$f^{\prime \prime}(\xi) \geq8$。

!!! Proof
    设 $f(x)$ 在 $x=a \in (0,1)$ 处取得最小值，则 $f(a)=-1, f^{\prime}(a)=0$。

    利用泰勒公式：

    $$
    f(x)=f(a)+f^{\prime}(a)(x-a)+\dfrac{f^{\prime\prime}(\xi)}{2!}(x-a)^{2} = -1+\dfrac{f^{\prime\prime}(\xi)}{2}(x-a)^{2}
    $$

    分别令 $x=0, x=1$ 得：
    
    1.  $0 = -1 + \dfrac{f^{\prime\prime}(\xi_{1})}{2}a^{2} \implies f^{\prime\prime}(\xi_{1}) = \dfrac{2}{a^2} \quad (0<\xi_{1}<a)$
    2.  $0 = -1 + \dfrac{f^{\prime\prime}(\xi_{2})}{2}(1-a)^{2} \implies f^{\prime\prime}(\xi_{2}) = \dfrac{2}{(1-a)^2} \quad (a<\xi_{2}<1)$

    - 若 $0 < a < \dfrac{1}{2}$，则 $a^2 < \dfrac{1}{4}$，故 $f^{\prime\prime}(\xi_{1}) > \dfrac{2}{1/4} = 8$；
    - 若 $\dfrac{1}{2} \le a < 1$，则 $1-a \le \dfrac{1}{2}$，即 $(1-a)^2 \le \dfrac{1}{4}$，故 $f^{\prime\prime}(\xi_{2}) \ge 8$。
    
    综上，至少存在一点 $\xi \in (0,1)$，使 $f^{\prime\prime}(\xi) \ge 8$。

!!! Tip
    极值点蕴含了导数的信息，所以常常将函数在极值点处泰勒展开。

---


**例题3** 设$f(x)$在$x = x_{0}$的邻域内四阶可导，$|f^{(4)}(x)| \leq M(M>0)$，证：对此邻域上任意一个不同于$x_{0}$的点$a$，以及其关于$x_0$的对称点$b$，有$|f^{\prime \prime}(x_{0})-\dfrac{f(a)+f(b)-2f(x_{0})}{(a - x_{0})^{2}}| \leq\dfrac{M}{12}(a - x_{0})^{2}$。

!!! Proof
    由题意 $a+b=2x_{0}$ （即 $b-x_0 = -(a-x_0)$）。将 $f(a), f(b)$ 在 $x_{0}$ 展开：

    $$
    f(a)=f(x_{0})+(a-x_{0})f^{\prime}(x_{0})+\dfrac{(a-x_{0})^{2}}{2}f^{\prime\prime}(x_{0})+\dfrac{(a-x_{0})^{3}}{6}f^{\prime\prime\prime}(x_{0})+\dfrac{(a-x_{0})^{4}}{24}f^{(4)}(\xi_{1})
    $$

    $$
    f(b)=f(x_{0})+(b-x_{0})f^{\prime}(x_{0})+\dfrac{(b-x_{0})^{2}}{2}f^{\prime\prime}(x_{0})+\dfrac{(b-x_{0})^{3}}{6}f^{\prime\prime\prime}(x_{0})+\dfrac{(b-x_{0})^{4}}{24}f^{(4)}(\xi_{2})
    $$

    注意 $(b-x_0) = -(a-x_0)$，则平方项相等，奇次项相反。两式相加，移项整理得：

    $$
    f(a)+f(b)-2f(x_{0})-(a-x_{0})^{2}f^{\prime\prime}(x_{0}) = \dfrac{(a-x_{0})^{4}}{24}(f^{(4)}(\xi_{1})+f^{(4)}(\xi_{2}))
    $$

    两边同除以 $(a-x_0)^2$ 并取绝对值：

    $$
    \left| \dfrac{f(a)+f(b)-2f(x_{0})}{(a-x_{0})^{2}} - f^{\prime\prime}(x_{0}) \right| = \dfrac{(a-x_{0})^{2}}{24} \left| f^{(4)}(\xi_{1})+f^{(4)}(\xi_{2}) \right|
    $$

    由于 $|f^{(4)}(x)| \le M$，则 $|f^{(4)}(\xi_{1})+f^{(4)}(\xi_{2})| \le 2M$。
    故：

    $$
    \text{左边} \le \dfrac{(a-x_{0})^{2}}{24} \cdot 2M = \dfrac{M}{12}(a-x_{0})^{2}
    $$

!!! Tip
    若题干中无具体点的导数信息，可观察欲证结论确定展开点和被展开点，此思想可解决下面两道类题。

!!! Note
    类题1: $f(x)$ 在 $[a,b]$ 二阶连续可导，证 $\exists \xi \in (a,b)$，使得

    $$
    f(a)-2f\left(\dfrac{a+b}{2}\right)+f(b)=\dfrac{(b-a)^{2}}{4}f^{\prime\prime}(\xi)
    $$


!!! Note
    类题2: $f(x)$ 在 $[a,b]$ 三阶连续可导，证：$\exists \xi \in (a,b)$，使

    $$
    f(b) = f(a) + (b-a)f\left(\dfrac{a+b}{2}\right) + \dfrac{(b-a)^3}{24}f^{\prime\prime\prime}(\xi)
    $$

    ---

    将 $f(a)$, $f(b)$ 在 $\frac{a+b}{2}$ 处展开：

    $$
    f(a)=f\left(\dfrac{a+b}{2}\right)+\dfrac{(a-b)}{2}f^{\prime}\left(\dfrac{a+b}{2}\right)+\dfrac{(a-b)^{2}}{8}f^{\prime\prime}\left(\dfrac{a+b}{2}\right)+\dfrac{(a-b)^{3}}{48}f^{\prime\prime\prime}(\xi_{1})
    $$

    $$
    f(b)=f\left(\dfrac{a+b}{2}\right)+\dfrac{(b-a)}{2}f^{\prime}\left(\dfrac{a+b}{2}\right)+\dfrac{(b-a)^{2}}{8}f^{\prime\prime}\left(\dfrac{a+b}{2}\right)+\dfrac{(b-a)^{3}}{48}f^{\prime\prime\prime}(\xi_{2})
    $$

    两式相减，整理得：

    $$
    f(b)-f(a)-f^{\prime}\left(\dfrac{a+b}{2}\right)(b-a)=\dfrac{(b-a)^{3}}{24}\left(\dfrac{f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})}{2}\right)
    $$

    由介值定理得 $\exists \xi \in (a,b)$ s.t. $f^{\prime\prime\prime}(\xi)=\dfrac{f^{\prime\prime\prime}(\xi_{1})+f^{\prime\prime\prime}(\xi_{2})}{2}$。由此得证。


**例题4** 在一条笔直的道路上，一辆汽车从开始启动到刹车停止用单位时间走完了单位路程，证明：至少有一个时间点，其加速度的绝对值不小于4。

!!! Proof
    设运动规律为 $S=S(t)$，则 $S(0)=0, S^{\prime}(0)=0, S(1)=1, S^{\prime}(1)=0$。

    由泰勒公式得：

    $$
    S\left(\dfrac{1}{2}\right)=S(0)+S^{\prime}(0)\left(\dfrac{1}{2}-0\right)+\dfrac{S^{\prime\prime}(\xi_{1})}{2!}\left(\dfrac{1}{2}-0\right)^{2}, \quad \xi_{1}\in\left(0,\dfrac{1}{2}\right)
    $$

    即 $S(\frac{1}{2}) = \frac{1}{8}S^{\prime\prime}(\xi_{1})$。

    又：

    $$
    S\left(\dfrac{1}{2}\right)=S(1)+S^{\prime}(1)\left(\dfrac{1}{2}-1\right)+\dfrac{S^{\prime\prime}(\xi_{2})}{2!}\left(\dfrac{1}{2}-1\right)^{2}, \quad \xi_{2}\in\left(\dfrac{1}{2},1\right)
    $$

    即 $S(\frac{1}{2}) = 1 + \dfrac{1}{8}S^{\prime\prime}(\xi_{2})$。
    两式相减得 $0 = -1 + \dfrac{1}{8}(S^{\prime\prime}(\xi_{1}) - S^{\prime\prime}(\xi_{2}))$，于是 $|S^{\prime\prime}(\xi_{1}) - S^{\prime\prime}(\xi_{2})| = 8$。

    由三角不等式 $|a|+|b| \ge |a-b|$，得 $|S^{\prime\prime}(\xi_{1})|+|S^{\prime\prime}(\xi_{2})| \ge 8$。

    (1) 当 $|S^{\prime\prime}(\xi_{1})| \ge |S^{\prime\prime}(\xi_{2})|$ 时， $|S^{\prime\prime}(\xi_{1})| \ge 4$；

    (2) 当 $|S^{\prime\prime}(\xi_{1})| < |S^{\prime\prime}(\xi_{2})|$ 时， $|S^{\prime\prime}(\xi_{2})| \ge 4$


!!! Tip
    对于端点处函数、导数信息都已知的题目，初学者可能选“两端点处相互展开”，但不够精确，通常将中点在端点处展开利用“对称美”，类似题目如下。

!!! Note
    **类题**: $f(x)$在$[a,b]$上$n$阶可导$(n\geq2)$，满足$f^{(i)}(a)=f^{(i)}(b)=0(i = 1,2,\cdots,n - 1)$，得$|f^{(n)}(\xi)| \geq\dfrac{2^{n - 1}n!}{(b - a)^{n}}|f(b)-f(a)|$

    ---

    **证明：**
    将 $f(x)$ 在 $x=\frac{a+b}{2}$ 处分别向 $a$ 和 $b$ 展开：

    由 $f^{(i)}(a)=0$：

    $$
    f\left(\dfrac{a+b}{2}\right)=f(a)+\dfrac{(b-a)^{n}}{2^{n}n!}f^{(n)}(\xi_{1})
    $$

    由 $f^{(i)}(b)=0$：

    $$
    f\left(\dfrac{a+b}{2}\right)=f(b)+\dfrac{(a-b)^{n}}{2^{n}n!}f^{(n)}(\xi_{2})
    $$

    两式相减得：

    $$
    f(b)-f(a) = \dfrac{(b-a)^n}{2^n n!} f^{(n)}(\xi_1) - \dfrac{(a-b)^n}{2^n n!} f^{(n)}(\xi_2)
    $$

    $$
    |f(b)-f(a)| \le \dfrac{(b-a)^{n}}{2^{n}n!} (|f^{(n)}(\xi_{1})| + |f^{(n)}(\xi_{2})|)
    $$

    取最大值或利用介值性思想，必存在 $\xi$ 使 $|f^{(n)}(\xi)|$ 满足：

    $$
    2|f^{(n)}(\xi)| \ge |f^{(n)}(\xi_{1})| + |f^{(n)}(\xi_{2})| \ge \dfrac{2^n n!}{(b-a)^n} |f(b)-f(a)|
    $$

    即 $|f^{(n)}(\xi)| \ge \dfrac{2^{n-1}n!}{(b-a)^{n}}|f(b)-f(a)|$。




### 无穷区间以及在任意点展开

当题目出现无穷区间时，我们有一种特殊的展开方式

$$
f(x+h) = f(x)+f'(x)h+\dfrac{f^{\prime \prime}(x)}{2!}h^{2}+\cdots+\dfrac{f^{(n)}(\xi)}{n!}h^{n}, \xi位于x和x+h之间
$$

以及

$$
f(x-h) = f(x)-f'(x)h+\dfrac{f^{\prime \prime}(x)}{2!}h^{2}-\cdots+\dfrac{f^{(n)}(\xi)}{n!}h^{n}, \xi位于x和x-h之间
$$

---


**例题5** 设 $f(x)$ 在 $[0,1]$ 二阶可导，且 $|f(x)|\le a$, $|f^{\prime\prime}(x)|\le b$。
**证：** $|f^{\prime}(x)|\le 2a+\dfrac{b}{2}$ 恒成立。

!!! Warning
    注意，本题的结论是对于$(0,1)$上的任意$x$都成立，而不是对于某个特定的$x$成立。请思考怎么展开


!!! Proof
    **证明：**
    $\forall x \in [0,1]$，考虑将 $f(0)$ 和 $f(1)$ 在任意点 $x \in [0,1]$ 展开：

    $$
    f(0)=f(x)+f^{\prime}(x)(0-x)+\dfrac{f^{\prime\prime}(\xi_{0})}{2}(0-x)^{2} \quad (0<\xi_{0}<x)
    $$

    $$
    f(1)=f(x)+f^{\prime}(x)(1-x)+\dfrac{f^{\prime\prime}(\xi_{1})}{2}(1-x)^{2} \quad (x<\xi_{1}<1)
    $$

    两式相减（消去 $f(x)$ 是不行的，应相减构造）：

    $$
    f(1)-f(0) = f'(x)(1) + \dfrac{f''(\xi_1)}{2}(1-x)^2 - \dfrac{f''(\xi_0)}{2}x^2
    $$

    移项得：

    $$
    f^{\prime}(x)=f(1)-f(0)+\dfrac{f^{\prime\prime}(\xi_{0})}{2}x^{2}-\dfrac{f^{\prime\prime}(\xi_{1})}{2}(1-x)^{2}
    $$

    两边取绝对值，由 $|f(x)|\le a, |f^{\prime\prime}(x)|\le b$：

    $$
    |f^{\prime}(x)| \le |f(1)|+|f(0)| + \dfrac{b}{2}x^2 + \dfrac{b}{2}(1-x)^2 \le 2a + \dfrac{b}{2}[x^2 + (1-x)^2]
    $$

    由于 $0 \le x \le 1$，有 $x^2 \le x, (1-x)^2 \le 1-x$，故 $x^2+(1-x)^2 \le x+1-x = 1$。
    所以 $|f^{\prime}(x)|\le 2a+\dfrac{b}{2}$。得证。

    > 注：若不需求出具体的界，可用拉格朗日中值定理：$|f'(x)| = |f'(x) - f'(\frac{1}{2}) + f'(\frac{1}{2})|\le |f'(x)-f(\frac{1}{2})|+|f'(\frac{1}{2})|$



**例题6** $f(x)$在$(0,+\infty)$二阶可导，且$f(x)$和$f''(x)$有界，证明：$f'(x)$在$(0,+\infty)$也有界。

!!! Proof
    **证明：**
    根据泰勒公式：

    $$
    f(x)=f(x_{0})+f^{\prime}(x_{0})(x-x_{0})+\dfrac{1}{2}f^{\prime\prime}(\xi)(x-x_{0})^{2}
    $$

    **$x>1$时**，分别取 $x_{0}=x$，且自变量取 $x+1, x-1$ 有：

    $$
    f(x+1)=f(x)+f^{\prime}(x)+\dfrac{1}{2}f^{\prime\prime}(\xi_1)
    $$

    $$
    f(x-1)=f(x)-f^{\prime}(x)+\dfrac{1}{2}f^{\prime\prime}(\xi_2)
    $$

    两式相减

    $$
    f(x+1)-f(x-1) = 2f'(x) + \dfrac{1}{2}(f''(\xi_1) - f''(\xi_2))
    $$

    除$f'$以外都是有界量，则 $f'$ 有界。

    **$x\in(0,1]$时**，由例题5注可知有界。

**例题7** 设 $f(x)$ 在 $(-\infty,+\infty)$ 二阶可导，记 $M_{i}=\max|f^{(i)}(x)|$ $(i=0,1,2)$。

**证明：** $M_{1}^{2}\le 2M_{0}M_{2}$。

!!! Proof
    **证明：**

    由泰勒展开得：

    $$
    f(x+h)=f(x)+hf^{\prime}(x)+\dfrac{f^{\prime\prime}(\xi)}{2}
    $$

    $$
    f(x-h)=f(x)-hf^{\prime}(x)+\dfrac{f^{\prime\prime}(\eta)}{2}
    $$

    相减得：

    $$
    f(x+h)-f(x-h)=2hf^{\prime}(x)+\dfrac{h^{2}}{2}[f^{\prime\prime}(\xi)-f^{\prime\prime}(\eta)]
    $$

    $$
    2hf^{\prime}(x)=f(x+h)-f(x-h)-\dfrac{h^{2}}{2}[f^{\prime\prime}(\xi)-f^{\prime\prime}(\eta)]
    $$

    $$
    |f^{\prime}(x)| \le \dfrac{M_{0}}{h} + \dfrac{hM_{2}}{2}
    $$

    上面是一个恒成立问题，右端关于 $h>0$ 取最小值，令 $\dfrac{M_0}{h} = \dfrac{hM_2}{2} \implies h=\sqrt{2M_{0}/M_{2}}$ 代入：

    $$
    |f^{\prime}(x)| \le \sqrt{2M_{0}M_{2}} \implies M_{1}^{2} \le 2M_{0}M_{2}
    $$


**类题** 设$f(x)$在$(0,+\infty)$二阶可导，记$M_{i}=\max |f^{(i)}(x)|(i = 0,1,2)$，证明：$M_{1}^{2} \leq 4M_{0}M_{2}$。

!!! Tip
    $f(x-h)$写不了，只有$f(x+h)$可以展开


!!! Note
    定义域缩小为$(0,+\infty)$，对称美消失，界不精确，属正常情况。

### 中值极限

有一种题目，是让你计算有限增量公式中的中值参数的极限。这种题目的思想其实特别简单，只需要自己将$f(x)$重新展开一次，然后和题干给出的展开式对比，得到一个简单等式，然后想办法把中值分离出来即可。

我们往往用**拉格朗日中值定理或者泰勒公式**去剥离中值参数


$f(x)$二阶连续可导，$f''(x)\neq0$，若$f(x + h)=f(x)+f'(x+\theta h)h(0<\theta<1)$，证：$\lim\limits_{h\to0}\theta=\dfrac{1}{2}$。

!!! Proof
    **证明：**
    泰勒展开： $f(x+h)=f(x)+hf^{\prime}(x)+\dfrac{h^{2}}{2}f^{\prime\prime}(\mu)$。

    结合题设：

    $$
    f^{\prime}(x)+\dfrac{h}{2}f^{\prime\prime}(\mu)=f^{\prime}(x+\theta h)
    $$

    整理得

    $$
    f^{\prime}(x+\theta h) - f'(x)= \dfrac{h}{2}f^{\prime\prime}(\mu)
    $$

    由拉格朗日中值定理：存在$\eta\in(x,x+\theta h)$满足

    $$
    \theta hf''(\eta) = \dfrac{h}{2}f''(\mu)
    $$

    $h\to0,\mu,\eta \to x$ 结合二阶导非零，取极限即证

    

$f(x)$有$n + 1$阶连续导数，若$f(a + h)=f(a)+f'(a)h+\dfrac{f''(a)}{2}h^{2}+\cdots+\dfrac{f^{(n)}(a+\theta h)}{n!}h^{n}(0<\theta<1)$且$f^{(n + 1)}(a)\neq0$，证明：$\lim\limits_{h\to0}\theta=\dfrac{1}{n + 1}$。

!!! Proof
    **[解]:**

    $$
    \begin{cases}
    f(a+h) = f(a) + f'(a)\cdot h + \dots + \dfrac{f^{(n)}(a+\theta h)}{n!} \cdot h^n & \text{------ ①} \\
    f(a+h) = f(a) + f'(a)\cdot h + \dots + \dfrac{f^{(n)}(a)}{n!} \cdot h^n + \dfrac{f^{(n+1)}(\xi)}{(n+1)!} \cdot h^{n+1} & \text{------ ②}
    \end{cases}
    $$

    （注： $\xi$ 介于 $a$ 和 $a+h$ 之间，当 $h \to 0$ 时， $\xi \to a$）

    联立 ① ② $\Rightarrow$

    $$
    \dfrac{f^{(n)}(a+\theta h)}{n!} \cdot h^n = \dfrac{f^{(n)}(a)}{n!} \cdot h^n + \dfrac{f^{(n+1)}(\xi)}{(n+1)!} \cdot h^{n+1}
    $$

    $$
    \Rightarrow f^{(n)}(a+\theta h) - f^{(n)}(a) = \dfrac{1}{n+1} \cdot f^{(n+1)}(\xi) \cdot h
    $$

    (此处对左边应用拉格朗日中值定理)

    $$
    \Rightarrow \theta h \cdot f^{(n+1)}(\eta) = \dfrac{1}{n+1} \cdot f^{(n+1)}(\xi) \cdot h
    $$

    （注： $\eta$ 介于 $a$ 和 $a+\theta h$ 之间，当 $h \to 0$ 时， $\eta \to a$）

    令 $h \to 0$ (两边消去 $h$)：

    $$
    \Rightarrow \lim\limits_{h \to 0} \theta \cdot f^{(n+1)}(a) = \dfrac{1}{n+1} \cdot f^{(n+1)}(a)
    $$

    由于 $f^{(n+1)}(a) \neq 0$，消去 $f^{(n+1)}(a)$：

    $$
    \Rightarrow \lim\limits_{h \to 0} \theta = \dfrac{1}{n+1}.
    $$

---

$f(x)$有$n$阶连续导数，$f^{(k)}(x_{0})=0(k = 2,3,\cdots,n - 1)$，$f^{(n)}(x_{0})\neq0$，$f(x_{0}+h)=f(x_{0})+hf'(x_{0}+\theta h)$，其中$0<\theta<1$，证明：$\lim\limits_{h\to0}\theta=\dfrac{1}{\sqrt[n - 1]{n}}$。


!!! Proof
    **[解]:**

    $$
    \begin{cases}
    f(x_0+h) = f(x_0) + f'(x_0+\theta h) \cdot h & \text{------ ①} \\
    f(x_0+h) = f(x_0) + f'(x_0) \cdot h + \underbrace{\left[ \dfrac{f''(x_0)}{2!}h^2 + \dots + \dfrac{f^{(n-1)}(x_0)}{(n-1)!}h^{n-1} \right]}_{=0} + \dfrac{f^{(n)}(\xi)}{n!}h^n & \text{------ ②}
    \end{cases}
    $$

    联立 ① ② $\Rightarrow$

    $$
    f'(x_0+\theta h) \cdot h = f'(x_0) \cdot h + \dfrac{f^{(n)}(\xi)}{n!} \cdot h^n
    $$

    $$
    \Rightarrow f'(x_0+\theta h) - f'(x_0) = \dfrac{f^{(n)}(\xi)}{n!} \cdot h^{n-1} \quad \text{------ ③}
    $$

    又由泰勒展开可得（对 $f'(x)$ 在 $x_0$ 处展开）：

    $$
    f'(x_0+\theta h) = f'(x_0) + \underbrace{f''(x_0) \cdot \theta h + \dfrac{f'''(x_0)}{2!} (\theta h)^2 + \dots}_{=0} + \dfrac{f^{(n-1)}(x_0)}{(n-2)!} (\theta h)^{n-2} + \dfrac{f^{(n)}(\eta)}{(n-1)!} (\theta h)^{n-1}
    $$

    $$
    \Rightarrow f'(x_0+\theta h) = f'(x_0) + \dfrac{f^{(n)}(\eta)}{(n-1)!} \theta^{n-1} h^{n-1} \quad \text{------ ④}
    $$

    （注：$\eta$ 介于 $x_0$ 和 $x_0+\theta h$ 之间）

    将 ④ 代入 ③：

    $$
    \dfrac{f^{(n)}(\eta)}{(n-1)!} \cdot \theta^{n-1} \cdot h^{n-1} = \dfrac{f^{(n)}(\xi)}{n!} \cdot h^{n-1}
    $$

    两边消去 $h^{n-1}$ 并整理（注意 $\frac{n!}{(n-1)!} = n$）：

    $$
    \theta^{n-1} \cdot f^{(n)}(\eta) = \dfrac{1}{n} f^{(n)}(\xi)
    $$

    令 $h \to 0$：
    此时 $\xi \to x_0, \eta \to x_0$。

    $$
    \Rightarrow \lim\limits_{h \to 0} \theta^{n-1} \cdot f^{(n)}(x_0) = \dfrac{1}{n} \cdot f^{(n)}(x_0)
    $$

    由于 $f^{(n)}(x_0) \neq 0$，消去该项：

    $$
    \Rightarrow \lim\limits_{h \to 0} \theta^{n-1} = \dfrac{1}{n} \Rightarrow \lim\limits_{h \to 0} \theta = \dfrac{1}{\sqrt[n-1]{n}} \quad \text{证毕!}
    $$




!!! Tip
    本题给出了很多导数的信息，所以在对估计一阶导数的差值时我们需要使用Taylor展开, 用Lagrange误差就太大了