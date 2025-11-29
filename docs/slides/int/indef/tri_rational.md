# 不定积分2

## 三角有理函数积分


### 万能公式

一切三角有理函数的积分，只需利用**万能公式**，令\(\tan(\dfrac{x}{2}) = t\)，就总能将三角有理函数的积分化为有理函数的积分。而由于一切有理函数的积分方法我们都已经学会，所以——“从理论上来说”，三角有理函数的积分本身并没有本质上的困难；但就像前文所述，通法并不一定是好方法，利用万能公式计算三角有理函数的积分是下下策，因为这种解法的计算量往往会很大，尤其是被积函数的次数太高时，计算量是不可想象的。

所以，我们常常希望避开万能公式去求解三角有理函数的积分。当然，为了不出现知识盲区，我们还是以两道题目为例，来展示一下三角有理函数的万能公式解法。

**例题1**：

$$
\int\frac{1}{3 + 5\cos x}\mathrm{d}x
$$

**解：** 使用万能公式，令 \(u = \tan\dfrac{x}{2}\)

$$
\begin{aligned}
I &= \int \dfrac{1}{3+5\frac{1-u^2}{1+u^2}}\cdot\dfrac{2}{1+u^2}\mathrm{d}u = \int \dfrac{1}{4-u^2}\mathrm{d}u = \dfrac{1}{4}\int \left(\dfrac{1}{2-u} + \dfrac{1}{2+u}\right)\mathrm{d}u \\
&= \dfrac{1}{4}\ln\left|\dfrac{u+2}{u-2}\right| + C = \dfrac{1}{4}\ln\left|\dfrac{\tan\frac{x}{2}+2}{\tan\frac{x}{2}-2}\right| + C
\end{aligned}
$$

**例题2**：

$$
\int\dfrac{1}{1+ \sin x+\cos x}\mathrm{d}x
$$

**解：** 使用万能公式，令 \(u = \tan\dfrac{x}{2}\)

$$
I = \int \dfrac{1}{1+\frac{2u}{1+u^2}+\frac{1-u^2}{1+u^2}}\cdot\dfrac{2}{1+u^2}\mathrm{d}u = \int \dfrac{1}{u+1}\mathrm{d}u = \ln|u+1| + C = \ln\left|\tan\dfrac{x}{2}+1\right| + C
$$

### 特殊解法

我们一般都是具体问题具体分析，灵活使用三角函数的各种恒等变形和凑微分技巧，达到快速求解的目的。总的来说，有以下几个小技巧——

#### 化简分母

如果分母为\(1\pm\cos x\)或者\(1\pm\sin x\)，那么我们可以尝试分子分母**乘以共轭表达式**，使分母从两项变为一项，达到化简的效果。因为，对于一个不定积分而言，如果分母项数太多，将是非常难于处理的；而如果分母只有一项，分子就算有很多项相加，我们也可以将整个积分拆分成若干个小积分，分别计算即可。当然，除了乘以共轭表达式以外，还可以利用\(\cos 2x\)的二倍角公式，也能达到缩分母的效果。


**例题3**：

$$
\int\frac{1}{1 + \cos x}\mathrm{d}x
$$

**解：**

$$
I = \int \dfrac{1}{2\cos^2\frac{x}{2}}\mathrm{d}x = \tan\dfrac{x}{2} + C
$$

**类题1**：

$$
\int\frac{\sin x}{1 + \sin x}\mathrm{d}x
$$

**解：**

$$
\int\frac{\sin x +1 -1}{1 + \sin x}\mathrm{d}x = 1-\int\dfrac{\mathrm{d}x}{1+\sin x}
$$

!!! Tip
    本题可以分子\(+1 - 1\)然后拆开，然后转化为上一题；也可以直接分子分母乘以\((1-\sin x)\)


**类题2**：

$$
\int\frac{1}{\sin x + \cos x}\mathrm{d}x
$$ 

**解：**

$$
I = \int \dfrac{1}{\sqrt{2}\sin(x+\frac{\pi}{4})}\mathrm{d}x = \dfrac{1}{\sqrt{2}}\ln\left|\csc(x+\dfrac{\pi}{4}) - \cot(x+\dfrac{\pi}{4})\right| + C
$$

