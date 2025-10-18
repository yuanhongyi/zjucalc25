# 2024 - 2025学年秋冬学期数学分析(甲)I(H)第二次小测


1.已知函数$f(x)$在$\mathbb{R}$上处处可导，且$\forall x \in \mathbb{R}$，$f(x)>0$，则$\lim\limits_{n \to \infty} n\ln\dfrac{f(2024+\dfrac{1}{n})}{f(2024)}=( )$

- A. 0
- B. 其他都不对
- C. $\dfrac{f'(2024)}{f(2024)}$
- D. $\ln f'(2024)$

**C** 

导数定义

---

2.(多选)设函数$f(x)$和$g(x)$都在$\mathbb{R}$上可导，且$g'(x)$在$\mathbb{R}$上恒不为0，则以下命题正确的是( )

- A. $g(x)$是$\mathbb{R}$上严格单调函数
- B. 若$\lim\limits_{x \to 0} f(x)=\lim\limits_{x \to 0} g(x)=0$，则$\lim\limits_{x \to 0} \dfrac{f(x)}{g(x)}=\lim\limits_{x \to 0} \dfrac{f'(x)}{g'(x)}$
- C. 若在$\mathbb{R}$上恒有$f(x) \geq g(x)$，则在$\mathbb{R}$上恒有$f'(x) \geq g'(x)$
- D. 若$\sup_{x \in \mathbb{R}}|f'(x)|<+\infty$，则$f(x)$在$\mathbb{R}$上一致连续

**AD**

A达布定理，D拉格朗日
B选项后面那个极限可能不存在

$f(x) = x^2\sin(\dfrac{1}{x}),g(x) = \sin x$

$\lim\limits_{x\to0}\dfrac{f(x)}{g(x)} = 0,\dfrac{f'(x)}{g'(x)} = \dfrac{2x\sin(\dfrac{1}{x})-\cos(\dfrac{1}{x})}{\cos x}极限不存在$

---

3.设函数$f(x)$定义在$\mathbb{R}$上，满足方程$f^{\prime \prime}(x)+(f'(x))^{2}=e^{x}$且$f'(0)=0$，则有( )

- A. $x = 0$不是$f$的极值
- B. $x = 0$是$f$的极大值
- C. $x = 0$是$f$的极小值
- D. 点$(0, f(0))$是曲线$y = f(x)$的拐点

**C**  

$f''(0) = 1,f'(0) = 0$


!!! 某点导数大于0的一个结论
    $若g(x)在0附近可导，g'(0)>0\iff\lim\limits_{x\to0}\dfrac{g(x)-g(0)}{x}>0$

    $(极限保号性)\Rightarrow\exists\delta>0$
    $x\in(0,\delta),g(x)>g(0). x\in(-\delta,0),g(x)<g(0)$

    但是得不到$g(x)$在$(0,1)$上单调递增

    原因是：单调递增$\Leftarrow\forall x,y\in(0,1),(x-y)(g(x)-g(y))\gt0$

    $x,y$都是任意变量，而我们得到的不等关系有一个是固定的0

---

4.设$f(x)$在$x = 0$点的某个邻域内有定义，且在$x = 0$点处连续。则以下命题正确的个数为( )

(1)若$f$在$x = 0$点处可导，则$\lim\limits_{h \to 0} \dfrac{f(2h)-f(h)}{h}=f'(0)$

(2)若$\lim\limits_{h \to 0} \dfrac{f(2h)-f(h)}{h}=0$，则$f'(0)=0$

(3)若$f$在$x = 0$点处可导，则$\lim\limits_{h \to 0} \dfrac{f(h)-f(-h)}{h}=2f'(0)$

(4)若$\lim\limits_{h \to 0} \dfrac{f(h)-f(-h)}{h}=0$，则$f'(0)=0$

- A. 3
- B. 4
- C. 1
- D. 2

**A** 

对于(1)(3) $令f(x) = x快速求解$

对于(2)

 $\forall \varepsilon>0, \exists\delta > 0$, 当 $|x| < \delta$ 时, 有

$$
-\frac{\varepsilon}{2} < \frac{f(2x) - f(x)}{x} < \frac{\varepsilon}{2}
$$

特别地, 取 $x_n = \dfrac{x}{2^n} (k \in \mathbb{N})$, 上式亦成立. 故有

$$\frac{1}{2^k}\left(- \frac{\varepsilon}{2}\right) < \frac{f\left(\frac{x}{2^{k-1}}\right) - f\left(\frac{x}{2^k}\right)}{x} < \frac{1}{2^k}\left(\frac{\varepsilon}{2}\right),$$

$k=1,2,\cdots,n$. 将此 n 式相加, 注意

$$\sum_{k=1}^{n} \left[f\left(\frac{x}{2^{k-1}}\right) - f\left(\frac{x}{2^k}\right)\right] = f(x) - f\left(\frac{x}{2^n}\right) = f(x) - f(x_n), \quad \sum_{k=1}^{n} \frac{1}{2^k} = 1 - \frac{1}{2^n},$$

有

$$\left(1 - \frac{1}{2^n}\right)\left(- \frac{\varepsilon}{2}\right) < \frac{f(x) - f(x_n)}{x} < \left(1 - \frac{1}{2^n}\right)\left(\frac{\varepsilon}{2}\right).$$

再令 $n \to \infty$, 取极限, 这时 $x_n = \dfrac{x}{2^n} \to 0$, 而 $f$ 在 $0$ 处连续, $\lim\limits_{n \to \infty} f(x_n) = f(0)$, 故

$$-\frac{\varepsilon}{2} \leq \frac{f(x) - f(0)}{x} \leq \frac{\varepsilon}{2}.$$

即

$$\left|\frac{f(x) - f(0)}{x} - 0\right| \leq \frac{\varepsilon}{2} < \varepsilon, \quad f'(0) \text{ 存在且 } f'(0) = 0.$$



---

5.下列函数中，在$x = 0$处不可导的是( )

- A. $f(x)=|x| \sin x$
- B. $f(x)=x \cos |x|$
- C. $f(x)=\cos |x|$
- D. $f(x)=(1 - x) \sin |x|$

**D** 导数定义

---

6.(多选)下述命题中正确的有( )

- A. 设$f(x)=\dfrac{1}{x^{2}-4}$，则$f^{(2024)}(3)=-\dfrac{(2024)!}{4}\left(1-\dfrac{1}{5^{2025}}\right)$ 
- B. $\dfrac{\pi}{e}>\dfrac{\pi^{e}}{e^{\pi}}$
- C. 方程$\ln x-\dfrac{x}{e}+100=0$恰有两个正实根
- D. 若函数$f(x)$在$(0,1)$上可导且有界，则导函数$f'(x)$在$(0,1)$上必有界

A 多了一个负号

$\pi^{e-1}<e^{\pi-1}\iff(e-1)\ln\pi<(\pi-1)\ln e$
$f(x) = \dfrac{\ln x}{x-1},f'(x) = \dfrac{1-\dfrac{1}{x}-\ln x}{(x-1)^2}\le 0$

D $f(x) = \sin(\dfrac{1}{x}),f'(x) = -\dfrac{1}{x^2}\cos(\dfrac{1}{x})$

**BC**

---

7.极坐标系下的曲线$C: r = 2\cos\theta$在$\theta=\dfrac{\pi}{3}$处的切线方程为( )

- A. $x+\sqrt{3}y - 1 = 0$
- B. $x-\sqrt{3}y - 1 = 0$
- C. $x-\sqrt{3}y + 1 = 0$
- D. $x+\sqrt{3}y + 1 = 0$

**C**

$(\dfrac{1}{2},\dfrac{\sqrt{3}}{2})$

---

8.设二阶可导函数$y = y(x)$由方程$e^{x}-e^{y}=xy + 1 - e$确定，则$y^{\prime \prime}(0)=( )$

- A. 1
- B. 0
- C. $\dfrac{1}{e}$
- D. $-1 - e$

**C**

$y(0) = 1$
$e^x-e^yy' = y+xy'\Rightarrow y'(0) = 0$

$e^x-e^y(y')^2-e^yy'' = 2y'+ xy''\Rightarrow y''(0) = \dfrac{1}{e}$ 

---

9.(多选)设$f(x)$在$(0,+\infty)$上有界且可导，则下述结论错误的有( )

- A. 若$\lim\limits_{x \to +\infty} f(x)=0$，则必有$\lim\limits_{x \to +\infty} f'(x)=0$
- B. 若$\lim\limits_{x \to 0^+} f(x)=0$，则必有$\lim\limits_{x \to 0^+} f'(x)=0$
- C. 若$\lim\limits_{x \to +\infty} f'(x)$存在，则必有$\lim\limits_{x \to +\infty} f'(x)=0$
- D. 若$\lim\limits_{x \to 0^+} f(x)$存在，则必有$\lim\limits_{x \to 0^+} f'(x)=0$

**ABD**    

注意A $f(x) = \dfrac{\sin(x^2)}{x},f'(x) = \dfrac{2x^2\cos(x^2)-\sin(x^2)}{x^2}$

C $设f'(+\infty) = k\neq 0, f(2x)-f(x) = xf'(\xi)\to+\infty(x\to+\infty)$

---

10.设$f(x)=x^{3}\left(\sin\dfrac{1}{x}-\ln\left(1+\dfrac{1}{x}\right)\right)-\dfrac{x}{2}$，则$\lim\limits_{x \to \infty} f(x)=( )$

- A. $-\dfrac{1}{2}$
- B. $-\dfrac{1}{6}$
- C. $\dfrac{1}{2}$
- D. $\dfrac{1}{6}$

**C**   

Taylor公式 $-\dfrac{1}{6} - \dfrac{1}{3} = -\dfrac{1}{2}$  