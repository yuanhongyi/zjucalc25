# 模拟题分析与解答

2024-2025学年微积分（甲）I期末考试题型为：
- 1-8 为计算类型的填空题
- 9-13 为稍有些计算过程的解答题
- 14-15 为比较综合的解答题，但是有递进设问

本模拟试卷题型直接参考去年期末考试题型，知识点概览如下

|题号|知识点|难易度|
|----|----|--|
|填空题|||
|1|函数无穷小|简单|
|2|求渐近线方程|简单|
|3|参数方程求导、导数定义|中等|
|4|隐函数求导|简单|
|5|高阶导数计算|简单|
|6|定积分求面积|简单|
|7|定积分求弧长|简单|
|8|反常积分审敛法与计算|中等|
|解答题|||
|9|泰勒公式计算极限|简单|
|10|计算不定积分|简单|
|11|定积分求体积，函数最值|中等|
|12|变上限积分的积分|中等|
|13|递推数列综合题|中等|
|14|定积分、微分中值定理综合题|中等|
|15|定积分、函数凹凸性、数形结合综合题|偏难|

> 第9、14题为2025年研究生入学考试（数学一）真题
> 第13、15题为2024-2025学年微积分（甲）I期末考试真题改编而来

## 试题分析与解答

### 填空题

**（每小题5分）**

1.当$x\to0$时，$\sqrt{1+\tan x} - \sqrt{1+\sin x}$与$x^\alpha$同阶无穷小，则$\alpha=$___________

!!! Answer

    $\boxed{3}$

    $$ \begin{aligned} \lim\limits_{x\to 0^+} \frac{\sqrt{1+\tan x} - \sqrt{1+\sin x}}{x^\alpha} &= \lim\limits_{x\to 0^+} \frac{(1+\tan x) - (1+\sin x)}{x^\alpha(\sqrt{1+\tan x} + \sqrt{1+\sin x})} \\ &= \lim\limits_{x\to 0^+} \frac{\tan x - \sin x}{2x^\alpha} \\ &= \lim\limits_{x\to 0^+} \frac{\sin x(1-\cos x)}{2x^\alpha \cos x} \\ &= \lim\limits_{x\to 0^+} \frac{x \cdot \frac{1}{2}x^2}{2x^\alpha} = \lim\limits_{x\to 0^+} \frac{1}{4} x^{3-\alpha} \end{aligned} $$

    上述极限若不为 $0$ 且存在, 则只能有 $3-\alpha=0$, 解得 $\alpha=3$.



---

2.曲线 $\displaystyle y = x \ln\left(e + \frac{1}{x-1}\right)$ 的斜渐近线方程为 ___________

!!! Answer
    $\boxed{y = x + \frac{1}{e}}$

    1.  **求斜率 $k$**：
        
        $$k = \lim_{x \to \infty} \frac{y}{x} = \lim_{x \to \infty} \ln\left(e + \frac{1}{x-1}\right) = \ln e = 1$$
    2.  **求截距 $b$**：
        
        利用等价无穷小 $\ln(1+t) \sim t$ (当 $t \to 0$)：
        
        $$
        \begin{aligned}
        b &= \lim_{x \to \infty} (y - kx) = \lim_{x \to \infty} x \left[ \ln\left(e + \frac{1}{x-1}\right) - 1 \right] \\
        &= \lim_{x \to \infty} x \left[ \ln\left(e + \frac{1}{x-1}\right) - \ln e \right] \\
        &= \lim_{x \to \infty} x \ln\left( 1 + \frac{1}{e(x-1)} \right) \\
        &= \lim_{x \to \infty} x \cdot \frac{1}{e(x-1)} = \frac{1}{e}
        \end{aligned}
        $$

    **评分：斜率2分，截距3分**

---

3.设函数\(y = f(x)\)由参数方程\(\begin{cases}x = 1 + t^{3}\\y = e^{t^{2}}\end{cases}\)确定，则$\lim\limits_{x\to+\infty}x\left[f\left(2+\dfrac{2}{x}\right)-f(2)\right]$的值为___________