!!! Tips
    辅助角公式$\sin x + \cos x = \sqrt{2}\sin(x + \dfrac{\pi}{4})$虽然用的频率不高，但是也需要记住，偶尔会产生奇效


**类题3**：

$$
\int\frac{\cos x}{\sin x + \cos x}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\cos(x+\frac{\pi}{4}-\frac{\pi}{4})}{\sqrt{2}\sin(x+\frac{\pi}{4})}\mathrm{d}x = \dfrac{1}{\sqrt{2}}\int \dfrac{\frac{\sqrt{2}}{2}\cos(x+\frac{\pi}{4}) + \frac{\sqrt{2}}{2}\sin(x+\frac{\pi}{4})}{\sin(x+\frac{\pi}{4})}\mathrm{d}x \\
&= \dfrac{1}{2}\int \cot(x+\dfrac{\pi}{4})\mathrm{d}x + \dfrac{1}{2}\int \mathrm{d}x = \dfrac{1}{2}\ln\left|\sin(x+\dfrac{\pi}{4})\right| + \dfrac{1}{2}x + C = \dfrac{1}{2}\ln|\sin x + \cos x| + \dfrac{1}{2}x + C
\end{aligned}
$$

#### \(R(\sin x,-\cos x)=-R(\sin x,\cos x)\)

!!! Tip
    把$\cos x$凑到$\mathrm{d}$后面凑微分


**例题4**：

$$
\int\frac{1}{\sin^{2}x\cdot\cos x}\mathrm{d}x
$$

**解：**

$$
I = \int\dfrac{\cos x\mathrm{d}x}{\sin^2x\cos^2x} = \int\dfrac{\mathrm{d}(\sin x)}{\sin^2x(1-\sin^2x)}
$$

或者

$$
I = \int \dfrac{\sin^2 x + \cos^2 x}{\sin^2 x \cos x}\mathrm{d}x = \ln|\sec x + \tan x| - \dfrac{1}{\sin x} + C
$$

**例题5**：

$$
\int\frac{\cos^{3}x - 2\cos x}{1 + \sin^{2}x + \sin^{4}x}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\cos^2 x - 2}{1+\sin^2 x + \sin^4 x}\mathrm{d}(\sin x) = -\int \dfrac{1+\sin^2 x}{1+\sin^2 x + \sin^4 x}\mathrm{d}(\sin x) = -\int \dfrac{1+\frac{1}{u^2}}{u^2+1+\frac{1}{u^2}}\mathrm{d}u \\
&= -\int \dfrac{\mathrm{d}(u-\frac{1}{u})}{(u-\frac{1}{u})^2+3} = -\dfrac{1}{\sqrt{3}}\arctan\left(\dfrac{u-\frac{1}{u}}{\sqrt{3}}\right) + C = -\dfrac{1}{\sqrt{3}}\arctan\left(\dfrac{\sin x - \frac{1}{\sin x}}{\sqrt{3}}\right) + C
\end{aligned}
$$

> 此题要联系上一讲的结论

**例题6**：

$$
\int\sec^3 x\mathrm{d}x
$$

**解：**法1

$$
I = \int\dfrac{\mathrm{d}x}{\cos^3 x} = \int\dfrac{\mathrm{d}(\sin x)}{(1-\sin^2 x)^2}
$$



解法2：

$$
\begin{aligned}
I &= \int \sec x \mathrm{d}(\tan x) = \sec x \tan x - \int \sec x \tan^2 x \mathrm{d}x = \sec x \tan x - \int \sec x (\sec^2 x - 1) \mathrm{d}x \\
&= \sec x \tan x + \int \sec x \mathrm{d}x - I \\
&\implies 2I = \sec x \tan x + \ln|\sec x + \tan x| \\
&\implies I = \dfrac{1}{2}(\sec x \tan x + \ln|\sec x + \tan x|) + C
\end{aligned}
$$

