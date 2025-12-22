# 极限计算2：泰勒公式与洛必达法则

## 1. 带皮亚诺 (Peano) 余项的泰勒公式

泰勒公式是分析学中将复杂函数近似为多项式的核心工具。在极限计算中，我们主要关注 **在 $x_0 = 0$ 处展开** 的麦克劳林公式。

### 1.1 定理内容

!!! abstract 带peano余项的泰勒公式
    设函数 $f(x)$ 在点 $x_0$ 处存在 $n$ 阶导数，则 $f(x)$ 在 $x_0$ 的邻域内可表示为：
    
    $$ f(x) = f(x_0) + f'(x_0)(x-x_0) + \frac{f''(x_0)}{2!}(x-x_0)^2 + \cdots + \frac{f^{(n)}(x_0)}{n!}(x-x_0)^n + o((x-x_0)^n) $$
    
    其中 $o((x-x_0)^n)$ 称为 **皮亚诺余项**，表示比 $(x-x_0)^n$ 高阶的无穷小量，即：
    
    $$ \lim_{x \to x_0} \frac{o((x-x_0)^n)}{(x-x_0)^n} = 0 $$

在极限计算中，我们通常取 $x_0 = 0$（麦克劳林展开）：

$$ f(x) = \sum_{k=0}^{n} \frac{f^{(k)}(0)}{k!} x^k + o(x^n) $$

### 1.2 常用函数的展开式 (需熟记)

当 $x \to 0$ 时：

| 函数 $f(x)$ | 展开式 (麦克劳林公式) |
| :--- | :--- |
| **$e^x$** | $1 + x + \dfrac{x^2}{2!} + \dfrac{x^3}{3!} + \cdots + \dfrac{x^n}{n!} + o(x^n)$ |
| **$\sin x$** | $x - \dfrac{x^3}{3!} + \dfrac{x^5}{5!} - \cdots + (-1)^{m-1}\dfrac{x^{2m-1}}{(2m-1)!} + o(x^{2m})$ |
| **$\cos x$** | $1 - \dfrac{x^2}{2!} + \dfrac{x^4}{4!} - \cdots + (-1)^m\dfrac{x^{2m}}{(2m)!} + o(x^{2m+1})$ |
| **$\ln(1+x)$** | $x - \dfrac{x^2}{2} + \dfrac{x^3}{3} - \cdots + (-1)^{n-1}\dfrac{x^n}{n} + o(x^n)$ |
| **$(1+x)^\alpha$** | $1 + \alpha x + \dfrac{\alpha(\alpha-1)}{2!}x^2 + \cdots + \dfrac{\alpha(\alpha-1)\cdots(\alpha-n+1)}{n!}x^n + o(x^n)$ |

!!! tip 
    *   **$(1+x)^\alpha$** 当 $\alpha=-1$ 时变为几何级数：$\dfrac{1}{1+x} = 1 - x + x^2 - x^3 + \cdots$

### 1.3 高阶无穷小 $o(x^n)$ 的运算规则


1.  $x^m \cdot o(x^n) = o(x^{m+n})$
2.  $o(x^n) \pm o(x^n) = o(x^n)$
3.  $o(x^m) + o(x^n) = o(x^{\min(m,n)})$ （低阶“吃掉”高阶）
4.  $c \cdot o(x^n) = o(x^n)$ ($c \neq 0$)

---

## 2. 洛必达法则 (L'Hôpital's Rule)

洛必达法则是通过导数来确定未定式极限的方法。

### 2.1 适用条件

!!! warning 使用条件
    1.  极限类型必须是 **$\dfrac{0}{0}$** 型或 **$\dfrac{\infty}{\infty}$** 型。
    2.  分子分母在去心邻域内可导，且分母导数不为 0。
    3.  $\lim\limits_{x\to x_0} \dfrac{f'(x)}{g'(x)}$ **存在** (或为无穷大)。

    若导数之比的极限不存在（且不是无穷大），不能说明原极限不存在，只能说明洛必达法则失效。

### 2.2 法则内容

若满足上述条件，则：

$$ \lim_{x \to x_0} \frac{f(x)}{g(x)} = \lim_{x \to x_0} \frac{f'(x)}{g'(x)} $$

### 2.3 其他未定式的转化

对于非 $\frac{0}{0}$ 或 $\frac{\infty}{\infty}$ 的形式，需先变形：

*   **$0 \cdot \infty$ 型**：$f \cdot g = \dfrac{f}{1/g}$ 或 $\dfrac{g}{1/f}$。
*   **$\infty - \infty$ 型**：通分（若是分式）或 提取公因式/有理化/倒代换。
*   **$1^\infty, 0^0, \infty^0$ 型**：利用恒等式 $u^v = e^{v \ln u}$，转化为指数上的 $0 \cdot \infty$ 极限。


