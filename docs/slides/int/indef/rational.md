# 不定积分1

## 有理函数积分
### 通用解法
**核心策略**

- 遇到有理函数积分，一般采用**裂项 + 待定系数法**，不过对于特定有理函数可能存在更便捷方法，但仍需以掌握基本方法为主。
- 先将有理函数划分为真分式与假分式，假分式可通过多项式除法转化为多项式与真分式之和，所以解决有理函数积分关键在于处理有理真分式积分。

**真分式积分步骤详解**

- **步骤一：分母因式分解**：将真分式分母彻底分解，直至无法继续分解。
- **步骤二：裂项规则**
    + 若分母含有\((x - a)^{k}\)，则裂项后的式子必定包含\(\dfrac{A_{1}}{x - a}+\dfrac{A_{2}}{(x - a)^{2}}+\cdots+\dfrac{A_{k}}{(x - a)^{k}}\)。
    + 若分母含有\((x^{2}+px + q)^{k}\)（需满足\(p^{2}-4q\lt0\)），则裂项后的式子必定包含\(\dfrac{B_{1}x + C_{1}}{(x^{2}+px + q)^{1}}+\dfrac{B_{2}x + C_{2}}{(x^{2}+px + q)^{2}}+\cdots+\dfrac{B_{k}x + C_{k}}{(x^{2}+px + q)^{k}}\)。
- **步骤三：确定待定系数**：对裂项后的式子通分，依据“通分后的分子与原被积函数的分子对应系数相等”原则，列出待定系数满足的方程，进而求解待定系数，从而将真分式分解为各个基本分式之和。
- **步骤四：计算基本分式积分**
  - 对于\(\displaystyle\int\dfrac{A}{(x - a)^{k}}\mathrm{d}x\)这类基本分式积分相对容易。
  - 对于\(\displaystyle\int\dfrac{Bx + C}{x^{2}+px + q}\mathrm{d}x\)和\(\displaystyle\int\dfrac{Bx + C}{(x^{2}+px + q)^{2}}\mathrm{d}x\)，其计算有通用方法，尤其在期末、考研范围内，分母次数通常为 1 或 2，后续例题将详细介绍其计算方法。

#### 例题解析

**例题 1**：

$$
  \int\dfrac{x + 3}{x^{2}+2x + 4}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\frac{1}{2}(2x+2)+2}{x^2+2x+4}\mathrm{d}x = \dfrac{1}{2}\ln|x^2+2x+4| + 2\int\dfrac{1}{(x+1)^2+(\sqrt{3})^2}\mathrm{d}x \\
&= \dfrac{1}{2}\ln|x^2+2x+4| + \dfrac{2}{\sqrt{3}}\arctan\dfrac{x+1}{\sqrt{3}} + C
\end{aligned}
$$

!!! Note
    通过该例题可总结出\(\int\dfrac{Bx + C}{x^{2}+px + q}\mathrm{d}x\)的积分套路为**改造分子，拆分为两个积分，其中第一个积分直接凑微分，第二个积分配方后套公式**

**例题 2**：

$$
\int\dfrac{x^{2}}{(a^{2}+x^{2})^{2}}\mathrm{d}x
$$



!!! Tip
    提示可尝试三角换元$x = a\tan t$
    
    同时也可考虑分部积分法降低分母次数。

    $$
    \int\dfrac{x^{2}}{(a^{2}+x^{2})^{2}}\mathrm{d}x = \int x\cdot\dfrac{x}{(a^{2}+x^{2})^{2}}\mathrm{d}x = \dfrac{1}{2}\int x\dfrac{\mathrm{d}(x^2+a^2)}{x^2+a^2}
    $$

**解：**

$$
I = -\dfrac{1}{2}\int x\mathrm{d}\left( \dfrac{1}{x^2+a^2} \right) = -\dfrac{x}{2(x^2+a^2)} + \dfrac{1}{2}\int\dfrac{1}{x^2+a^2}\mathrm{d}x = -\dfrac{x}{2(x^2+a^2)} + \dfrac{1}{2a}\arctan\dfrac{x}{a} + C
$$