!!! Note
    注：本题除了利用\(R(\sin x,-\cos x)=-R(\sin x,\cos x)\)外，还可以使用分部积分，然后出现积分重现，即可解出我们需要的\(\displaystyle\int\sec^{3}x\mathrm{d}x\)。利用这个思想，我们解决下面两个类题——
    **类题1**：

    $$
    \int\sqrt{1 + x^{2}}\mathrm{d}x
    $$
    
    **解：**

    $$
    \begin{aligned}
    I &= x\sqrt{1+x^2} - \int \dfrac{x^2}{\sqrt{1+x^2}}\mathrm{d}x = x\sqrt{1+x^2} - \int \dfrac{x^2+1-1}{\sqrt{1+x^2}}\mathrm{d}x \\
    &= x\sqrt{1+x^2} - I + \ln|x+\sqrt{1+x^2}| \\
    &\implies I = \dfrac{1}{2}(x\sqrt{1+x^2} + \ln|x+\sqrt{1+x^2}|) + C
    \end{aligned}
    $$

    **类题2**：请思考如何计算积分

    $$
    I_{n}=\int\sec^{n}x\mathrm{d}x(n\geq3)
    $$
    
    **解：**

    $$
    \begin{aligned}
    I_n &= \int \sec^{n-2}x \mathrm{d}(\tan x) = \tan x \sec^{n-2}x - (n-2)\int \tan^2 x \sec^{n-2}x \mathrm{d}x \\
    &= \tan x \sec^{n-2}x - (n-2)\int (\sec^2 x - 1)\sec^{n-2}x \mathrm{d}x \\
    &= \tan x \sec^{n-2}x - (n-2)(I_n - I_{n-2}) \\
    &\implies I_n = \dfrac{1}{n-1}\tan x \sec^{n-2}x + \dfrac{n-2}{n-1}I_{n-2}
    \end{aligned}
    $$

    其中 \(I_1 = \ln|\sec x + \tan x| + C, I_2 = \tan x + C\)

    Hint：分奇偶，直接凑，很简单；\(I_{2n + 1}\)的计算方法和\(I_{2n - 1}\)类似，也是“分部积分 + 积分重现”，然后得到\(I_{2n + 1}\)和\(I_{2n - 1}\)之间的递推关系。大家可以利用这个思想去计算一下\(\displaystyle\int\sec^{4}x\mathrm{d}x\)，\(\displaystyle\int\sec^{5}x\mathrm{d}x\)）

    **类题3**：
    请推导出积分

    $$
    I_{n}=\int\tan^{n}x\mathrm{d}x(n\geq2)
    $$

    的递推公式
    
    **解：**

    $$
    I_n = \int \tan^{n-2}x(\tan^2 x + 1 - 1)\mathrm{d}x = \int \tan^{n-2}x \sec^2 x \mathrm{d}x - I_{n-2} = \dfrac{1}{n-1}\tan^{n-1}x - I_{n-2}
    $$
    
    其中 \(I_0 = x + C, I_1 = -\ln|\cos x| + C\)


    **类题4**：
    请推导出积分

    $$
    I_{n}=\int\sin^{n}x\mathrm{d}x(n\geq2)
    $$

    的递推公式
    
    **解：**

    $$
    \begin{aligned}
    I_n - I_{n-2} &= \int \sin^n x - \sin^{n-2}x \mathrm{d}x = \int \sin^{n-2}x (\sin^2 x - 1)\mathrm{d}x = -\int \sin^{n-2}x \cos^2 x \mathrm{d}x \\
    &= -\dfrac{1}{n-1}\int \cos x \mathrm{d}(\sin^{n-1}x) = -\dfrac{1}{n-1}\left(\cos x \sin^{n-1}x + \int \sin^{n-1}x \sin x \mathrm{d}x\right) \\
    &= -\dfrac{1}{n-1}\cos x \sin^{n-1}x - \dfrac{1}{n-1}I_n \\
    &\implies I_n = -\dfrac{1}{n}\sin^{n-1}x \cos x + \dfrac{n-1}{n}I_{n-2}
    \end{aligned}
    $$

    其中 \(I_1 = -\cos x + C, I_0 = x + C\)

    **类题5**：根据类题4的结论，可推导出定积分中大名鼎鼎的“点火公式”——

    $$
    I_{n}=\int_{0}^{\frac{\pi}{2}}\sin^{n}x\mathrm{d}x=\begin{cases}\frac{n - 1}{n}\cdot\frac{n - 3}{n - 2}\cdots\frac{2}{3},&n为奇数\\\frac{n - 1}{n}\cdot\frac{n - 3}{n - 2}\cdots\frac{1}{2}\cdot\frac{\pi}{2},&n为偶数\end{cases}
    $$


