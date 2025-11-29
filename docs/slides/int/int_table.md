# 不定积分表

## 背景补充

### 双曲正弦函数

$y = \sinh x = \dfrac{e^x - e^{-x}}{2}$

反函数

$y = \ln(x + \sqrt{x^2 + 1})$

### 双曲余弦函数

$y = \cosh x = \dfrac{e^x + e^{-x}}{2}$

反函数

$y = \ln(x + \sqrt{x^2 - 1})$

### 双曲正切函数

$y = \tanh x = \dfrac{\sinh x}{\cosh x} = \dfrac{e^x - e^{-x}}{e^x + e^{-x}}$

反函数

$y = \dfrac{1}{2}\ln\dfrac{1 + x}{1 - x}$

---

为何叫双曲三角函数呢，是因为他们跟三角函数有类似的性质，甚至存在双曲三角函数线，有兴趣的同学可以参考知乎的两篇文章


[三角函数的孪生兄弟，双曲函数](https://zhuanlan.zhihu.com/p/398460302)

[双曲函数的一些公式](https://zhuanlan.zhihu.com/p/338449318)

了解了双曲三角函数以后，一些不定积分公式也容易理解了

1.$\displaystyle\int k \, \mathrm{d}x = kx + C$

2.$\displaystyle\int x^\alpha \, \mathrm{d}x = \frac{x^{\alpha+1}}{\alpha+1} + C \quad (\alpha \neq -1)$

3.$\displaystyle\int \frac{1}{x} \, \mathrm{d}x = \ln|x| + C$

4.$\displaystyle\int \frac{\mathrm{d}x}{1+x^2} = \arctan x + C$

5.$\displaystyle\int \frac{\mathrm{d}x}{\sqrt{1-x^2}} = \arcsin x + C$

6.$\displaystyle\int \cos x \, \mathrm{d}x = \sin x + C$

7.$\displaystyle\int \sin x \, \mathrm{d}x = -\cos x + C$

8.$\displaystyle\int \frac{\mathrm{d}x}{\cos^2 x} = \tan x + C$

9.$\displaystyle\int \frac{\mathrm{d}x}{\sin^2 x} = -\cot x + C$

10.$\displaystyle\int \sec x \tan x \, \mathrm{d}x = \sec x + C$

11.$\displaystyle\int \csc x \cot x \, \mathrm{d}x = -\csc x + C$

12.$\displaystyle\int a^x \, \mathrm{d}x = \frac{a^x}{\ln a} + C$

13.$\displaystyle\int \sinh x \, \mathrm{d}x = \cosh x + C$

14.$\displaystyle\int \cosh x \, \mathrm{d}x = \sinh x + C$

15.$\displaystyle\int \tan x \, \mathrm{d}x = -\ln|\cos x| + C$

16.$\displaystyle\int \cot x \, \mathrm{d}x = \ln|\sin x| + C$

17.$\displaystyle\int \sec x \, \mathrm{d}x = \ln|\sec x + \tan x| + C$

18.$\displaystyle\int \csc x \, \mathrm{d}x = \ln|\csc x - \cot x| + C$

19.$\displaystyle\int \frac{\mathrm{d}x}{a^2+x^2} = \frac{1}{a} \arctan \frac{x}{a} + C$

20.$\displaystyle\int \frac{\mathrm{d}x}{a^2-x^2} = \frac{1}{2a} \ln \left| \frac{x+a}{a-x} \right| + C$

21.$\displaystyle\int \frac{\mathrm{d}x}{\sqrt{a^2-x^2}} = \arcsin \frac{x}{a} + C$

22.$\displaystyle\int \frac{\mathrm{d}x}{\sqrt{a^2+x^2}} = \ln \left( x + \sqrt{x^2+a^2} \right) + C$

23.$\displaystyle\int \frac{\mathrm{d}x}{\sqrt{x^2-a^2}} = \ln \left| x + \sqrt{x^2-a^2} \right| + C$

24.$\displaystyle\int \sqrt{a^2-x^2} \, \mathrm{d}x = \frac{1}{2} \left( x\sqrt{a^2-x^2} + a^2 \arcsin \frac{x}{a} \right) + C$

25.$\displaystyle\int \sqrt{x^2 \pm a^2} \, \mathrm{d}x = \frac{1}{2} \left( x\sqrt{x^2 \pm a^2} \pm a^2 \ln \left| x \pm \sqrt{x^2 \pm a^2} \right| \right) + C$

26.$\displaystyle\int \frac{\mathrm{d}x}{(a^2+x^2)^2} = \frac{1}{2a^3} \left( \arctan \frac{x}{a} + \frac{ax}{x^2+a^2} \right) + C$

> $\displaystyle\int \frac{\mathrm{d}x}{(1+x^2)^2} = \frac{1}{2} \left( \arctan x + \frac{x}{x^2+1} \right) + C$
> $\displaystyle\int \frac{x^2 \mathrm{d}x}{(1+x^2)^2} = \frac{1}{2} \left( \arctan x - \frac{x}{1+x^2} \right) + C$

27.$\displaystyle\int e^x \sin x \, \mathrm{d}x = \frac{1}{2} e^x (\sin x - \cos x) + C$

28.$\displaystyle\int e^x \cos x \, \mathrm{d}x = \frac{1}{2} e^x (\sin x + \cos x) + C$