---

## 4. 例题解析

**题目1**：计算 $\lim\limits_{x \to 0} \dfrac{\sin x - x \cos x}{x^3}$

!!! success 解
    **分析**：分母是 $x^3$，提示我们需要将分子展开到 $x^3$ 项。

    $$
    \begin{aligned}
    \sin x &= x - \frac{x^3}{6} + o(x^3) \\
    x \cos x &= x \left( 1 - \frac{x^2}{2} + o(x^2) \right) = x - \frac{x^3}{2} + o(x^3)
    \end{aligned}
    $$

    代入原式：

    $$
    \begin{aligned}
    \text{原式} &= \lim_{x \to 0} \dfrac{\left(x - \frac{x^3}{6} + o(x^3)\right) - \left(x - \frac{x^3}{2} + o(x^3)\right)}{x^3} \\
    &= \lim_{x \to 0} \dfrac{\left(-\frac{1}{6} + \frac{1}{2}\right)x^3 + o(x^3)}{x^3} \\
    &= \frac{1}{3}
    \end{aligned}
    $$


**题目2**：计算 $\lim\limits_{x \to 0} \left( \dfrac{\sin x}{x} \right)^{\frac{1}{x^2}}$

!!! success 解
    这是一个 $1^\infty$ 型极限
    
    需要计算极限 $L = \lim\limits_{x \to 0} \frac{1}{x^2} \left( \dfrac{\sin x}{x} - 1 \right) = \lim\limits_{x \to 0} \dfrac{\sin x - x}{x^3}$。

    此处遇到 $\frac{\sin x - x}{x^3}$，是典型的泰勒公式适用场景。

    $$
    \sin x = x - \frac{x^3}{6} + o(x^3)
    $$

    $$
    L = \lim_{x \to 0} \dfrac{(x - \frac{x^3}{6} + o(x^3)) - x}{x^3} = \lim_{x \to 0} \dfrac{-\frac{x^3}{6}}{x^3} = -\frac{1}{6}
    $$

    故原极限为 $e^{-1/6}$。



**题目3**：求函数 $f(x) = \tan x$ 在 $x=0$ 处的泰勒展开式（麦克劳林公式），精确到 $x^5$ 项。

!!! success 不太严谨的多项式除法

    不太严谨的多项式除法

    我们知道 $\sin x$ 和 $\cos x$ 的麦克劳林展开式为：
    
    $$
    \begin{aligned}
    \sin x &= x - \frac{x^3}{3!} + \frac{x^5}{5!} - \cdots = x - \frac{1}{6}x^3 + \frac{1}{120}x^5 - o(x^5) \\
    \cos x &= 1 - \frac{x^2}{2!} + \frac{x^4}{4!} - \cdots = 1 - \frac{1}{2}x^2 + \frac{1}{24}x^4 - o(x^4)
    \end{aligned}
    $$
    
    由 $\tan x = \dfrac{\sin x}{\cos x}$，我们可以列出长除法算式：
    
    $$ \dfrac{x - \frac{1}{6}x^3 + \frac{1}{120}x^5 - \cdots}{1 - \frac{1}{2}x^2 + \frac{1}{24}x^4 - \cdots} $$

    **步骤 1：确定 $x$ 一次项**
    
    $$ \text{商} = x $$

    $$ x(1 - \frac{1}{2}x^2 + \frac{1}{24}x^4) = x - \frac{1}{2}x^3 + \frac{1}{24}x^5 $$

    $$ \text{余式 1} = (x - \frac{1}{6}x^3 + \frac{1}{120}x^5) - (x - \frac{1}{2}x^3 + \frac{1}{24}x^5) = \frac{1}{3}x^3 - \frac{1}{30}x^5 $$

    **步骤 2：确定 $x$ 三次项**
    用余式 1 的首项 $\frac{1}{3}x^3$ 除以分母首项 $1$，得商 $\frac{1}{3}x^3$。
    
    $$ \text{商} = \frac{1}{3}x^3 $$

    $$ \frac{1}{3}x^3(1 - \frac{1}{2}x^2) = \frac{1}{3}x^3 - \frac{1}{6}x^5 $$

    $$ \text{余式 2} = (\frac{1}{3}x^3 - \frac{1}{30}x^5) - (\frac{1}{3}x^3 - \frac{1}{6}x^5) = (-\frac{1}{30} + \frac{5}{30})x^5 = \frac{2}{15}x^5 $$

    **步骤 3：确定 $x$ 五次项**

    用余式 2 的首项 $\frac{2}{15}x^5$ 除以分母首项 $1$，得商 $\frac{2}{15}x^5$。

    **结论：**
    $$ \tan x = x + \frac{1}{3}x^3 + \frac{2}{15}x^5 + o(x^5) $$

