# 不定积分3

## 换元法、分部积分法

### 根式换元

!!! Note

    见到$\sqrt{\frac{一次函数}{一次函数}}$、$\sqrt{e^{ax}+b}$、$\sqrt{\frac{e^{ax}+b}{e^{ax}-b}}$等形式，可直接将整个根号令成$t$，以消去根号。但此方法不一定是最简方法，需具体问题具体分析。

**例题1**

$$\int \sqrt{\dfrac{x}{x + 1}}\mathrm{d}x$$

**解：**


令 $\sqrt{\dfrac{x}{x + 1}}=t$，则 $x = \dfrac{t^2}{1-t^2} , \mathrm{d}x = \mathrm{d}\left(\dfrac{1}{1-t^2}\right)$。

$$
\begin{aligned}
\text{原式} &= \int t \mathrm{d}\left(\dfrac{1}{1-t^2}\right) = \dfrac{t}{1-t^2} - \int \dfrac{1}{1-t^2} \mathrm{d}t \\
&= \dfrac{t}{1-t^2} - \dfrac{1}{2}\ln\left|\dfrac{1+t}{1-t}\right| + C \\
&= (x+1)\sqrt{\dfrac{x}{x+1}} - \dfrac{1}{2}\ln\left|\dfrac{\sqrt{x+1}+\sqrt{x}}{\sqrt{x+1}-\sqrt{x}}\right| + C \\
&= \sqrt{x(x+1)} - \ln(\sqrt{x}+\sqrt{x+1}) + C
\end{aligned}
$$

> 注：换元后不要解出$\mathrm{d}x$，应直接分部积分，否则会升高分母阶数，使积分次数变高。


**类题1**

$$\int \dfrac{1}{x}\sqrt{\dfrac{x + 1}{x}}\mathrm{d}x$$

**解：**

令 $\sqrt{\dfrac{x+1}{x}}=t$，则 $x=\dfrac{1}{t^2-1}$。

$$
\begin{aligned}
\text{原式} &= \int (t^2-1) t \mathrm{d}\left(\dfrac{1}{t^2-1}\right) = \int (t^2-1) t \cdot \dfrac{-2t}{(t^2-1)^2} \mathrm{d}t \\
&= -2\int \dfrac{t^2}{t^2-1} \mathrm{d}t = -2\int \left(1+\dfrac{1}{t^2-1}\right) \mathrm{d}t \\
&= -2t - \ln\left|\dfrac{t-1}{t+1}\right| + C \\
&= -2\sqrt{\dfrac{x+1}{x}} - \ln\left|\dfrac{\sqrt{x+1}-\sqrt{x}}{\sqrt{x+1}+\sqrt{x}}\right| + C
\end{aligned}
$$

**类题2**
请计算下列两个积分

$$(1)\int \sqrt{\dfrac{1 - x}{1 + x}}\mathrm{d}x$$

$$(2)\int(\sqrt{\dfrac{1 - x}{1 + x}}+\sqrt{\dfrac{1 + x}{1 - x}})\mathrm{d}x$$

**解：**

(1) 分子有理化：

$$
\text{原式} = \int \dfrac{1-x}{\sqrt{1-x^2}} \mathrm{d}x = \int \dfrac{1}{\sqrt{1-x^2}}\mathrm{d}x - \int \dfrac{x}{\sqrt{1-x^2}}\mathrm{d}x = \arcsin x + \sqrt{1-x^2} + C
$$

(2) 通分：

$$
\text{原式} = \int \left(\dfrac{1-x}{\sqrt{1-x^2}} + \dfrac{1+x}{\sqrt{1-x^2}}\right) \mathrm{d}x = \int \dfrac{2}{\sqrt{1-x^2}} \mathrm{d}x = 2\arcsin x + C
$$

> 注：换元法可行，但思考有无简便方法（提示：分子有理化，然后裂开，拆成2个积分）

**类题3**

$$\int \dfrac{xe^{x}}{\sqrt{e^{x}-2}}\mathrm{d}x$$

**解：**

令 $\sqrt{e^x-2}=t$，则 $e^x = t^2+2, \mathrm{d}x = \dfrac{2t}{t^2+2}\mathrm{d}t$

