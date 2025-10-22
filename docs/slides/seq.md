# 数列极限梳理与拓展

## 基础回顾

- **数列极限定义**: $\epsilon-N$ 语言, 无穷大数列

**定义1.1.2 (收敛数列)**

设 $\{a_{n}\}$ 是一个数列, 如果存在 $a\in\mathbb{R}$, 使得 $\forall\epsilon>0$, $\exists N\in\mathbb{N}_{+}$ 当 $n\ge N$ 时, 都有

$$|a_{n}-a|<\epsilon,$$

就称数列 $\{a_{n}\}$ 是**收敛的**并且收敛于a, 记为 $\lim\limits_{n\rightarrow\infty}a_{n}=a$ 或者 $a_{n}\rightarrow a$。

若不成立, 就称 $\{a_{n}\}$ 是**发散的**。


**定义1.1.19 (无穷大数列)**

设 $\{a_{n}\}$ 是一个数列, 如果 $\forall M>0$, $\exists N\in\mathbb{N}_{+}$ 当 $n\ge N$ 时, 都有 $|a_{n}|>M$, 那么称 $\{a_{n}\}$ 为无穷大数列, 记为 $\lim\limits_{n\rightarrow\infty}a_{n}=\infty$。

特别地, 如果 $a_n > M$ (或 $a_n < -M$), 则称 $\{a_{n}\}$ 趋于 $+\infty$ (或 $-\infty$)。


!!! tip

    上述定义的否定也要掌握。

    数列极限的几何意义是什么？



- **数列极限性质**: 唯一性、有界性、保号性、四则运算 (注意极限要存在才能用)

**定理 1.1.9 (有界性)**

如果数列 $\{a_{n}\}$ 收敛, 那么 $\{a_{n}\}$ 有界。

**定理 1.1.10 (保号性)**

如果 $\lim\limits_{n\rightarrow\infty}a_{n}=a>0$, 那么 $\forall p\in(0,a)$, $\exists N>0,$ 当 $n\ge N$ 时, 有 $a_{n}>p>0$

**推论 1.1.11**

若数列 $\{a_{n}\}$ 满足: 当 $n\ge N$ 时, $a_{n}\ge0$ 且 $\{a_{n}\}$ 收敛于a, 则 $a\ge0$。


!!! tip

    即使对所有的 $n$，都有$a_{n}>0$, 也不能得出 $a>0$。例如: 数列 $\{\frac{1}{n}\}$ 满足 $\frac{1}{n}>0$, 但其极限为零。


- **证明数列收敛或求极限**: 单调有界原理, 夹逼准则, Cauchy收敛原理


**定理 1.2.6 (单调收敛准则)**

若单调数列 $\{a_{n}\}$ 有界, 则 $\{a_{n}\}$ 必收敛。

**定理 1.1.15 (夹逼定理)**

设数列 $\{a_{n}\},\{b_{n}\},\{c_{n}\}$ 满足当 $n\ge N_{0}$ 时, 有 $b_{n}\le a_{n}\le c_{n},$ 并且 $\lim\limits_{n\rightarrow\infty}b_{n}=\lim\limits_{n\rightarrow\infty}c_{n}=a$, 则数列 $\{a_{n}\}$ 也是收敛的, 且极限为a。

**定理 1.3.5 (柯西准则)**

数列 $\{a_{n}\}$ 收敛当且仅当 $\{a_{n}\}$ 是柯西数列。

(柯西数列: $\forall\epsilon>0$, $\exists N$, 当 $m,n\ge N$ 时, $|a_{m}-a_{n}|<\epsilon$)


!!! tip

    单调递增无上界的数列一定是正无穷大，为什么？

    柯西收敛原理的否定形式也要掌握


---


## 课本例题、习题选讲

### 幂平均极限

**(4) 求极限: $\lim\limits_{n\rightarrow\infty}\sqrt[n]{1^{n}+2^{n}+\cdot\cdot\cdot+9^{n}}$**