#### \(R(-\sin x,\cos x)=-R(\sin x,\cos x)\)

注：这种情况和上面的情形类似，所以只用两个简单的例子作为说明即可。


**例题7**：

$$
\int\frac{1}{\sin x\cdot\cos^{2}x}\mathrm{d}x
$$

**解：**

$$
I = \int\dfrac{-\mathrm{d}(\cos x)}{(1-\cos^2 x)\cos^2 x}
$$

**例题8**：

$$
\int\frac{5 + 4\cos x}{(2 + \cos x)^{2}\cdot\sin x}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= -\int \dfrac{5+4\cos x}{(2+\cos x)^2(1-\cos^2 x)}\mathrm{d}(\cos x) = -\int \dfrac{5+4u}{(2+u)^2(1-u)(1+u)}\mathrm{d}u \\
&= \dfrac{1}{2}\ln\left|\dfrac{\cos x - 1}{\cos x + 1}\right| + \dfrac{1}{2+\cos x} + C
\end{aligned}
$$

#### $R(-\sin x,-\cos x) = R(\sin x, \cos x)$

想办法创造出$\sec^2\mathrm{d}x$, 凑出$\text{dtan}x$

我们 有时候喜欢分子分母同时除以 $\cos ^{2} x$ ,使分子出现$\sec^2\mathrm{d}x$,就是这个原因｡

**例题9**: 

$$
\int \frac{1}{1+\cos ^{2} x} \text{d} x
$$

**解：**

$$
I = \int \dfrac{1}{\sin^2 x + 2\cos^2 x}\mathrm{d}x = \int \dfrac{1}{\tan^2 x + 2}\mathrm{d}(\tan x) = \dfrac{1}{\sqrt{2}}\arctan\dfrac{\tan x}{\sqrt{2}} + C
$$

**例题10**:

$$
\int \frac{1}{(3 \sin x+2 \cos x)^{2}}\text{d}x
$$

**解：**

$$
I = \int \dfrac{\sec^2 x}{(3\tan x + 2)^2}\mathrm{d}x = \dfrac{1}{3}\int \dfrac{1}{(3\tan x + 2)^2}\mathrm{d}(3\tan x + 2) = -\dfrac{1}{3(3\tan x + 2)} + C
$$

**例题11**: 

$$
\int \frac{1}{a^{2} \sin ^{2} x+b^{2} \cos ^{2} x} \text{d}x
$$

**解：**
当 \(a \neq 0, b \neq 0\) 时，

$$
I = \int \dfrac{1}{a^2 \tan^2 x + b^2}\mathrm{d}(\tan x) = \dfrac{1}{ab}\arctan\left(\dfrac{a}{b}\tan x\right) + C
$$

**例题12**: 

$$
\int \frac{1}{\sin ^{4} x \cdot \cos ^{2} x} \text{d}x
$$

**解：**

$$
\begin{aligned}
I &= \int \frac{1}{\sin^4 x \cdot \cos^2 x} \mathrm{d}x \\
&= \int \frac{(\sec^2 x)^2}{\tan^4 x} \cdot \sec^2 x \mathrm{d}x \\
&= \int \frac{(1 + \tan^2 x)^2}{\tan^4 x} \mathrm{d}(\tan x)
\end{aligned}
$$

!!! Note
    注:如果把被积函数中的分子分母颠倒,改为 $\displaystyle\int \sin ^{4} x \cdot \cos ^{2} x \mathrm{d}x$ 后,虽然也可以凑 ,但后续操作并不容易(当然,也能做);
    
    但是若能灵活地使用二倍角公式,变为 $\displaystyle\int \sin ^{4} x \cdot \cos ^{2} x ~d x=\dfrac{1}{4} \displaystyle\int \sin ^{2} 2 x \cdot \dfrac{1-\cos 2x}{2}\text{d}x$ , 则后续操作会容易很多｡这再一次体现了不定积分特别容易出现一题多解的情况,希望大家具体问题具体分析｡ 


#### 对于形如\(\displaystyle\int\dfrac{A\sin x + B\cos x}{C\sin x + D\cos x}\)的积分