$$
\begin{aligned}
\text{原式} &= \int \dfrac{\ln(2+t^2)(t^2+2)}{t} \cdot \dfrac{2t}{t^2+2} \mathrm{d}t = 2\int \ln(2+t^2) \mathrm{d}t \\
&= 2t\ln(2+t^2) - 2\int t \cdot \dfrac{2t}{2+t^2} \mathrm{d}t \\
&= 2t\ln(2+t^2) - 4t + 4\sqrt{2}\arctan\dfrac{t}{\sqrt{2}} + C \\
&= 2\sqrt{e^x-2}\ln(e^x) - 4\sqrt{e^x-2} + 4\sqrt{2}\arctan\dfrac{\sqrt{e^x-2}}{\sqrt{2}} + C \\
&= 2x\sqrt{e^x-2} - 4\sqrt{e^x-2} + 4\sqrt{2}\arctan\dfrac{\sqrt{e^x-2}}{\sqrt{2}} + C
\end{aligned}
$$

**类题4**

$$\int \dfrac{1}{\sqrt[3]{(x + 1)^{2}(x - 1)^{4}}}\mathrm{d}x$$

**解：**

变形为 $\int \dfrac{1}{(x-1)^2 \sqrt[3]{\left(\dfrac{x+1}{x-1}\right)^2}} \mathrm{d}x$。
令 $\sqrt[3]{\dfrac{x+1}{x-1}} = t$，则 $\dfrac{x+1}{x-1} = t^3$。求导得 $\dfrac{-2}{(x-1)^2}\mathrm{d}x = 3t^2 \mathrm{d}t \Rightarrow \dfrac{\mathrm{d}x}{(x-1)^2} = -\dfrac{3}{2}t^2 \mathrm{d}t$。

$$
\text{原式} = -\int \dfrac{1}{t^2} \cdot \dfrac{3}{2}t^2 \mathrm{d}t = -\dfrac{3}{2} \int \mathrm{d}t = -\dfrac{3}{2}t + C = -\dfrac{3}{2}\sqrt[3]{\dfrac{x+1}{x-1}} + C
$$

> 注：第一次做想不到正常


!!! Note
    为消去多个根号，需具体问题具体分析换元方式。

**例题2**

$$\int \dfrac{1}{(1+\sqrt[3]{x})\sqrt{x}}\mathrm{d}x$$

**解：**

令 $x = t^6$，则 $\mathrm{d}x = 6t^5 \mathrm{d}t$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{6t^5}{(1+t^2)t^3} \mathrm{d}t = 6\int \dfrac{t^2}{1+t^2} \mathrm{d}t = 6\int \left(1 - \dfrac{1}{1+t^2}\right) \mathrm{d}t \\
&= 6t - 6\arctan t + C = 6\sqrt[6]{x} - 6\arctan\sqrt[6]{x} + C
\end{aligned}
$$

**类题**

$$\int \dfrac{1}{1 + e^{\frac{x}{2}} + e^{\frac{x}{3}} + e^{\frac{x}{6}}}\mathrm{d}x$$

**解：**

令 $t = e^{\frac{x}{6}}$，则 $x = 6\ln t$，$\mathrm{d}x = \dfrac{6}{t} \mathrm{d}t$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{1}{1+t^3+t^2+t} \cdot \dfrac{6}{t} \mathrm{d}t = 6\int \dfrac{1}{t(1+t)(1+t^2)} \mathrm{d}t \\
&= \int \left(\dfrac{6}{t} - \dfrac{3}{1+t} - \dfrac{3t+3}{1+t^2}\right) \mathrm{d}t \\
&= 6\ln t - 3\ln(1+t) - \dfrac{3}{2}\ln(1+t^2) - 3\arctan t + C \\
&= x - 3\ln(1+e^{\frac{x}{6}}) - \dfrac{3}{2}\ln(1+e^{\frac{x}{3}}) - 3\arctan e^{\frac{x}{6}} + C
\end{aligned}
$$

### 三角换元

!!! Note
    若根号里面没有一次项，只有平方项和常数项：

    - 形如“$\sqrt{a^{2}-x^{2}}$”，令$x = a\sin t$。
    - 形如“$\sqrt{a^{2}+x^{2}}$”，令$x = a\tan t$。
    - 形如“$\sqrt{x^{2}-a^{2}}$”，令$x = a\sec t$。
        - 注：有时不一定非要出现根号才用三角换元，如$\displaystyle\int \dfrac{1}{(x^{2}+1)^{2}}\mathrm{d}x$，可用三角换元 + 二倍角处理。

    若根号里面含有一次项，先对根号里面的二次函数配方，消去一次项后转化为上述问题。


**例题3**

$$\int \dfrac{1}{x^{4}}\sqrt{4 - x^{2}}\mathrm{d}x$$