**解**:

利用夹逼定理。

一方面，显然有：

$$9=\sqrt[n]{9^{n}}<\sqrt[n]{1^{n}+2^{n}+3^{n}+\cdot\cdot\cdot+9^{n}}$$

另一方面：

$$\sqrt[n]{1^{n}+2^{n}+\cdot\cdot\cdot+9^{n}}<\sqrt[n]{9\cdot9^{n}}=9\sqrt[n]{9}$$

综上：

$$9 < \sqrt[n]{1^{n}+2^{n}+\cdot\cdot\cdot+9^{n}} < 9\sqrt[n]{9}$$

由于 $\lim\limits_{n\rightarrow\infty}9\sqrt[n]{9} = 9 \cdot 1 = 9$。

由夹逼定理可知:

$$\lim\limits_{n\rightarrow\infty}\sqrt[n]{1^{n}+2^{n}+3^{n}+\cdot\cdot\cdot+9^{n}}=9.$$

---

### 幂平均


**定义**: 对 $a_i \ge 0, p \in R$, $a_i$ 的p次幂平均定义为:

$$ 
M_{p}(a_{i})=\left(\frac{\sum\limits_{i=1}^{n}a_{i}^{p}}{n}\right)^{\frac{1}{p}}=\left(\frac{a_{1}^{p}+a_{2}^{p}+\cdot\cdot\cdot+a_{n}^{p}}{n}\right)^{\frac{1}{p}} 
$$

- $p=1$: $M_{1}(a_{i})=\frac{a_{1}+a_{2}+\cdot\cdot\cdot+a_{n}}{n}$ (算术平均值)
- $p=-1$: $M_{-1}(a_{i})=\frac{n}{\frac{1}{a_{1}}+\frac{1}{a_{2}}+\cdot\cdot\cdot+\frac{1}{a_{n}}}$ (调和平均值)
- $p\rightarrow0$: $\lim\limits_{p\rightarrow0}M_{p}(a_{i})=\sqrt[n]{a_{1}a_{2}\cdot\cdot\cdot a_{n}}$ (几何平均值)
- $p\rightarrow+\infty$: $\lim\limits_{p\rightarrow+\infty}M_{p}(a_{i})=\max\limits\{a_{1},a_{2},\cdot\cdot\cdot,a_{n}\}$ (最大值)
- $p\rightarrow-\infty$: $\lim\limits_{p\rightarrow-\infty}M_{p}(a_{i})=\min\limits\{a_{1},a_{2},\cdot\cdot\cdot,a_{n}\}$ (最小值)


---

**16. 求极限 $\lim\limits_{n\rightarrow\infty}(1+\frac{1}{n^{2}})(1+\frac{2}{n^{2}})\cdot\cdot\cdot(1+\frac{n}{n^{2}})$**


**提示**: 利用不等式

$$\frac{x}{x+1}\le \ln(1+x)\le x$$

**答案**: $\sqrt{e}$


### 习题选讲：欧拉常数



**(5) 利用单调有界准则证明下面极限存在: $\lim\limits_{n\rightarrow\infty}(1+\frac{1}{2}+\frac{1}{3}+\cdot\cdot\cdot+\frac{1}{n}-\ln n)$**


**证明**:

令 $u_{n}=1+\frac{1}{2}+\frac{1}{3}+\cdot\cdot\cdot+\frac{1}{n}-\ln n$.

1.  **单调性**:

    $u_{n+1}-u_{n} = (\frac{1}{n+1}) - (\ln(n+1) - \ln n) = \frac{1}{n+1}-\ln(1+\frac{1}{n})$

    因为当 $x>0$ 时，$\ln(1+x) > \frac{x}{x+1}$，令 $x=\frac{1}{n}$，则 $\ln(1+\frac{1}{n}) > \frac{1/n}{1/n+1} = \frac{1}{n+1}$。


    所以 $u_{n+1}-u_{n} < 0$，数列 $\{u_n\}$ 单调递减。