!!! Note

    **类题**：

    $$
    \int\dfrac{1}{(a^{2}+x^{2})^{2}}\mathrm{d}x
    $$
    
    **解：** 使用三角换元，令 \(x=a\tan t\)，则 \(\mathrm{d}x=a\sec^2 t \mathrm{d}t\)

    $$
    \begin{aligned}
    I &= \int \dfrac{1}{a^4 \sec^4 t} \cdot a \sec^2 t \mathrm{d}t = \dfrac{1}{a^3} \int \cos^2 t \mathrm{d}t = \dfrac{1}{2a^3} \int (\cos 2t + 1) \mathrm{d}t = \dfrac{1}{4a^3}\sin 2t + \dfrac{t}{2a^3} + C \\
    &= \dfrac{x}{2a^2(x^2+a^2)} + \dfrac{1}{2a^3}\arctan\dfrac{x}{a} + C
    \end{aligned}
    $$

    *注：换元后一定要回代！*

    借助例题 2 及该类题，能够推导出\(\displaystyle\int\dfrac{Bx + C}{(x^{2}+px + q)^{2}}\mathrm{d}x\)的计算方法，例如计算\(\displaystyle\int\dfrac{x + 2}{(x^{2}+2x + 10)^{2}}\mathrm{d}x\)，其方法可总结为**改造分子、拆分为两个积分，对分母配方、换元，归结于计算\(\displaystyle\int\dfrac{1}{(a^{2}+t^{2})^{2}}\mathrm{d}t\)**
    
    思考：\(\displaystyle\int\dfrac{x^{2}}{(x^{2}+px + q)^{2}}\mathrm{d}x\)的计算方式。


!!! Exercise
    $$
    \int\dfrac{x+2}{(x^{2}+2x + 10)^{2}}\mathrm{d}x
    $$


**例题 3**

$$
\int\dfrac{3x + 6}{(x - 1)^{2}(x^{2}+x + 1)}\mathrm{d}x
$$

**解：**

设 \(\dfrac{3x+6}{(x-1)^2(x^2+x+1)} = \dfrac{A}{x-1} + \dfrac{B}{(x-1)^2} + \dfrac{Cx+D}{x^2+x+1}\)

通分可得：

\(3x+6 = A(x-1)(x^2+x+1) + B(x^2+x+1) + (Cx+D)(x-1)^2\)
可得方程组：

\(\begin{cases} A+C=0 \\ 3B=9 (x=1\text{代入}) \\ B-2C+D=0 \\ -A+B+D=6 (x=0\text{代入}) \end{cases}\)
解得 \(A=-2, B=3, C=2, D=1\)

$$
\begin{aligned}
I &= \int \left( -\dfrac{2}{x-1} + \dfrac{3}{(x-1)^2} + \dfrac{2x+1}{x^2+x+1} \right) \mathrm{d}x \\
&= -2\ln|x-1| - \dfrac{3}{x-1} + \ln|x^2+x+1| + C
\end{aligned}
$$

**例题 4**

$$  
  \int\dfrac{1}{1 + x^{3}}\mathrm{d}x
$$

**解：**

\(\dfrac{1}{x^3+1} = \dfrac{A}{x+1} + \dfrac{Bx+C}{x^2-x+1}\)

可得 \(1 = A(x^2-x+1) + (Bx+C)(x+1)\)

解得 \(A=\dfrac{1}{3}, B=-\dfrac{1}{3}, C=\dfrac{2}{3}\)

$$
\begin{aligned}
I &= \int \left( \dfrac{1}{3}\cdot\dfrac{1}{x+1} + \dfrac{-\frac{1}{3}x+\frac{2}{3}}{x^2-x+1} \right) \mathrm{d}x \\
&= \dfrac{1}{3}\ln|x+1| - \dfrac{1}{6}\ln|x^2-x+1| + \dfrac{1}{2}\int \dfrac{1}{(x-\frac{1}{2})^2+\frac{3}{4}}\mathrm{d}x \\
&= \dfrac{1}{3}\ln|x+1| - \dfrac{1}{6}\ln|x^2-x+1| + \dfrac{1}{\sqrt{3}}\arctan\left( \dfrac{2x-1}{\sqrt{3}} \right) + C
\end{aligned}
$$