**解：**

令 $x = 2\sin t$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{2\cos t}{16\sin^4 t} \cdot 2\cos t \mathrm{d}t = \dfrac{1}{4}\int \dfrac{\cos^2 t}{\sin^4 t} \mathrm{d}t = \dfrac{1}{4}\int \cot^2 t \csc^2 t \mathrm{d}t \\
&= -\dfrac{1}{4}\int \cot^2 t \mathrm{d}(\cot t) = -\dfrac{1}{12}\cot^3 t + C \\
&= -\dfrac{1}{12} \left(\dfrac{\sqrt{4-x^2}}{x}\right)^3 + C
\end{aligned}
$$

**例题4**

$$\int \dfrac{1}{\sqrt{(x^{2}+1)^{3}}}\mathrm{d}x$$

**解：**

令 $x = \tan t$。

$$
\text{原式} = \int \dfrac{1}{\sec^3 t} \sec^2 t \mathrm{d}t = \int \cos t \mathrm{d}t = \sin t + C = \dfrac{x}{\sqrt{1+x^2}} + C
$$

**例题5**

$$\int \dfrac{1}{\sqrt{x(4 - x)}}\mathrm{d}x$$

**解：**

配方：$\sqrt{x(4-x)} = \sqrt{4x-x^2} = \sqrt{4-(x-2)^2}$。
令 $x-2 = 2\sin t$。

$$
\text{原式} = \int \dfrac{1}{\sqrt{4-(x-2)^2}}\mathrm{d}x = \int 1 \mathrm{d}t = t + C = \arcsin\dfrac{x-2}{2} + C
$$

**例题6**

$$\int x\sqrt{2x - x^{2}}\mathrm{d}x$$

**解：**

配方：$2x-x^2 = 1-(x-1)^2$。令 $x-1 = \sin t$。

$$
\begin{aligned}
\text{原式} &= \int (\sin t + 1)\cos^2 t \mathrm{d}t = -\int \cos^2 t \mathrm{d}(\cos t) + \int \dfrac{1+\cos 2t}{2} \mathrm{d}t \\
&= -\dfrac{1}{3}\cos^3 t + \dfrac{1}{2}t + \dfrac{1}{4}\sin 2t + C \\
&= -\dfrac{1}{3}(1-(x-1)^2)^{\frac{3}{2}} + \dfrac{1}{2}\arcsin(x-1) + \dfrac{1}{2}(x-1)\sqrt{1-(x-1)^2} + C
\end{aligned}
$$

**例题7**

$$\int \dfrac{1}{x^{2}\sqrt{x^{2}-1}}\mathrm{d}x$$

**解：**

令 $x = \sec t$。

$$
\text{原式} = \int \dfrac{\sec t \tan t}{\sec^2 t \tan t} \mathrm{d}t = \int \cos t \mathrm{d}t = \sin t + C = \dfrac{\sqrt{x^2-1}}{x} + C
$$

!!! Note
    注：令$x = \sec t$可行，但本题可归为一种模型，即一切可化为$\int \dfrac{1}{(x + d)\sqrt{ax^{2}+bx + c}}\mathrm{d}x$和$\int \dfrac{1}{(x + d)^{2}\sqrt{ax^{2}+bx + c}}\mathrm{d}x$的不定积分，可用倒代换$x + d=\dfrac{1}{t}$简化后积分。

**类题1**

$$\int \dfrac{1}{x\sqrt{2x^{2}+2x + 1}}\mathrm{d}x$$

**解：**

令 $x = \dfrac{1}{t}$，$\mathrm{d}x = -\dfrac{1}{t^2}\mathrm{d}t$。

$$
\begin{aligned}
\text{原式} &= -\int \dfrac{1}{\frac{1}{t}\sqrt{\frac{2}{t^2}+\frac{2}{t}+1}} \dfrac{1}{t^2} \mathrm{d}t = -\int \dfrac{1}{\sqrt{t^2+2t+2}} \mathrm{d}t = -\int \dfrac{\mathrm{d}(t+1)}{\sqrt{(t+1)^2+1}} \\
&= -\ln|t+1+\sqrt{(t+1)^2+1}| + C \\
&= -\ln\left|\dfrac{1}{x}+1+\sqrt{\left(\dfrac{1}{x}+1\right)^2+1}\right| + C
\end{aligned}
$$

**类题2**

$$\int \dfrac{1}{x^{2}\sqrt{2x^{2}+2x + 1}}\mathrm{d}x$$