2.  **有界性**:

    $u_{n} = \sum\limits_{k=1}^{n} \frac{1}{k} - \ln n > \sum\limits_{k=1}^{n} \ln(1+\frac{1}{k}) - \ln n = \sum\limits_{k=1}^{n} (\ln(k+1) - \ln k) - \ln n$

    $= (\ln 2 - \ln 1) + (\ln 3 - \ln 2) + \cdot\cdot\cdot + (\ln(n+1) - \ln n) - \ln n$

    $= \ln(n+1) - \ln n > 0$

    所以 $\{u_n\}$ 有下界。



**结论**: 数列 $\{u_n\}$ 单调递减有下界，故极限存在。 (该极限即欧拉常数 $\gamma \approx 0.5772$)

---

### p级数

**例1.3.7 证明数列 $\{1+\frac{1}{2}+\cdot\cdot\cdot+\frac{1}{n}\}$ 发散.**


**证明 (柯西准则)**:

设 $a_{n}=1+\frac{1}{2}+\cdot\cdot\cdot+\frac{1}{n}$。 

取 $m=2n$, 则

$|a_{2n}-a_{n}|=\frac{1}{n+1}+\frac{1}{n+2}+\cdot\cdot\cdot+\frac{1}{2n}$

$\ge \frac{1}{2n}+\frac{1}{2n}+\cdot\cdot\cdot+\frac{1}{2n} = n \cdot \frac{1}{2n} = \frac{1}{2}.$


由于不满足柯西收敛原理，故数列发散。


**31. 证明数列 $\{\frac{1}{1^{\alpha}}+\frac{1}{2^{\alpha}}+\frac{1}{3^{\alpha}}+\cdot\cdot\cdot+\frac{1}{n^{\alpha}}\}$ ($\alpha>1$) 收敛.**

**证明 (单调有界准则)**:

令 $a_{n}=\sum\limits_{k=1}^{n} \frac{1}{k^\alpha}$。

1.  **单调性**: $a_{n+1} - a_n = \frac{1}{(n+1)^\alpha} > 0$, 显然 $a_{n}$ 单调增加。

2.  **有界性 (柯西凝聚法)**:

    $a_n = \frac{1}{1^{\alpha}}+(\frac{1}{2^{\alpha}}+\frac{1}{3^{\alpha}})+(\frac{1}{4^{\alpha}}+\dots+\frac{1}{7^{\alpha}})+\cdot\cdot\cdot$

    $< 1+(\frac{1}{2^{\alpha}}+\frac{1}{2^{\alpha}})+(\frac{1}{4^{\alpha}}+\dots+\frac{1}{4^{\alpha}})+\cdot\cdot\cdot$

    $= 1+\frac{2}{2^{\alpha}}+\frac{4}{4^{\alpha}}+\frac{8}{8^{\alpha}}+\cdot\cdot\cdot = 1+\frac{1}{2^{\alpha-1}}+\frac{1}{4^{\alpha-1}}+\frac{1}{8^{\alpha-1}}+\cdot\cdot\cdot$

    $= \sum\limits_{k=0}^{\infty} (\frac{1}{2^{\alpha-1}})^k$

    由于 $\alpha > 1$, 公比 $\frac{1}{2^{\alpha-1}} \in (0, 1)$, 该等比级数收敛。

    其和为 $\frac{1}{1-\frac{1}{2^{\alpha-1}}}$。

    所以 $\{a_n\}$ 有上界。

**结论**: 数列 $\{a_n\}$ 单调递增有上界，故收敛。

---


### 压缩映射原理

对于递推数列 $x_{n+1}=f(x_{n})$:


**方法一: 证明与不动点的距离收缩**

若能证明极限为 $A$, 且存在 $k \in (0, 1)$ 使得:

$$|x_{n+1}-A|\le k|x_{n}-A|$$

则可推出:

$$0\le|x_{n+1}-A|\le k^{n}|x_{1}-A|$$