我们一般假设“分子 = \(p\)分母 + \(q\)（分母）'”，解出\(p\)和\(q\)即可。
  
**例题14**：

$$
\int\frac{\cos x}{\sin x + \cos x}\mathrm{d}x
$$

**解：**

$$
I = \int \dfrac{\frac{1}{2}(\sin x + \cos x) + \frac{1}{2}(\cos x - \sin x)}{\sin x + \cos x}\mathrm{d}x = \dfrac{x}{2} + \dfrac{1}{2}\ln|\sin x + \cos x| + C
$$

#### 当被积函数中出现不同角度的三角函数时

我们一般先用倍角公式统一角度。


**例题15**：

$$
\int\frac{1}{\sin x\cdot\sin 2x}\mathrm{d}x
$$

**解：**

$$
I = \dfrac{1}{2}\int \dfrac{1}{\sin^2 x \cos x}\mathrm{d}x = -\dfrac{1}{2}\sec x \cot x + \dfrac{1}{2}\ln|\sec x + \tan x| + C
$$

**例题16**：

$$
\int\frac{\cos 2x - \sin 2x}{\sin x + \cos x}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\cos^2 x - \sin^2 x - 2\sin x \cos x}{\sin x + \cos x}\mathrm{d}x = \int \left(\cos x - \sin x + \dfrac{1-(\sin x + \cos x)^2}{\sin x + \cos x}\right)\mathrm{d}x \\
&= 2\cos x + \int \dfrac{1}{\sqrt{2}\sin(x+\frac{\pi}{4})}\mathrm{d}x = 2\cos x + \dfrac{1}{\sqrt{2}}\ln\left|\csc(x+\frac{\pi}{4}) - \cot(x+\frac{\pi}{4})\right| + C
\end{aligned}
$$

!!! Tip

    $$
    \int\dfrac{\sin x\cos x}{\sin x+\cos x}\mathrm{d}x
    $$

    的求解，利用$(\sin x+\cos x)^2 = 1 + 2\sin x\cos x$

#### 对于形如\(\int\sin ax\sin bx(a\neq b)\)之类的题

我们可以直接采用积化和差公式，一步秒杀

**例题17**：

$$
\int\sin 2x\cdot\sin 3x\mathrm{d}x
$$

**解：**

$$
I = \dfrac{1}{2}\int (\cos x - \cos 5x)\mathrm{d}x = \dfrac{1}{2}\sin x - \dfrac{1}{10}\sin 5x + C
$$

#### 有些题，具体问题具体分析

这是最核心的思想。


**例题18-1**：

$$
\int\frac{\sin x\cos x}{\sin x + \cos x}\mathrm{d}x
$$

**解：**

$$
\begin{aligned}
I &= \dfrac{1}{2}\int \dfrac{(\sin x + \cos x)^2 - 1}{\sin x + \cos x}\mathrm{d}x = \dfrac{1}{2}\int (\sin x + \cos x)\mathrm{d}x - \dfrac{1}{2}\int \dfrac{1}{\sin x + \cos x}\mathrm{d}x \\
&= \dfrac{1}{2}(\sin x - \cos x) - \dfrac{1}{2\sqrt{2}}\ln\left|\csc(x+\frac{\pi}{4}) - \cot(x+\frac{\pi}{4})\right| + C
\end{aligned}
$$


**例题18-2**：

$$
\int\frac{\sin x\cos x}{\sin x - \cos x}\mathrm{d}x
$$


**例题19**：

$$
\int\frac{\sin x\cdot\cos x}{\sin^{4}x + \cos^{4}x}\mathrm{d}x
$$

> 分母配方降次$(\sin^2x+\cos^2x)^2-2\sin^2x\cos^2x$
$$
\int\frac{\sin x\cdot\cos x}{\sin^{4}x + \cos^{4}x}\mathrm{d}x = \int\frac{\sin(2x)}{1 + \cos^2(2x)}\mathrm{d}x
$$

**解：**

$$
I = \int \dfrac{\tan x \sec^2 x}{\tan^4 x + 1}\mathrm{d}x = \dfrac{1}{2}\int \dfrac{\mathrm{d}(\tan^2 x)}{\tan^4 x + 1} = \dfrac{1}{2}\arctan(\tan^2 x) + C
$$