**解：**

令 $x = \dfrac{1}{t}$。

$$
\begin{aligned}
\text{原式} &= -\int \dfrac{t+1-1}{\sqrt{(t+1)^2+1}} \mathrm{d}t = -\int \dfrac{t+1}{\sqrt{(t+1)^2+1}}\mathrm{d}t + \int \dfrac{1}{\sqrt{(t+1)^2+1}}\mathrm{d}t \\
&= -\sqrt{t^2+2t+2} + \ln|t+1+\sqrt{t^2+2t+2}| + C \\
&= -\dfrac{\sqrt{2x^2+2x+1}}{x} + \ln\left|\dfrac{1}{x}+1+\dfrac{\sqrt{2x^2+2x+1}}{x}\right| + C
\end{aligned}
$$

### 分部积分法


!!! Note
    见到不同种类函数相乘，一般用分部积分公式$\displaystyle\int u\mathrm{d}v = uv-\displaystyle\int v\mathrm{d}u$。

    分部积分使用原则：
    - 口诀：按**反|对|幂|指|三**顺序，谁排在后面，就把谁凑到微分符号$\mathrm{d}$后面，然后分部积分。
    - 思想：“对/反”函数求导后不再是同类函数，所以要把其他函数凑到$\mathrm{d}$后分部积分，使$\mathrm{d}$对“对/反”函数求导；指数函数与幂函数相乘时，幂函数怕求导，指数函数不怕，所以把指数函数凑到$d$后。总之，谁怕求导，就把其余部分凑到$\mathrm{d}$后。


**例题1**

$$\int x\arctan x\mathrm{d}x$$

**解：**


$$
\begin{aligned}
\text{原式} &= \dfrac{1}{2}\int \arctan x \mathrm{d}(x^2+1) = \dfrac{1}{2}(x^2+1)\arctan x - \dfrac{1}{2}\int (x^2+1) \dfrac{1}{1+x^2} \mathrm{d}x \\
&= \dfrac{1}{2}(x^2+1)\arctan x - \dfrac{1}{2}x + C
\end{aligned}
$$

> 注：分部积分时，善于在$\mathrm{d}$后增减常数使式子更简洁。


**类题**

$$\int x\cdot\ln(1 + x^{2}) \arctan x\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \dfrac{1}{2}\int \arctan x \ln(x^2+1) \mathrm{d}(x^2+1) \\
&= \dfrac{1}{2}(x^2+1)\ln(x^2+1)\arctan x - \dfrac{1}{2}\int (x^2+1)\left[ \dfrac{2x}{x^2+1}\arctan x + \dfrac{\ln(x^2+1)}{1+x^2} \right] \mathrm{d}x \\
&= \dfrac{1}{2}(x^2+1)\ln(x^2+1)\arctan x - \int x \arctan x \mathrm{d}x - \dfrac{1}{2}\int \ln(x^2+1) \mathrm{d}x \\
&= \dfrac{1}{2}(x^2+1)\ln(x^2+1)\arctan x - \left( \dfrac{1}{2}(x^2+1)\arctan x - \dfrac{x}{2} \right) - \left( \dfrac{x}{2}\ln(x^2+1) - x + \arctan x \right) + C
\end{aligned}
$$

**例题2**

$$\int e^{x}\sin x\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int \sin x \mathrm{d}(e^x) = e^x \sin x - \int e^x \cos x \mathrm{d}x \\
&= e^x \sin x - \left( \int \cos x \mathrm{d}(e^x) \right) = e^x \sin x - (e^x \cos x - \int e^x (-\sin x) \mathrm{d}x) \\
&= e^x \sin x - e^x \cos x - \int e^x \sin x \mathrm{d}x \\
\Rightarrow 2\int e^x \sin x \mathrm{d}x &= e^x(\sin x - \cos x) \\
\therefore \int e^x \sin x \mathrm{d}x &= \dfrac{e^x}{2}(\sin x - \cos x) + C
\end{aligned}
$$

> 注：被积函数为指数函数和三角函数相乘时，需连续两次分部积分，出现“积分重现”后解决问题，且两次分部积分凑到$d$后的函数必须同类，否则原路返回。


**类题**

$$\int x\cdot e^{x}\sin x\mathrm{d}x$$

**解：**