由于 $k^n \to 0$, 根据夹逼定理, $x_{n}\rightarrow A$。


**方法二: 证明相邻项的距离收缩**

若能证明存在 $k \in (0, 1)$ 使得:

$$|x_{n+1}-x_{n}|\le k|x_{n}-x_{n-1}|$$

则可推出:

$$|x_{n+1}-x_{n}|\le k^{n-1}|x_{2}-x_{1}|$$

由此可证明 $\{x_n\}$ 是柯西数列，因此收敛。

求出极限 $A$ 后, 解方程 $A=f(A)$ 即可。

---

**36. 设数列 $\{a_{n}\}$ 满足:对任意 $n\ge1$,有 $|a_{n+2}-a_{n+1}|\le\frac{1}{2}|a_{n+1}-a_{n}|,$ 证明 $\{a_{n}\}$ 收敛.**

**证明 (柯西准则)**:

由题意递推可得:

$$
|a_{n+1}-a_{n}|\le\frac{1}{2}|a_{n}-a_{n-1}|\le\cdot\cdot\cdot\le(\frac{1}{2})^{n-1}|a_{2}-a_{1}|
$$

对任意 $m>n$, 有:

$|a_{m}-a_{n}|=|(a_{m}-a_{m-1})+(a_{m-1}-a_{m-2})+\cdot\cdot\cdot+(a_{n+1}-a_{n})|$

$\le |a_{m}-a_{m-1}|+|a_{m-1}-a_{m-2}|+\cdot\cdot\cdot+|a_{n+1}-a_{n}|$

$\le |a_{2}-a_{1}| \left( (\frac{1}{2})^{m-2} + \cdot\cdot\cdot + (\frac{1}{2})^{n-1} \right)$

$= |a_{2}-a_{1}| \cdot \frac{(\frac{1}{2})^{n-1}(1-(\frac{1}{2})^{m-n})}{1-\frac{1}{2}} < |a_{2}-a_{1}| \cdot (\frac{1}{2})^{n-2}$

当 $n\rightarrow\infty$ 时, $(\frac{1}{2})^{n-2} \rightarrow 0$。

因此, $\forall \epsilon > 0$, 可取足够大的 $N$, 当 $m>n\ge N$ 时, $|a_m - a_n| < \epsilon$。

故 $\{a_n\}$ 是柯西列, 从而收敛。

---

**例1.2.13** 已知 $u_{1}>0, u_{n+1}=3+\frac{4}{u_{n}}$, 证明 $\{u_{n}\}$ 收敛并求极限。

**解 (压缩映射)**:

> 不动点 $A = 3 + 4/A \Rightarrow A^2-3A-4=0 \Rightarrow A=4$ 或 $A=-1$(舍)。

$|u_{n+1}-4| = |3+\frac{4}{u_{n}} - 4| = |\frac{4-u_n}{u_n}| = \frac{|u_n-4|}{u_n}$

因为 $u_n > 3$, 所以 $\frac{1}{u_n} < \frac{1}{3}$。

$|u_{n+1}-4| < \frac{1}{3}|u_{n}-4| < \cdot\cdot\cdot < (\frac{1}{3})^n |u_1 - 4|$

由夹逼定理, $\lim\limits_{n\rightarrow\infty}|u_{n+1}-4|=0$, 故 $\lim\limits_{n\rightarrow\infty}u_{n}=4$

---

**26.** 设 $u_{1}=2, u_{n+1}=\frac{u_{n}(u_{n}^{2}+3)}{3u_{n}^{2}+1}$, 证明 $\{u_{n}\}$ 收敛并求极限。

**解 (单调有界)**:

> 不动点 $a = \frac{a(a^2+3)}{3a^2+1} \Rightarrow a=0, 1, -1$。