---

**题4：推导 $\arctan x$ 的麦克劳林公式**

!!! success 按照定义计算各阶导数

    已知$f'(x)(1+x^2) = 1$，根据莱布尼兹法则计算导数

    过程略

    



!!! success 级数方法

    级数方法（仅供参考记忆）

    **第一步：导数展开**
    
    已知 $(\arctan x)' = \dfrac{1}{1+x^2}$。
    
    利用等比级数公式 $\dfrac{1}{1-u} = 1 + u + u^2 + u^3 + \cdots$ (当 $|u| < 1$)。
    令 $u = -x^2$，则有：
    
    $$
    \begin{aligned}
    \frac{1}{1+x^2} &= \frac{1}{1-(-x^2)} \\
    &= 1 + (-x^2) + (-x^2)^2 + (-x^2)^3 + \cdots + (-x^2)^n + \cdots \\
    &= 1 - x^2 + x^4 - x^6 + \cdots + (-1)^n x^{2n} + \cdots
    \end{aligned}
    $$
    
    此式成立条件为 $|-x^2| < 1$，即 $|x| < 1$。

    **第二步：逐项积分**
    
    由于 $f(0) = \arctan 0 = 0$，我们可以对上式从 $0$ 到 $x$ 进行定积分（即变上限积分）：
    
    $$
    \begin{aligned}
    \arctan x &= \int_0^x \dfrac{1}{1+t^2} \mathrm{d}t \\
    &= \int_0^x \left( 1 - t^2 + t^4 - t^6 + \cdots + (-1)^n t^{2n} + \cdots \right) \mathrm{d}t \\
    &= \left[ t - \frac{t^3}{3} + \frac{t^5}{5} - \frac{t^7}{7} + \cdots + (-1)^n \frac{t^{2n+1}}{2n+1} \right]_0^x
    \end{aligned}
    $$
    
    **所以**
    
    $$ \arctan x = x - \frac{x^3}{3} + \frac{x^5}{5} - \frac{x^7}{7} + \cdots + (-1)^n \frac{x^{2n+1}}{2n+1} + o(x^{2n+1}) $$


---


**题目5**：求函数 $f(x) = (1+x)^{\frac{1}{x}}$ 在 $x=0$ 处的带有 Peano 余项的泰勒展开式（展开到 $x^2$ 项）。


!!! success 解

    **第一步：指数变形**
    
    $$ f(x) = (1+x)^{\frac{1}{x}} = e^{\frac{1}{x} \ln(1+x)} $$

    **第二步：处理指数部分**
    
    我们需要将 $f(x)$ 展开到 $x^2$，这意味着 $e^u$ 中的 $u$ 需要精确到 $x^2$。
    由于指数前方有一个 $\frac{1}{x}$，这意味着 $\ln(1+x)$ 需要展开到 $x^3$ (这样除以 $x$ 后才能剩 $x^2$)。

    $$
    \begin{aligned}
    \ln(1+x) &= x - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3) \\
    \text{指数} = \frac{1}{x} \ln(1+x) &= \frac{1}{x} \left( x - \frac{x^2}{2} + \frac{x^3}{3} + o(x^3) \right) \\
    &= 1 - \frac{x}{2} + \frac{x^2}{3} + o(x^2)
    \end{aligned}
    $$

    **第三步：代回原式并分离常数**
    
    $$
    \begin{aligned}
    f(x) &= e^{1 - \frac{x}{2} + \frac{x^2}{3} + o(x^2)} \\
    &= e^1 \cdot e^{-\frac{x}{2} + \frac{x^2}{3} + o(x^2)}
    \end{aligned}
    $$
    
    令 $u = -\frac{x}{2} + \frac{x^2}{3}$。当 $x \to 0$ 时，$u \to 0$，符合 $e^u$ 展开条件。

    **第四步：复合展开**
    
    利用 $e^u = 1 + u + \frac{u^2}{2} + o(u^2)$：

    1.  **计算 $u$**：
        
        $$ u = -\frac{1}{2}x + \frac{1}{3}x^2 $$
        *(注：这里忽略 $o(x^2)$ 以简化书写，最后加上即可)*

    2.  **计算 $u^2$**：
        我们需要保留到 $x^2$ 项，因此展开平方时，$x^3$ 及更高次项直接扔进 $o(x^2)$。
        
        $$ u^2 = \left( -\frac{1}{2}x + \frac{1}{3}x^2 \right)^2 = \frac{1}{4}x^2 + \underbrace{2(-\frac{1}{2}x)(\frac{1}{3}x^2) + \dots}_{o(x^2)} = \frac{1}{4}x^2 + o(x^2) $$

    3.  **代入公式**：
        
        $$
        \begin{aligned}
        e^u &= 1 + \left( -\frac{1}{2}x + \frac{1}{3}x^2 \right) + \frac{1}{2} \left( \frac{1}{4}x^2 \right) + o(x^2) \\
        &= 1 - \frac{1}{2}x + \left( \frac{1}{3} + \frac{1}{8} \right)x^2 + o(x^2) \\
        &= 1 - \frac{1}{2}x + \frac{11}{24}x^2 + o(x^2)
        \end{aligned}
        $$

    **第五步：最终结果**
    
    不要忘记最前面的系数 $e$。
    
    $$
    f(x) = e \left( 1 - \frac{1}{2}x + \frac{11}{24}x^2 + o(x^2) \right)
    $$
    
    即：
    
    $$ (1+x)^{\frac{1}{x}} = e - \frac{e}{2}x + \frac{11e}{24}x^2 + o(x^2) $$