$$
\text{原式} = \dfrac{1}{2}\int x \mathrm{d}\left( e^x(\sin x - \cos x) \right) = \dfrac{x}{2}e^x(\sin x - \cos x) - \dfrac{1}{2}\int e^x(\sin x - \cos x) \mathrm{d}x
$$
后半部分即为标准指数三角积分，分别计算即可。
$$
= \dfrac{x}{2}e^x(\sin x - \cos x) - \dfrac{1}{2}e^x \sin x + C
$$

**例题3**

$$\int\ln^{2}(x+\sqrt{1 + x^{2}})\mathrm{d}x$$

**解：**

直接分部积分即可，答案为：

$= x \ln^2(x+\sqrt{1+x^2}) - 2\sqrt{1+x^2}\ln(x+\sqrt{1+x^2}) + 2x + C$


### 换元法 + 分部积分

换元后分部积分是常见出题风格，需熟练掌握。若预判需换元与分部积分，建议先换元，因其可使被积表达式更“清爽”利于后续操作。

**例题1**

$$\int e^{2x}\arctan\sqrt{e^{x}-1}\mathrm{d}x$$

**解：**

令 $\sqrt{e^x-1}=t$，则 $e^x = t^2+1$，$\mathrm{d}x = \dfrac{2t}{t^2+1}\mathrm{d}t$。

$$
\begin{aligned}
\text{原式} &= \int (t^2+1)^2 \arctan t \cdot \dfrac{2t}{t^2+1} \mathrm{d}t \\
&= \int (t^2+1) \arctan t \cdot 2t \mathrm{d}t = \int \arctan t \mathrm{d}((t^2+1)^2) \\
&= (t^2+1)^2 \arctan t - \int (t^2+1)^2 \dfrac{1}{1+t^2} \mathrm{d}t \\
&= (t^2+1)^2 \arctan t - \int (t^2+1) \mathrm{d}t \\
&= e^{2x} \arctan\sqrt{e^x-1} - \dfrac{1}{3}(e^x-1)^{\frac{3}{2}} - \sqrt{e^x-1} + C
\end{aligned}
$$

**类题1**

$$\int \dfrac{x\cdot e^{\arctan x}}{(1 + x^{2})^{\frac{3}{2}}}\mathrm{d}x$$

$$\int \dfrac{e^{\arctan x}}{(1 + x^{2})^{\frac{3}{2}}}\mathrm{d}x$$

**解：**

令 $x = \tan t$。

(1) $\displaystyle \int \dfrac{\tan t \cdot e^t}{\sec^3 t} \sec^2 t \mathrm{d}t = \int \sin t e^t \mathrm{d}t = \dfrac{e^t}{2}(\sin t - \cos t) + C$
代回 $t=\arctan x$。

(2) $\displaystyle \int \dfrac{e^t}{\sec^3 t} \sec^2 t \mathrm{d}t = \int \cos t e^t \mathrm{d}t = \dfrac{e^t}{2}(\sin t + \cos t) + C$

**类题2**

$$
\int \dfrac{\ln x}{(1 + x^{2})^{\frac{3}{2}}}\mathrm{d}x
$$

**解：**

令 $x = \tan t$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{\ln \tan t}{\sec^3 t} \sec^2 t \mathrm{d}t = \int \cos t \ln \tan t \mathrm{d}t = \int \ln \tan t \mathrm{d}(\sin t) \\
&= \sin t \ln \tan t - \int \sin t \dfrac{\sec^2 t}{\tan t} \mathrm{d}t = \sin t \ln \tan t - \int \sec t \mathrm{d}t \\
&= \dfrac{x}{\sqrt{1+x^2}} \ln x - \ln|x+\sqrt{1+x^2}| + C
\end{aligned}
$$

**类题3**

$$\int \dfrac{\arctan\sqrt{x - 1}}{x\sqrt{x - 1}}\mathrm{d}x$$

**解：**

(1) 令 $\sqrt{x-1}=t$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{\arctan t}{(t^2+1)t} \cdot 2t \mathrm{d}t = 2\int \dfrac{\arctan t}{1+t^2} \mathrm{d}t = (\arctan t)^2 + C \\
&= (\arctan\sqrt{x-1})^2 + C
\end{aligned}
$$



**例题2**

$$\int\ln(1+\sqrt{\dfrac{1 + x}{x}})\mathrm{d}x$$

**解：**

令 $\sqrt{\dfrac{1+x}{x}} = t$，则 $x = \dfrac{1}{t^2-1}$。