### 有理函数积分特殊解法

从理论上讲，所有有理函数积分均可运用上述待定系数法求解，但此通法未必是最优选择，其工作量往往较大。实际上，许多有理函数积分具备独特解法，需仔细剖析被积函数结构，具体问题具体分析。学习数学是一个积累过程，尽管特殊解法较为灵活，但同学们不应畏惧。

**例题 6**

$$
\int\dfrac{1}{1-x^4}
$$

**解：**

$$
\begin{aligned}
I &= \dfrac{1}{2}\int \left( \dfrac{1}{1+x^2} + \dfrac{1}{1-x^2} \right) \mathrm{d}x = \dfrac{1}{2}\left( \int \dfrac{1}{1+x^2}\mathrm{d}x + \dfrac{1}{2}\int \left( \dfrac{1}{1-x} + \dfrac{1}{1+x} \right) \mathrm{d}x \right) \\
&= \dfrac{1}{4}\ln\left| \dfrac{x+1}{x-1} \right| + \dfrac{1}{2}\arctan x + C
\end{aligned}
$$

!!! Tip
    在进行有理函数积分时，有时可依据分母形式对分子进行改造，以此达成**裂项**目的，类似题目如下：
    
    **类题 1**：

    $$
    \int\dfrac{1}{x^{8}(1 + x^{2})}\mathrm{d}x
    $$
    
    **解：**

    $$
    \begin{aligned}
    I &= \int \dfrac{x^8+1-x^8}{x^8(1+x^2)}\mathrm{d}x = -\int \dfrac{(x^4+1)(x^2+1)(x^2-1)}{x^8(1+x^2)}\mathrm{d}x + \arctan x + C \\
    &= -\int \dfrac{x^6+x^2-x^4-1}{x^8}\mathrm{d}x + \arctan x + C \\
    &= -\dfrac{1}{7x^7} + \dfrac{1}{5x^5} - \dfrac{1}{3x^3} - \dfrac{1}{x} + \arctan x + C
    \end{aligned}
    $$
    
    可以改造分子
    
    也可尝试倒代换\(x = \dfrac{1}{t}\)（倒代换一般适用于分母次数远高于分子时）
    
    **类题 2**：
    
    $$
    \int\dfrac{1 + x^{4}}{1 + x^{6}}\mathrm{d}x
    $$
    
    **解：**

    $$
    \begin{aligned}
    I &= \int \dfrac{1+x^4-x^2+x^2}{1+x^6}\mathrm{d}x = \int \dfrac{1+x^4-x^2}{(1+x^2)(1-x^2+x^4)}\mathrm{d}x + \dfrac{1}{3}\int \dfrac{1}{1+(x^3)^2}\mathrm{d}(x^3) \\
    &= \arctan x + \dfrac{1}{3}\arctan x^3 + C
    \end{aligned}
    $$
    
    
    **类题 3**：\(\displaystyle\int\dfrac{1}{x(x^{3}+27)}\mathrm{d}x\)

    **解：**
    
    $$
    I = \dfrac{1}{27}\int \dfrac{x^3+27-x^3}{x(x^3+27)}\mathrm{d}x = \dfrac{1}{27}\ln|x| - \dfrac{1}{81}\ln|x^3+27| + C
    $$

    关于类题3，其实一般形式为:

    $$
    \int\dfrac{1}{xf(x^n)}\mathrm{d}x = \dfrac{1}{n}\int\dfrac{\mathrm{d}(x^n)}{x^n f(x^n)} = \dfrac{1}{n}\int\dfrac{\mathrm{d}t}{t f(t)}
    $$

    更多地，还有如下积分

    $$
    \int \dfrac{1}{\sqrt[n]{1+x^n}}\mathrm{d}x = \int\dfrac{1}{x\sqrt[n]{1+\frac{1}{x^n}}}\mathrm{d}x
    $$



**例题 7**：

$$
\int\dfrac{1 + x^{2}}{1 + x^{4}}\mathrm{d}x
$$

**解：**