!!! Tip
    利用上述展开式，可以求解如下极限题：
    
    $$ \lim_{x \to 0} \frac{(1+x)^{\frac{1}{x}} - e}{x} $$

    **解**：

    $$
    \begin{aligned}
    \text{原式} &= \lim_{x \to 0} \frac{\left( e - \frac{e}{2}x + o(x) \right) - e}{x} \\
    &= \lim_{x \to 0} \frac{-\frac{e}{2}x}{x} = -\frac{e}{2}
    \end{aligned}
    $$

---

## 5.洛必达法则的“失效”情形

洛必达法则的核心结论是：若 $\lim \dfrac{f'(x)}{g'(x)} = A$ (或 $\infty$)，则 $\lim \dfrac{f(x)}{g(x)} = A$。

然而，**逆命题不成立**。即：如果 $\lim \dfrac{f'(x)}{g'(x)}$ **不存在** (且不是无穷大)，**不能** 说明原极限不存在，仅仅说明 **洛必达法则在此处失效**，需要改用夹逼准则、泰勒公式或代数变形求解。

以下是三种典型的失效或不适用场景：

### 5.1. 导数极限震荡不存在

**例题**

计算 $\displaystyle\lim_{x \to +\infty} \dfrac{x + \sin x}{x}$

!!! failure
    这是一个 $\frac{\infty}{\infty}$ 型未定式。尝试使用洛必达法则：
    
    $$ \lim_{x \to +\infty} \dfrac{(x + \sin x)'}{(x)'} = \lim_{x \to +\infty} \dfrac{1 + \cos x}{1} $$
    
    由于 $x \to +\infty$ 时，$\cos x$ 在 $[-1, 1]$ 之间无限震荡，故上述极限 **不存在**。
    

!!! success
    虽然导数比值的极限不存在，但原极限其实很容易计算：
    
    $$ \lim_{x \to +\infty} \dfrac{x + \sin x}{x} = \lim_{x \to +\infty} \left( 1 + \dfrac{\sin x}{x} \right) = 1 $$

---

### 5.2. 循环失效


**例题**：计算 $\displaystyle\lim_{x \to +\infty} \dfrac{\sqrt{x^2+1}}{x}$

!!! failure
    这是 $\frac{\infty}{\infty}$ 型。尝试洛必达：
    
    $$
    \begin{aligned}
    L &= \lim_{x \to +\infty} \dfrac{\frac{1}{2\sqrt{x^2+1}} \cdot 2x}{1} = \lim_{x \to +\infty} \dfrac{x}{\sqrt{x^2+1}} \\
    \text{再洛必达} &= \lim_{x \to +\infty} \dfrac{1}{\frac{2x}{2\sqrt{x^2+1}}} = \lim_{x \to +\infty} \dfrac{\sqrt{x^2+1}}{x}
    \end{aligned}
    $$
    
    **结果**：转了一圈又回到了原题目。继续求导只会无限循环。

!!! success
    直接进行代数变形：
    
    $$ \lim_{x \to +\infty} \dfrac{\sqrt{x^2(1+\frac{1}{x^2})}}{x} = \lim_{x \to +\infty} \dfrac{x\sqrt{1+\frac{1}{x^2}}}{x} = \lim_{x \to +\infty} \sqrt{1+\frac{1}{x^2}} = 1 $$