$$
\begin{aligned}
\text{原式} &= \int \ln(1+t) \mathrm{d}\left(\dfrac{1}{t^2-1}\right) = \dfrac{\ln(1+t)}{t^2-1} - \int \dfrac{1}{t^2-1} \dfrac{1}{1+t} \mathrm{d}t \\
&= \dfrac{\ln(1+t)}{t^2-1} - \int \dfrac{1}{(t-1)(t+1)^2} \mathrm{d}t \\
&= \dots \quad (\text{有理函数积分}) \\
&= x\ln\left(1+\sqrt{\dfrac{1+x}{x}}\right) + \dfrac{1}{2}\ln(\sqrt{x}+\sqrt{1+x}) + \dfrac{1}{2}x - \dfrac{1}{2}\sqrt{x^2+x} + C
\end{aligned}
$$

> 注：换元后不解出$x$，直接分部积分消去对数符号。若解出$x$再代入，计算更繁琐。类似题目还有：


**类题1**


$$\int\arctan(1+\sqrt{x})\mathrm{d}x$$

**解：**

令 $\sqrt{x}=t$。

$$
\text{原式} = \int \arctan(1+t) \cdot 2t \mathrm{d}t = t^2\arctan(1+t) - t + \ln(t^2+2t+2) + C
$$

回代即可


### 利用分部积分对分母进行降阶

分母次数高时，除倒代换外，可用分部积分降阶，核心是将分母凑到$\mathrm{d}$后分部积分。

**例题1**

$$\int \dfrac{xe^{x}}{(1 + x)^{2}}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int xe^x \mathrm{d}\left(-\dfrac{1}{1+x}\right) = -\dfrac{xe^x}{1+x} + \int \dfrac{1}{1+x}(e^x+xe^x) \mathrm{d}x \\
&= -\dfrac{xe^x}{1+x} + \int e^x \mathrm{d}x = -\dfrac{xe^x}{1+x} + e^x + C = \dfrac{e^x}{1+x} + C
\end{aligned}
$$

**类题1**

$$\int \dfrac{x^{2}e^{x}}{(x + 2)^{2}}\mathrm{d}x$$

**解：**

$\text{原式} = \displaystyle\int x^2 e^x \mathrm{d}\left(-\dfrac{1}{x+2}\right)= -\dfrac{x^2 e^x}{x+2} + \displaystyle\int \dfrac{e^x(2x+x^2)}{x+2} \mathrm{d}x$

$= -\dfrac{x^2 e^x}{x+2} + \displaystyle\int xe^x \mathrm{d}x = -\dfrac{x^2 e^x}{x+2} + (x-1)e^x + C$

**类题2**

$$\int \dfrac{xe^{x}}{(1 + e^{x})^{2}}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int x \cdot \dfrac{e^x}{(1+e^x)^2} \mathrm{d}x = \int x \mathrm{d}\left(-\dfrac{1}{1+e^x}\right) \\
&= -\dfrac{x}{1+e^x} + \int \dfrac{1}{1+e^x} \mathrm{d}x = -\dfrac{x}{1+e^x} + \ln\dfrac{e^x}{1+e^x} + C
\end{aligned}
$$

以下例题需用“强制凑微分”技巧，核心仍是对分母降阶。


**例题2**

$$\int \dfrac{x^{2}}{(x\sin x+\cos x)^{2}}\mathrm{d}x$$

**解：**

观察分母，$(x\sin x + \cos x)' = \sin x + x\cos x - \sin x = x\cos x$。

$$
\begin{aligned}
\text{原式} &= \int \dfrac{x}{\cos x} \cdot \dfrac{x\cos x}{(x\sin x + \cos x)^2} \mathrm{d}x \\
&= \int \dfrac{x}{\cos x} \mathrm{d}\left(-\dfrac{1}{x\sin x+\cos x}\right) \\
&= -\dfrac{x}{\cos x(x\sin x+\cos x)} + \int \dfrac{1}{x\sin x+\cos x} \cdot \dfrac{\cos x + x\sin x}{\cos^2 x} \mathrm{d}x \\
&= -\dfrac{x}{\cos x(x\sin x+\cos x)} + \tan x + C
\end{aligned}
$$

### 利用分部积分实现“积分抵消”


有些题目将积分拆成两个，对其中一个积分$I_{2}$用分部积分，使其与另一个积分$I_{1}$抵消。被积函数一般含指数函数$e^{x}$。


**例题1**