**例题20**：

$$
\int\dfrac{1}{\sin^6x + \cos^6x}\mathrm{d}x
$$

> 立方差，配方

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\sec^6 x}{\tan^6 x + 1}\mathrm{d}x = \int \dfrac{(\tan^2 x + 1)^2}{\tan^6 x + 1}\mathrm{d}(\tan x) = \int \dfrac{\tan^4 x + 1 - \tan^2 x + 3\tan^2 x}{\tan^6 x + 1}\mathrm{d}(\tan x) \\
&= \int \dfrac{1}{\tan^2 x + 1}\mathrm{d}(\tan x) + \int \dfrac{3\tan^2 x}{(\tan^3 x)^2 + 1}\mathrm{d}(\tan x) \\
&= x + \arctan(\tan^3 x) + C
\end{aligned}
$$

**例题 20**：

$$
\int\dfrac{1}{\sin^6x + \cos^6x}\mathrm{d}x
$$

**解：** 先利用立方和公式、倍角公式，原积分转化为：

$$
\begin{aligned}
I &= \int \dfrac{4}{4 - 3\sin^2 2x}\mathrm{d}x
\end{aligned}
$$

分子分母同时除以 \(\cos^2 2x\)，将积分化为关于 \(\tan 2x\) 的形式：

$$
\begin{aligned}
I &= \int \dfrac{4\sec^2 2x}{4\sec^2 2x - 3\tan^2 2x}\mathrm{d}x \\
&= \int \dfrac{4\sec^2 2x}{4(1 + \tan^2 2x) - 3\tan^2 2x}\mathrm{d}x \\
&= \int \dfrac{4\sec^2 2x}{\tan^2 2x + 4}\mathrm{d}x
\end{aligned}
$$

令 \(u = \tan 2x\)，则 \(\mathrm{d}u = 2\sec^2 2x \mathrm{d}x\)，即 \(4\sec^2 2x \mathrm{d}x = 2\mathrm{d}u\)，代入得：

$$
\begin{aligned}
I &= \int \dfrac{2}{u^2 + 2^2}\mathrm{d}u \\
&= 2 \cdot \dfrac{1}{2}\arctan\dfrac{u}{2} + C \\
&= \arctan\left(\dfrac{\tan 2x}{2}\right) + C
\end{aligned}
$$

**例题21**：

$$
\int\frac{1}{\sin^{3}x + \cos^{3}x}\mathrm{d}x
$$

> 注：本题涉及到了三角有理函数的裂项，它们没有通法（或许是我不知道），只有观察式子结构，不断尝试，类似的还有下面这道题。

**解：**

$$
\begin{aligned}
I &= \int \dfrac{1}{(\sin x + \cos x)(\sin^2 x + \cos^2 x - \sin x \cos x)}\mathrm{d}x \\
&= \dfrac{1}{3}\int \dfrac{(\sin x + \cos x)^2 + 2(1-\sin x \cos x)}{(\sin x + \cos x)(1-\sin x \cos x)}\mathrm{d}x \\
&= \dfrac{1}{3}\int \dfrac{\sin x + \cos x}{1-\sin x \cos x}\mathrm{d}x + \dfrac{2}{3}\int \dfrac{1}{\sin x + \cos x}\mathrm{d}x \\
&= \dfrac{2}{3}\arctan(\sin x - \cos x) + \dfrac{\sqrt{2}}{3}\ln\left|\csc(x+\frac{\pi}{4}) - \cot(x+\frac{\pi}{4})\right| + C
\end{aligned}
$$


例题22

$$
\int\frac{1}{\sin(x + a)\sin(x + b)}\mathrm{d}x(\sin(a - b)\neq0)
$$

**解：**

$$
\begin{aligned}
I &= \int \dfrac{\sin[x+a-(x+b)]}{\sin(a-b)\sin(x+a)\sin(x+b)}\mathrm{d}x = \int \dfrac{\sin(x+a)\cos(x+b) - \cos(x+a)\sin(x+b)}{\sin(a-b)\sin(x+a)\sin(x+b)}\mathrm{d}x \\
&= \dfrac{1}{\sin(a-b)}\ln\left|\dfrac{\sin(x+b)}{\sin(x+a)}\right| + C
\end{aligned}
$$