1.  **有界性**: 证明 $u_n > 1$。

    $u_{n+1}-1=\frac{u_{n}^{3}+3u_{k}-3u_{n}^{2}-1}{3u_{n}^{2}+1}=\frac{(u_{n}-1)^{3}}{3u_{n}^{2}+1}$

    $u_1=2>1$, 若 $u_n>1$, 则 $u_{n+1}-1 > 0$, 故 $u_{n+1}>1$。

    由归纳法得 $u_n > 1$。

2.  **单调性**:

    $\frac{u_{n+1}}{u_{n}}=\frac{u_{n}^{2}+3}{3u_{n}^{2}+1} = \frac{3u_n^2+1 - 2u_n^2+2}{3u_n^2+1} = 1-\frac{2(u_n^2-1)}{3u_n^2+1}$

    因为 $u_n>1$, 所以 $u_n^2-1>0$, 故 $\frac{u_{n+1}}{u_{n}} < 1$, 即 $u_{n+1} < u_n$。

$\{u_n\}$ 单调递减有下界1, 故收敛。设极限为 $b$, 解得 $b=1$。



---

### Stolz公式与柯西命题


**Stolz 公式 ($\frac{\infty}{\infty}$ 型)**

若 $\{y_{n}\}$ 严格单调趋于 $+\infty$, 且 $\lim\limits_{n\rightarrow\infty}\frac{x_{n}-x_{n-1}}{y_{n}-y_{n-1}}=A$,

则 $\lim\limits_{n\rightarrow\infty}\frac{x_{n}}{y_{n}}=A$。

**Stolz公式的推论 (柯西命题)**

-   **算术平均形式**: 若 $\lim\limits_{n\rightarrow\infty}x_{n} = A$, 则 $\lim\limits_{n\rightarrow\infty}\frac{\sum\limits_{k=1}^n x_k}{n}=A$。

-   **几何平均形式**: 若 $x_n > 0$ 且 $\lim\limits_{n\rightarrow\infty}x_{n} = A$, 则 $\lim\limits_{n\rightarrow\infty}\sqrt[n]{x_{1}x_{2}\cdot\cdot\cdot x_{n}}=A$。

---

**求极限 $\lim\limits_{n\rightarrow\infty}\frac{1+\frac{1}{2}+\cdot\cdot\cdot+\frac{1}{n}}{\ln n}$**

**解**:

$\lim\limits_{n\rightarrow\infty}\frac{\sum\limits_{k=1}^n \frac{1}{k}}{\ln n} \xlongequal{Stolz} \lim\limits_{n\rightarrow\infty}\frac{\frac{1}{n}}{\ln n-\ln(n-1)}$

$=\lim\limits_{n\rightarrow\infty}\frac{\frac{1}{n}}{-\ln(1-\frac{1}{n})} = \lim\limits_{n\rightarrow\infty}\frac{\frac{1}{n}}{\frac{1}{n}} = 1$

---

**求 $\lim\limits_{n\rightarrow\infty}\frac{n}{\sqrt[n]{n!}}$**

**解**:

令 $x_n = \frac{n^n}{n!}$。考虑 $\lim\limits_{n\rightarrow\infty} \frac{x_{n+1}}{x_n}$。

$\lim\limits_{n\rightarrow\infty}\frac{(n+1)^{n+1}/(n+1)!}{n^n/n!} = \lim\limits_{n\rightarrow\infty}\frac{(n+1)^{n+1}}{n^n(n+1)} = \lim\limits_{n\rightarrow\infty}(\frac{n+1}{n})^n = e$<br>

由柯西命题的几何平均形式的推论:<br>

$\lim\limits_{n\rightarrow\infty}\sqrt[n]{\frac{n^n}{n!}} = \lim\limits_{n\rightarrow\infty}\frac{n}{\sqrt[n]{n!}} = e$

---

**设 $x_{1}\in(0,1),x_{n+1}=x_{n}(1-x_{n})$, 证明 $\lim\limits_{n\rightarrow\infty}nx_{n}=1$**