$$\int \dfrac{xe^{x}}{(1 + x)^{2}}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int \dfrac{[(x+1)-1]e^x}{(1+x)^2}\mathrm{d}x \\
&= \int \dfrac{e^x}{1+x}\mathrm{d}x - \int \dfrac{e^x}{(1+x)^2}\mathrm{d}x \\
&= \int \dfrac{e^x}{1+x}\mathrm{d}x + \int e^x \mathrm{d}\left(\dfrac{1}{1+x}\right) \quad \text{（凑微分）} \\
&= \int \dfrac{e^x}{1+x}\mathrm{d}x + \left[ \dfrac{e^x}{1+x} - \int \dfrac{1}{1+x} \mathrm{d}(e^x) \right] \quad \text{（分部积分）} \\
&= \boxed{\int \dfrac{e^x}{1+x}\mathrm{d}x} + \dfrac{e^x}{1+x} - \boxed{\int\dfrac{e^x}{1+x}\mathrm{d}x} \\
&= \dfrac{e^x}{1+x} + C
\end{aligned}
$$

> $\displaystyle\int e^x(f(x)+f'(x))\mathrm{d}x = e^xf(x)+C$

**类题1**

$$\int \dfrac{(1+\sin x)e^{x}}{1+\cos x}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int \left(\dfrac{1}{1+\cos x} + \dfrac{\sin x}{1+\cos x}\right)e^x \mathrm{d}x
\end{aligned}
$$

注意到$\left(\dfrac{\sin x}{1+\cos x}\right)' = \dfrac{1}{1+\cos x}$

**类题2**

$$\int e^{x}\left(\dfrac{1 - x}{1 + x^{2}}\right)^{2}\mathrm{d}x$$

**解：**

原式 $= \displaystyle\int e^x\left(\dfrac{1+x^2-2x}{(1+x^2)^2}\right)\mathrm{d}x$

**类题3**

$$\int \dfrac{x^{2}e^{x}}{(x + 2)^{2}}\mathrm{d}x$$

**例题2**

$$\int \dfrac{e^{-\sin x}\cdot\sin 2x}{\sin^{4}\left(\dfrac{\pi}{4}-\dfrac{x}{2}\right)}\mathrm{d}x$$

**解：**

$$
I = \int \dfrac{e^{-\sin x} \cdot 2\sin x \cos x}{\frac{(1-\sin x)^2}{4}} \mathrm{d}x = 8 \int \dfrac{e^{-\sin x} \sin x}{(1-\sin x)^2} \cos x \mathrm{d}x
$$

令 $\sin x = t$，则 $\mathrm{d}t = \cos x \mathrm{d}x$。

$$
I = 8 \int \dfrac{t e^{-t}}{(1-t)^2} \mathrm{d}t = 8 \int \dfrac{t e^{-t}}{(t-1)^2} \mathrm{d}t
$$


**例题3**

$$\int e^{-\frac{x}{2}}\dfrac{\cos x-\sin x}{\sqrt{\sin x}}\mathrm{d}x$$

**解：**

$$
\text{原式} = \int e^{-\frac{x}{2}} \boxed{\dfrac{\cos x}{\sqrt{\sin x}}} \mathrm{d}x - \int e^{-\frac{x}{2}} \sqrt{\sin x} \mathrm{d}x
$$


**类题1**

$$\int e^{\sin x}\dfrac{x\cos^{3}x-\sin x}{\cos^{2}x}\mathrm{d}x$$

**解：**

$$
\text{原式} = \int x \mathrm{d}(e^{\sin x}) - \int e^{\sin x} \mathrm{d}\dfrac{1}{\cos x} = xe^{\sin x} - \dfrac{e^{\sin x}}{\cos x} + C
$$


**例题3**

$$\int(\ln\ln x+\dfrac{1}{\ln x})\mathrm{d}x$$

**解：**

$$
\text{原式} = x\ln\ln x - \int x \dfrac{1}{\ln x} \dfrac{1}{x} \mathrm{d}x + \int \dfrac{1}{\ln x} \mathrm{d}x = x\ln\ln x + C
$$

**例题4**

已知$f''(x)$连续，$f'(x)\neq0$，求

$$\int\left[\dfrac{f(x)}{f'(x)}-\dfrac{f^{2}(x)f''(x)}{(f'(x))^{3}}\right]\mathrm{d}x$$

**解：**

$$
\text{原式} = \int \dfrac{f}{f'} \mathrm{d}x - \int \dfrac{f^2}{f'^3} \mathrm{d}(f') = \dots = \dfrac{1}{2}\left(\dfrac{f(x)}{f'(x)}\right)^2 + C
$$