!!! Answer
    $\boxed{\dfrac{4}{3}e}$

    容易看出函数\(f(x)\)可导，且\(f^{\prime}(x)=\dfrac{\text{d}y}{\text{d}x}=\dfrac{e^{t^{2}} \cdot 2t}{3t^{2}}\)，

    当\(x = 2,t = 1\)时，\(f^{\prime}(2)=\left.\dfrac{e^{t^{2}} \cdot 2t}{3t^{2}}\right|_{t = 1}=\dfrac{2}{3}e\)，所以，

    \[
    \lim_{x \to +\infty} x\left(f\left(2+\dfrac{2}{x}\right)-f(2)\right)=2 \lim_{x \to +\infty} \dfrac{f\left(2+\dfrac{2}{x}\right)-f(2)}{\dfrac{2}{x}}=2f^{\prime}(2) = \dfrac{4}{3}e.
    \]



---

4.设函数 $y=y(x)$ 由方程 $\ln(x^2+y) = x^3y+\sin x$ 确定, 则 $\mathrm{d}y\big|_{x=0}=$__________


!!! Answer
    $\boxed{\mathrm{d}x}$

    代入 $x=0$, 则 $\ln y = 0+0=0$, 所以 $y=1$.

    对方程两边同时对 x 求导有

    $$
    \frac{1}{x^2+y}(2x+y') = 3x^2y+x^3y'+\cos x
    $$

    代入 $x=0, y=1$, 则 $\frac{1}{0+1}(0+y') = 0+0+\cos 0 = 1$.

    $y'|_{x=0} = 1$, 则 $\mathrm{d}y|_{x=0} = 1 \cdot \mathrm{d}x = \mathrm{d}x$.


---

5.设函数 $f(x) = x\ln(1+x)$，则 $f^{(5)}(0) =$___________


!!! Answer
    $\boxed{-30}$

    **方法1**

    1.  利用常见展开式：
        
        $$ f(x) = x \cdot \ln(1+x) = x \left( x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + \cdots \right) \\
         = x^2 - \frac{x^3}{2} + \frac{x^4}{3} - \frac{x^5}{4} + \cdots $$

    2.  根据泰勒展开式通项的定义：
        函数 $f(x)$ 在 $x=0$ 处的泰勒展开式通项为 $\frac{f^{(n)}(0)}{n!}x^n$。
        我们需要求 $f^{(5)}(0)$，因此只需要看 **$x^5$ 的系数**。

        $$ f^{(5)}(0) = 5! \cdot \left(-\frac{1}{4}\right) = 120 \cdot \left(-\frac{1}{4}\right) = -30 $$

    **方法2**

    设 $u = \ln(1+x)$，$v = x$。

    因为 $v=x$，其二阶及以上导数均为 0，所以公式只剩前两项：

    $$ f^{(5)}(x) = C_5^0 u^{(5)}(x) \cdot x + C_5^1 u^{(4)}(x) \cdot 1 $$

    代入 $x=0$：$f^{(5)}(0) = u^{(5)}(0) \cdot 0 + 5 u^{(4)}(0) = 5 u^{(4)}(0)$

    我们需要求 $u(x)=\ln(1+x)$ 的 4 阶导数：

    容易计算$u^{(4)}(0) = -6$，代入得$f^{(5)}(0) = 5 \times (-6) = -30$。

---

6.已知曲线 $L$ 的参数方程为 $\begin{cases} x = t - \sin t \\ y = 1 - \cos t \end{cases} (0 \le t \le 2\pi)$，则 $L$ 与 $x$ 轴围成的图形面积为 ___________

!!! Answer
    $\boxed{3\pi}$

    参数方程 $\begin{cases} x = x(t) \\ y = y(t) \end{cases}$ 围成的面积公式为 $S = \displaystyle\int_{t_1}^{t_2} y(t) \mathrm{d}(x(t))$。

    $$
    \begin{aligned}
    S &= \int_{0}^{2\pi} (1 - \cos t)^2 \mathrm{d}t \\
    &= \int_{0}^{2\pi} (1 - 2\cos t + \cos^2 t) \mathrm{d}t\\
    &= \int_{0}^{2\pi} \left( \frac{3}{2} - 2\cos t + \frac{1}{2}\cos 2t \right) \mathrm{d}t\\
    &= 3\pi
    \end{aligned}
    $$

---


7.已知曲线 $L$ 的极坐标方程为 $r = 1 + \cos \theta \ (0 \le \theta \le 2\pi)$，则曲线 $L$ 的全长为 ___________

!!! Answer
    $\boxed{8}$

    极坐标下弧长公式为 $s = \displaystyle\int_{\alpha}^{\beta} \sqrt{r^2 + (r')^2} \mathrm{d}\theta$。

    由于图形关于极轴对称，可以先算上半部分 ($0 \le \theta \le \pi$) 再乘以 2。

    $$
    \begin{aligned}
    s &= 2 \int_{0}^{\pi} 2\cos \frac{\theta}{2} \mathrm{d}\theta \\
    &= 8
    \end{aligned}
    $$

---

8.设 $\displaystyle\int_{1}^{+\infty} \left[ \dfrac{2x^2+bx+a}{x(2x+a)} - 1 \right]\mathrm{d}x = 1$，则$a =$_________$b =$ __________

!!! Answer
    $\boxed{a = 2e-2}, \boxed{b = 2e-2}$

    通分，$\displaystyle\int_{1}^{+\infty} \left[ \dfrac{2x^2+bx+a}{x(2x+a)} - 1 \right]\mathrm{d}x = \displaystyle\int_{1}^{+\infty} \dfrac{(b-a)x+a}{x(2x+a)}\mathrm{d}x$。

    要想收敛，必须有 $a=b$（否则 $x \to +\infty$ 时，$f(x) = \dfrac{(b-a)x+a}{x(2x+a)} = O\left(\dfrac{1}{x}\right)$，积分显然发散）。

    此时，$I = \displaystyle\int_{1}^{+\infty} \dfrac{a}{x(2x+a)}\mathrm{d}x = \displaystyle\int_{1}^{+\infty} \left( \dfrac{1}{2x} - \dfrac{1}{2x+a} \right)\mathrm{d}(2x) = \ln\dfrac{2x}{2x+a} \Big|_1^{+\infty} = 0 - \ln\dfrac{2}{2+a} = 1$。

    故 $\dfrac{2}{2+a} = \dfrac{1}{e}$，解得 $a = 2(e-1)$，故 $a=b=2(e-1)$。

    **评分：答对一个给3分，两个给5分**

---

### 解答题

（本题6分）9.求极限 $\displaystyle \lim_{x\to 0} \left(\frac{1}{x} - \frac{\ln(1+x)}{x\sin x}\right)$.

!!! Answer
    $\boxed{\dfrac{1}{2}}$

    **【分析】**
    本题属于 $\infty - \infty$ 型未定式，首先需要通分将其转化为 $\frac{0}{0}$ 型，然后可以利用等价无穷小代换、泰勒公式或洛必达法则求解。

    **【解答】**
    解：原式通分可得

    $$ L = \lim_{x\to 0} \frac{\sin x - \ln(1+x)}{x\sin x} $$

    由于当 $x \to 0$ 时，$\sin x \sim x$

    $$ L = \lim_{x\to 0} \frac{\sin x - \ln(1+x)}{x^2} $$

    当 $x \to 0$ 时，$\sin x = x - \dfrac{1}{6}x^3 + o(x^3), \ln(1+x) = x - \dfrac{1}{2}x^2 + o(x^2)$，
    
    代入原式得：

    $$ 
    \begin{aligned}
    L &= \lim_{x\to 0} \frac{\left[x - o(x^2)\right] - \left[x - \frac{1}{2}x^2 + o(x^2)\right]}{x^2} \\ 
    &= \lim_{x\to 0} \frac{\frac{1}{2}x^2 + o(x^2)}{x^2} \\ 
    &= \frac{1}{2} 
    \end{aligned} 
    $$

    **评分：写出泰勒展开式酌情给1-2分**

---

（本题6分）10.求不定积分

$$
\int \dfrac{\ln x}{(1 + x^{2})^{\frac{3}{2}}}\mathrm{d}x
$$

!!! Answer

    令 $x = \tan t$。

    $$
    \begin{aligned}
    \text{原式} &= \int \dfrac{\ln \tan t}{\sec^3 t} \sec^2 t \mathrm{d}t = \int \cos t \ln \tan t \mathrm{d}t = \int \ln \tan t \mathrm{d}(\sin t) \\
    &= \sin t \ln \tan t - \int \sin t \dfrac{\sec^2 t}{\tan t} \mathrm{d}t = \sin t \ln \tan t - \int \sec t \mathrm{d}t \\
    &= \dfrac{x}{\sqrt{1+x^2}} \ln x - \ln|x+\sqrt{1+x^2}| + C
    \end{aligned}
    $$

    **评分：使用换元法算出关于$t$的正确积分给5分，回代形式有多种，可以不化简**

---


（本题8分）11.设\(t > 0\)，平面有界区域\(D\)由曲线\(y = \sqrt{x}e^{-x}\)与直线\(x = t\)，\(x = 2t\)及\(x\)轴围成，\(D\)绕\(x\)轴旋转一周所成旋转体的体积为\(V(t)\)，求\(V(t)\)的最大值。

!!! Answer

    \(V(t)=\displaystyle\int_{t}^{2t}\pi x e^{-2x}\mathrm{d}x=-\dfrac{\pi}{2}\left[(2t + \dfrac{1}{2})e^{-4t}-(t + \dfrac{1}{2})e^{-2t}\right]\)

    则\(V^{\prime}(t)=-\pi te^{-2t}(1 - 4e^{-2t})\)，令\(V^{\prime}(t)=0\Rightarrow t=\ln 2\)，

    \(\because t\in(\ln 2-\delta,\ln 2)\)有\(V^{\prime}(t)>0\)，\(t\in(\ln 2,\ln 2+\delta)\)有\(V^{\prime}(t)<0\)，

    \(\therefore t = \ln 2\)为\(V(t)\)的极大值点即最大值点，

    故最大值为\(V(\ln 2)=\dfrac{\pi}{16}(\ln 2+\dfrac{3}{4})\)。

    **评分：求出正确函数得4分，求出极值点得2分，结果正确得到剩下分数**

---

（本题6分）12.设 $f(x)=\displaystyle\int_{1}^{x} \dfrac{\ln(1+t)}{t} \mathrm{d}t$，计算 $\displaystyle\int_{0}^{1} \dfrac{f(x)}{\sqrt{x}} \mathrm{d}x$

!!! Answer

    $$
    \begin{aligned}
    \displaystyle\int_{0}^{1} \dfrac{f(x)}{\sqrt{x}} \mathrm{d}x &= 2\displaystyle\int_{0}^{1} f(x) \mathrm{d}\sqrt{x} = 2\sqrt{x} f(x) \bigg|_{0}^{1} - 2\displaystyle\int_{0}^{1} \sqrt{x} \mathrm{d}f(x) \\
    &= \boxed{-2 \displaystyle\int_{0}^{1} \sqrt{x} \dfrac{\ln(1+x)}{x} \mathrm{d}x} \xrightarrow{x \to x^2} -4 \displaystyle\int_{0}^{1} \ln(1+x^2) \mathrm{d}x \\
    &= -4 \ln 2 + 8 \displaystyle\int_{0}^{1} \dfrac{x^2}{1+x^2} \mathrm{d}x = 8 - 2\pi - 4\ln 2
    \end{aligned}
    $$

    **评分：分部积分法结果正确得2分**


---

13.已知数列 $\{a_n\}, \{b_n\}$ 满足 $a_n = \ln(1+a_n) + b_n$，其中 $0 < a_n < \dfrac{1}{n^2}$

（本小题6分）(1) 证明：$0 < b_n < \dfrac{1}{2}a_n^2$；

（本小题4分）(2) $\lim\limits_{n\to\infty} \left(\dfrac{b_1}{a_1} + \dfrac{b_2}{a_2} + \cdots + \dfrac{b_n}{a_n}\right)$ 存在。


!!! Answer
    (1)由题设条件 $a_n = \ln(1+a_n) + b_n$ 可得：

    $$ b_n = a_n - \ln(1+a_n) = \displaystyle\int_0^{a_n} \left(1 - \frac{1}{1+t}\right) \mathrm{d}t = \displaystyle\int_0^{a_n} \frac{t}{1+t} \mathrm{d}t $$

    因为 $a_n > 0$，所以积分区间为 $[0, a_n]$。当 $t \in (0, a_n]$ 时，显然有：$0 < \dfrac{t}{1+t} < t$

    $$ \displaystyle\int_0^{a_n} 0 \,\mathrm{d}t < \displaystyle\int_0^{a_n} \frac{t}{1+t} \mathrm{d}t < \displaystyle\int_0^{a_n} t \,\mathrm{d}t $$

    即：

    $$ 0 < b_n < \left[ \frac{1}{2}t^2 \right]_0^{a_n} = \dfrac{1}{2}a_n^2 $$

    故不等式 $0 < b_n < \dfrac{1}{2}a_n^2$ 成立。

    **(2)** 记 $S_n = \sum\limits_{k=1}^n \dfrac{b_k}{a_k}$。要证明极限存在，即证明级数 $\sum\limits_{n=1}^{\infty} \dfrac{b_n}{a_n}$ 收敛。

    由 (1) 中结论 $0 < b_n < \dfrac{1}{2}a_n^2$，两边同时除以 $a_n$（已知 $a_n > 0$）：

    $$ 0 < \dfrac{b_n}{a_n} < \dfrac{1}{2}a_n $$

    根据题设条件， $0 < a_n < \dfrac{1}{n^2}$，代入上式可得：

    $$ 0 < \dfrac{b_n}{a_n} < \dfrac{1}{2n^2} $$

    记$S_n = \sum\limits_{k=1}^n \dfrac{b_k}{a_k}$，则$S_n < \sum\limits_{k=1}^n \dfrac{1}{2k^2}< 1$(裂项易得)

    故$S_n$有上界，且$S_n$单调递增，故$S_n$收敛。
    
    故 $\lim\limits_{n\to\infty} \left(\dfrac{b_1}{a_1} + \dfrac{b_2}{a_2} + \cdots + \dfrac{b_n}{a_n}\right)$ 存在。

    **评分：（1）（2）小问方法不唯一，正确即可**
---

14.设可导函数 $f(x)$ 严格单调递增且满足 $\displaystyle\int_{-1}^1 f(x)\mathrm{d}x=0$，记 $a=\displaystyle\int_0^1 f(x)\mathrm{d}x$.

（本小题5分）（1）证明 $a>0$；

（本小题5分）（2）令 $F(x)=a(1-x^2)+\displaystyle\int_1^x f(t)\mathrm{d}t$，证明：存在 $\xi \in (-1,1)$，使得 $F''(\xi)=0$.


!!! Answer

    (1)用反证法。假设 $a\le0$

    因为$f(x)$严格单调递增，所以当$x\in(0,1)$时，$f(x)>f(0)$，当$x\in(-1,0)$时，$f(x)<f(0)$

    $\implies 0\ge \boxed{a = \displaystyle\int_0^1 f(x)\mathrm{d}x} > \boxed{\displaystyle\int_0^1 f(0)\mathrm{d}x = f(0) = \displaystyle\int_{-1}^0 f(0)\mathrm{d}x} > \displaystyle\int_{-1}^0 f(x)\mathrm{d}x$

    则$\displaystyle\int_{-1}^1 f(x)\mathrm{d}x = \displaystyle\int_{-1}^0 f(x)\mathrm{d}x + \displaystyle\int_0^1 f(x)\mathrm{d}x < 0$矛盾！

    故$a>0$

    (2)由题可知 $F(-1)=F(0)=F(1)=0$
    
    又因为 $F(x)$ 在 $[-1,1]$ 上连续且可导，由罗尔定理可知：

    $\exists\xi_1\in(-1,0)$，$\exists\xi_2\in(0,1)$，，使得$F'(\xi_1) = 0, F'(\xi_2) = 0$

    再次使用罗尔定理：$\exists\xi\in(\xi_1,\xi_2)$使得 $F''(\xi) = 0$

    **评分：（1）方法不唯一，正确即可**
    **(2)观察到3个零点得3分**
---


15.已知函数 $f(x)$ 在区间 $[0,1]$ 上具有二阶连续导数，且 $f''(x) < 0$，$f(0) = f(1) = 0$。

（本小题7分）(1) 证明：存在唯一的 $x_0 \in (0,1)$ 使得 $f'(x_0) = 0$，且
$$ \int_0^1 f(x) \mathrm{d}x > \frac{1}{2} f(x_0) $$

（本小题7分）(2) 记 $k_1 = f'(0)$， $k_2 = f'(1)$，证明：
$$ \int_0^1 f(x) \mathrm{d}x < \frac{k_1 k_2}{2(k_2 - k_1)} $$


!!! Answer

    (1)

    因为 $f(0)=f(1)=0$ 由罗尔定理知道：$\exists x_0 \in (0,1)$，使得 $f'(x_0) = 0$。
    
    因为 $f''(x)<0$ 知 $f'(x)$严格递减，因此有唯一零点$x_0$。
    
    在区间 $[0, x_0]$ 上，令辅助函数 $F(x) = f(x) - \dfrac{f(x_0)}{x_0}x$。
    
    显然 $F(0) = 0$，$F(x_0) = 0$。由罗尔定理知：$\exists\xi\in(0,x_0)$满足$F'(\xi) = 0$。
    
    又由$F''(x) = f''(x)<0$可知$F'(x)$严格递减，因此有唯一零点$\xi$。并且$x\in(0,\xi)$时，$F'(x)>0$，$F(x)$单调递增。$x\in(\xi,x_0)$时，$F'(x)<0$，$F(x)$单调递减

    所以$\forall x\in(0,x_0)$有$F(x)\gt0\iff f(x)\gt \dfrac{f(x_0)}{x_0}x, \forall x\in(0,x_0)$
    

    同理可证 **$f(x) > \dfrac{f(x_0)}{x_0-1}(x-1)$**。

    综上，在 $[0,1]$ 上积分：
    $$
    \begin{aligned}
    \int_0^1 f(x) \mathrm{d}x &= \int_0^{x_0} f(x) \mathrm{d}x + \int_{x_0}^1 f(x) \mathrm{d}x \\
    &> \int_0^{x_0} \frac{f(x_0)}{x_0}x \mathrm{d}x + \int_{x_0}^1 \frac{f(x_0)}{x_0-1}(x-1) \mathrm{d}x\\
    &= \dfrac{f(x_0)}{2}
    \end{aligned}
    $$

    ***

    (2)

    记 $k_1 = f'(0)$，$k_2 = f'(1)$。
    对 $f(x)$ 在 $x=0$ 处应用**泰勒公式**（拉格朗日余项）：
    $$
    f(x) = f(0) + f'(0)x + \frac{1}{2}f''(\xi_1)x^2 \quad (0 < \xi_1 < x)
    $$
    因 $f(0)=0$，$f''(\xi_1) < 0$，故$f(x) < k_1 x$。

    同理，$f(x) < k_2(x-1)$。

    令$x_p = \dfrac{-k_2}{k_1 - k_2}$

    $$
    \int_0^1 f(x) \mathrm{d}x < \int_0^{x_p} k_1 x \mathrm{d}x + \int_{x_p}^1 k_2(x-1) \mathrm{d}x = \dfrac{k_1 k_2}{2(k_2 - k_1)}
    $$

    **评分：（1）（2）本质上在探讨函数积分值和内接三角形、外切三角形面积的关系，若有画出图形说明却没有严谨证明者，可以得到一半分数**
    **（1）证明零点1分，证明割线不等式5分，放缩1分**
    **（2）证明切线不等式5分，取出交点1分，放缩1分**