首先证明 $x_n \to 0$。 $x_{n+1}-x_n = -x_n^2 < 0$, 数列单调递减。$x_n \in (0,1)$ 有下界0, 故收敛。设极限为 $a$, 则 $a=a(1-a) \Rightarrow a=0$。

考虑 $\lim\limits_{n\rightarrow\infty}nx_{n} = \lim\limits_{n\rightarrow\infty}\frac{n}{\frac{1}{x_{n}}}$。应用Stolz公式。<br>

  $\lim\limits_{n\rightarrow\infty}\frac{n+1-n}{\frac{1}{x_{n+1}}-\frac{1}{x_{n}}} = \lim\limits_{n\rightarrow\infty}\frac{x_{n+1}x_n}{x_{n}-x_{n+1}}$

$=\lim\limits_{n\rightarrow\infty}\frac{x_{n+1}x_n}{x_{n}^2}$

$=\lim\limits_{n\rightarrow\infty}\frac{x_{n+1}}{x_{n}} = \lim\limits_{n\rightarrow\infty}\frac{x_n(1-x_n)}{x_{n}}$

$=\lim\limits_{n\rightarrow\infty}(1-x_{n})$<br>

因为 $x_{n} \to 0$, 所以极限为 1。

---

### 杂题: 卷积型极限

**若 $\lim\limits_{n\rightarrow\infty}a_{n}=a, \lim\limits_{n\rightarrow\infty}b_{n}=b,$ 求证 $\lim\limits_{n\rightarrow\infty}\frac{a_{1}b_{n}+a_{2}b_{n-1}+\cdot\cdot\cdot+a_{n}b_{1}}{n}=ab$**

**证明 (松弛变量法)**:

令 $b_n = b + c_n$, 则 $\lim\limits_{n\rightarrow\infty} c_n = 0$。

原式 $= \lim\limits_{n\rightarrow\infty}\frac{\sum\limits_{k=1}^n a_k b_{n-k+1}}{n} = \lim\limits_{n\rightarrow\infty}\frac{\sum\limits_{k=1}^n a_k (b+c_{n-k+1})}{n}$

$= \lim\limits_{n\rightarrow\infty} \left( \frac{\sum\limits_{k=1}^n a_k b}{n} + \frac{\sum\limits_{k=1}^n a_k c_{n-k+1}}{n} \right)$<br>

第一部分: $\lim\limits_{n\rightarrow\infty} b \cdot \frac{\sum\limits_{k=1}^n a_k}{n} = b \cdot a = ab$ (由柯西命题)。<br>

第二部分: 需证 $\lim\limits_{n\rightarrow\infty} \frac{\sum\limits_{k=1}^n a_k c_{n-k+1}}{n} = 0$。

因为 $\{a_n\}$ 收敛, 所以有界, $\exists M>0, |a_n| \le M$。因为 $c_n \to 0$, $\forall \epsilon > 0$, $\exists N$, 当 $k > N$ 时, $|c_k| < \epsilon$。

可以证明第二部分极限为0。

所以原极限为 $ab$。

---

### 杂题: 加权平均极限

**设 $\lim\limits_{n\rightarrow\infty}x_{n}=a$, 求证 $\lim\limits_{n\rightarrow\infty}\frac{x_{1}+2x_{2}+\cdot\cdot\cdot+nx_{n}}{n^{2}}=\frac{a}{2}$**

**证明 (拆分数列法)**:

令 $x_n = a + \alpha_n$, 则 $\lim\limits_{n\rightarrow\infty} \alpha_n = 0$。

原式 $= \lim\limits_{n\rightarrow\infty} \frac{\sum\limits_{k=1}^n k x_k}{n^2} = \lim\limits_{n\rightarrow\infty} \frac{\sum\limits_{k=1}^n k(a+\alpha_k)}{n^2}$

$= \lim\limits_{n\rightarrow\infty} \left( \frac{\sum\limits_{k=1}^n ka}{n^2} + \frac{\sum\limits_{k=1}^n k\alpha_k}{n^2} \right)$<br>