**例题5**

$$\int \dfrac{1-\ln x}{(x-\ln x)^{2}}\mathrm{d}x$$

**解：**

$$
\text{原式} = \int \dfrac{1}{x-\ln x} \mathrm{d}x + \int \dfrac{1-x}{(x-\ln x)^2} \mathrm{d}x = \dfrac{x}{x-\ln x} + C
$$

> 第一项分母次数降下来了，考虑分部积分尝试抵消第二项

### 对复杂因子求导，期待出现奇迹


被积函数某部分出现复杂“整体”（复合函数或两函数乘积）时，对其求导看特点，便于后续凑微分等操作。


**例题1**

$$\int \dfrac{\ln x}{\sqrt{1 + [x(\ln x - 1)]^{2}}}\mathrm{d}x$$

**解：**

观察 $[x(\ln x - 1)]' = \ln x - 1 + 1 = \ln x$。

$$
\text{原式} = \int \dfrac{\mathrm{d}(x(\ln x - 1))}{\sqrt{1+[x(\ln x - 1)]^2}} = \ln(x(\ln x - 1) + \sqrt{1+[x(\ln x - 1)]^2}) + C
$$

**例题2**

$$\int \dfrac{x + 1}{x(1 + xe^{x})}\mathrm{d}x$$

**解：**

$(xe^x)' = e^x(1+x)$。

$$
\text{原式} = \int \dfrac{e^x(x+1)}{xe^x(1+xe^x)} \mathrm{d}x = \int \dfrac{\mathrm{d}(xe^x)}{xe^x(1+xe^x)} = \ln\left|\dfrac{xe^x}{1+xe^x}\right| + C
$$

**类题**

$$\int \dfrac{1 + x\cos x}{x(1 + xe^{\sin x})}\mathrm{d}x$$

**解：**

$(xe^{\sin x})' = e^{\sin x}(1+x\cos x)$

!!! Note

    注1：通过例题2和类题可总结出题模板$\displaystyle\int \dfrac{1 + xf'(x)}{x(1 + xe^{f(x)})}\mathrm{d}x=\int \dfrac{[1 + xf'(x)]e^{f(x)}}{xe^{f(x)}(1 + xe^{f(x)})}\mathrm{d}x=\int \dfrac{[xe^{f(x)}]'}{xe^{f(x)}(1 + xe^{f(x)})}\mathrm{d}x=\ln|\dfrac{xe^{f(x)}}{1 + xe^{f(x)}}| + C$


**例题3**

$$\int \dfrac{1-\ln x}{(x-\ln x)^{2}}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int \dfrac{1-\ln x}{x^2 \left(1-\frac{\ln x}{x}\right)^2}\mathrm{d}x \\
&= \int \dfrac{1}{\left(1-\frac{\ln x}{x}\right)^2} \cdot \dfrac{1-\ln x}{x^2}\mathrm{d}x \\
&= \int \dfrac{1}{\left(\frac{\ln x}{x}-1\right)^2} \mathrm{d}\left(\dfrac{\ln x}{x}\right)\\
&= \dfrac{x}{x-\ln x} + C
\end{aligned}
$$

**类题1**

$$\int \dfrac{e^{x}(x - 1)}{(x - e^{x})^{2}}\mathrm{d}x$$

**解：**

$$
\text{原式} = \int \dfrac{e^x(x-1)}{x^2(1-\frac{e^x}{x})^2} \mathrm{d}x = \dots = \dfrac{1}{1-\frac{e^x}{x}} + C = \dfrac{x}{x-e^x} + C
$$

**类题2**

$$\int \dfrac{x+\sin x\cdot\cos x}{(\cos x - x\cdot\sin x)^{2}}\mathrm{d}x$$

**解：**

$$
\begin{aligned}
\text{原式} &= \int \dfrac{x+\sin x\cos x}{\cos^2 x (1-x\tan x)^2} \mathrm{d}x \\
&= \int \dfrac{x\sec^2 x + \tan x}{(1-x\tan x)^2} \mathrm{d}x
\end{aligned}
$$

观察分子，发现恰好是 $x\tan x$ 的导数：

$$
(x\tan x)' = 1 \cdot \tan x + x \cdot \sec^2 x
$$

于是进行凑微分：

$$
\begin{aligned}
\text{原式} &= \int \dfrac{\mathrm{d}(x\tan x)}{(1-x\tan x)^2} \\
&= -\dfrac{1}{x\tan x - 1} + C
\end{aligned}
$$