$$
I = \int \dfrac{1+\frac{1}{x^2}}{x^2+\frac{1}{x^2}}\mathrm{d}x = \int \dfrac{\mathrm{d}(x-\frac{1}{x})}{(x-\frac{1}{x})^2+2} = \dfrac{1}{\sqrt{2}}\arctan\dfrac{x-\frac{1}{x}}{\sqrt{2}} + C
$$

注：被积函数是连续的，而其计算得到的原函数（含 \(\arctan(x-1/x)\)）含有间断点 \(x=0\)，此处严格来说需要定义分段函数以保证原函数连续性。

$$
F(x) = \begin{cases} \dfrac{1}{\sqrt{2}}\arctan\dfrac{x-\frac{1}{x}}{\sqrt{2}} + C, & x > 0 \\ C, & x=0 \\ \dfrac{1}{\sqrt{2}}\arctan\dfrac{x-\frac{1}{x}}{\sqrt{2}} + C + \dfrac{\pi}{\sqrt{2}}, & x < 0 \end{cases}
$$

!!! Summary
    此例题**解法经典且独具特色**，**通过该题可解决所有形如\(\displaystyle\int\dfrac{1\pm x^{2}}{1 + kx^{2}+x^{4}}\mathrm{d}x\)的积分。**
    
    同时也可对\(1 + x^{4}\)强行因式分解为\((1 + x^{2})^{2}-2x^{2}=(1 + x^{2}+\sqrt{2}x)(1 + x^{2}-\sqrt{2}x)\)，但该方法在裂项后计算系数时运算量巨大，不太可取。类似题目还有：

    **类题 1**：
    
    $$
    \int\dfrac{1 - x^{2}}{1 + x^{4}}\mathrm{d}x
    $$
    
    **解：**

    $$
    \begin{aligned}
    I &= -\int \dfrac{1-\frac{1}{x^2}}{\frac{1}{x^2}+x^2}\mathrm{d}x = -\int \dfrac{\mathrm{d}(x+\frac{1}{x})}{(x+\frac{1}{x})^2-2} \\
    &= -\dfrac{1}{2\sqrt{2}}\ln\left| \dfrac{x+\frac{1}{x}-\sqrt{2}}{x+\frac{1}{x}+\sqrt{2}} \right| + C = -\dfrac{1}{2\sqrt{2}}\ln\left| \dfrac{x^2+1-\sqrt{2}x}{x^2+1+\sqrt{2}x} \right| + C
    \end{aligned}
    $$

    **类题 2**：
    
    $$
    \int\dfrac{1}{1 + x^{6}}\mathrm{d}x
    $$
    
    **解：**

    $$
    \begin{aligned}
    I &= \int \dfrac{1+x^2-x^2}{1+x^6}\mathrm{d}x = \int \dfrac{1}{1-x^2+x^4}\mathrm{d}x - \dfrac{1}{3}\arctan x^3 \\
    &= \dfrac{1}{2}\int \dfrac{1+\frac{1}{x^2}}{x^2+\frac{1}{x^2}-1}\mathrm{d}x + \dfrac{1}{2}\int \dfrac{1-\frac{1}{x^2}}{x^2+\frac{1}{x^2}-1}\mathrm{d}x - \dfrac{1}{3}\arctan x^3 \\
    &= \dfrac{1}{2}\int \dfrac{\mathrm{d}(x-\frac{1}{x})}{(x-\frac{1}{x})^2+1} - \dfrac{1}{2}\int \dfrac{\mathrm{d}(x+\frac{1}{x})}{(x+\frac{1}{x})^2-3} - \dfrac{1}{3}\arctan x^3 \\
    &= \dfrac{1}{2}\arctan\left(x-\dfrac{1}{x}\right) - \dfrac{1}{4\sqrt{3}}\ln\left| \dfrac{x+\frac{1}{x}-\sqrt{3}}{x+\frac{1}{x}+\sqrt{3}} \right| - \dfrac{1}{3}\arctan x^3 + C
    \end{aligned}
    $$

    利用以上两题可求得
    
    $$
    \int\dfrac{1}{1 + x^{4}}\mathrm{d}x=\dfrac{1}{2}\left[\int\dfrac{1 + x^{2}}{1 + x^{4}}\mathrm{d}x+\int\dfrac{1 - x^{2}}{1 + x^{4}}\mathrm{d}x\right]
    $$