第一部分: $\lim\limits_{n\rightarrow\infty} \frac{a \cdot \frac{n(n+1)}{2}}{n^2} = \lim\limits_{n\rightarrow\infty} a \cdot \frac{n+1}{2n} = \frac{a}{2}$。<br>

第二部分: $\lim\limits_{n\rightarrow\infty} \frac{\sum\limits_{k=1}^n k\alpha_k}{n^2}$。应用Stolz公式。

$\lim\limits_{n\rightarrow\infty} \frac{n \alpha_n}{n^2 - (n-1)^2} = \lim\limits_{n\rightarrow\infty} \frac{n \alpha_n}{2n-1} = \lim\limits_{n\rightarrow\infty} \frac{n}{2n-1} \cdot \alpha_n = \frac{1}{2} \cdot 0 = 0$。

所以原极限为 $\frac{a}{2} + 0 = \frac{a}{2}$。

---

### 估阶



**设 $a_{1}=1$, $a_{n+1}=a_{n}+\frac{1}{a_{n}}$.**

**(1) 求证 $\lim\limits_{n\rightarrow\infty}\frac{a_{n}}{\sqrt{n}}=\sqrt{2}$** &nbsp;&nbsp;

**(2) 求 $\lim\limits_{n\rightarrow\infty}\frac{\sqrt{n}(a_{n}-\sqrt{2n})}{\ln n}$**



(1)

$a_{n+1}-a_n = \frac{1}{a_n} > 0$, 故 $\{a_n\}$ 单调递增。<br>

若有上界则必收敛，设极限为$C$, 则 $C = C+\frac{1}{C}$, 矛盾。故 $a_n \to +\infty$。

考虑 $a_{n+1}^{2}-a_{n}^{2} = (a_n+\frac{1}{a_n})^2 - a_n^2 = 2+\frac{1}{a_{n}^{2}}$。

$\lim\limits_{n\rightarrow\infty} (a_{n+1}^{2}-a_{n}^{2}) = 2 + 0 = 2$。<br>

$\lim\limits_{n\rightarrow\infty}\frac{a_{n}^{2}}{n} \xlongequal{Stolz} \lim\limits_{n\rightarrow\infty}\frac{a_{n}^{2}-a_{n-1}^{2}}{n-(n-1)} = \lim\limits_{n\rightarrow\infty}(2+\frac{1}{a_{n-1}^{2}}) = 2$&nbsp;

所以 $\lim\limits_{n\rightarrow\infty}\frac{a_{n}}{\sqrt{n}}=\sqrt{2}$。

(2)

$a_n^2 - 2n = (a_n^2 - a_{n-1}^2-2) + \cdot\cdot\cdot + (a_2^2-a_1^2-2) + (a_1^2-2) = \sum\limits_{k=1}^{n-1} \frac{1}{a_k^2} - 1$.<br>

原极限 $\xlongequal{分子有理化} \lim\limits_{n\rightarrow\infty}\frac{\sqrt{n}(a_{n}^2-2n)}{(a_{n}+\sqrt{2n})\ln n} = \lim\limits_{n\rightarrow\infty}\frac{\sqrt{n}(\sum\limits_{k=1}^{n-1}\frac{1}{a_k^2}-1)}{(a_{n}+\sqrt{2n})\ln n}$

由于 $a_n \sim \sqrt{2n}$, $a_n+\sqrt{2n} \sim 2\sqrt{2n}$。<br>

原极限 $=  \lim\limits_{n\rightarrow\infty}\frac{\sum\limits_{k=1}^{n-1}\frac{1}{a_k^2}-1}{2\sqrt{2} \ln n} \xlongequal{Stolz} \lim\limits_{n\rightarrow\infty} \frac{1}{2\sqrt{2}}\frac{\frac{1}{a_{n}^2}}{\ln(n+1)-\ln n} = \frac{1}{4\sqrt{2}}$。
