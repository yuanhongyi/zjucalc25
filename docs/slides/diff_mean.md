# 微分中值定理

## 定理梳理与证明

### 费马引理

设 $x_0$ 是函数 $f$ 的极值点, 并且 $f$ 在 $x_0$ 处可微, 则:

$$ f'(x_0) = 0 $$

!!! Tips
    **证明：**

    根据定义，存在 $x_0$ 的一个邻域，对该邻域内的任意 $x$，都有 $f(x) \le f(x_0)$。

    因此，当 $x > x_0$ 时，$\dfrac{f(x)-f(x_0)}{x-x_0} \le 0$；而当 $x < x_0$ 时，$\dfrac{f(x)-f(x_0)}{x-x_0} \ge 0$。

    由极限的保号性可知 $f'_+(x_0) = \lim\limits_{x \to x_0^+} \dfrac{f(x)-f(x_0)}{x-x_0} \le 0$，$f'_-(x_0) = \lim\limits_{x \to x_0^-} \dfrac{f(x)-f(x_0)}{x-x_0} \ge 0$。

    所以$f'(x_0)=0$

### 罗尔(Rolle)定理

设 $f(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, 且 $f(a) = f(b)$, 则 $\exists \xi \in (a,b)$, 使得 $f'(\xi)=0$.

!!! Tips
    **证明:** 分类讨论

    (i) $f=C, \Rightarrow f'(\xi)=0, \forall \xi \in (a,b)$

    (ii) 不妨 $\exists x_0$ 满足 $f(x_0) < f(a) = f(b)$, 则 $f(x)$ 存在最小值, $f'(\xi)=0$.

### 拉格朗日中值定理

设 $f(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, $\exists \xi \in (a,b)$, 使得:

$$ f'(\xi) = \frac{f(b)-f(a)}{b-a} \quad \text{或者} \quad f(b)-f(a) = f'(\xi)(b-a) $$

!!! Tips
    **证明:** 设 $k = \dfrac{f(b)-f(a)}{b-a} \iff$ 证明 $f'(\xi)=k$.

    由上式得: $f(b)-f(a)-k(b-a)=0$.

    设 $F(x) = f(x) - f(a) - k(x-a) \Rightarrow F(b)=F(a)=0$.

    由罗尔定理: $\exists \xi \in (a,b), F'(\xi)=0 \iff f'(\xi)=k$.


### 柯西中值定理

设 $f(x), g(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, 且 $g'(x) \neq 0$, 则 $\exists \xi \in (a,b)$, 使得:

$$ \frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(\xi)}{g'(\xi)} $$


!!! Tips
    **证明:** 设 $k = \dfrac{f(b)-f(a)}{g(b)-g(a)} \Rightarrow f(b)-f(a)-k(g(b)-g(a))=0$.

    设 $F(x) = f(x)-f(a)-k(g(x)-g(a)) \Rightarrow F(a)=F(b)=0$.

    由罗尔定理: $\exists \xi \in (a,b), F'(\xi)=0 \iff \dfrac{f'(\xi)}{g'(\xi)} = k = \dfrac{f(b)-f(a)}{g(b)-g(a)}$.


## 例题

仅梳理期中考可能考的问题，后续再对期末考可能考的进行深挖。

### 构造函数

**14.已知$f(x)$在$[0,1]$上连续，在$(0,1)$上可导，$f(0) = f(1) = 0$，$f(\dfrac{1}{2}) = 1$. 证明：**

**$(1)\exist\varepsilon\in(\dfrac{1}{2},1)$,使得$f(\varepsilon) = \varepsilon$**

**$(2)\forall\gamma\in\R, \exist\rho\in(0,\varepsilon)$,使得$f'(\rho)-\gamma(f(\rho)-\rho) = 1$**


(1)即证$g(x) = f(x)-x$在$(\dfrac{1}{2},1)$上存在零点，略


(2)

$h(x) = e^{-\gamma x}(f(x)-x)$

$h'(x) = e^{-\gamma x}(f'(x)-1-\gamma(f(x)-x))$

对$h(x)$使用罗尔定理即证

---


### 双中值问题

关键在于确定区间内的(某些)中间点c

**24.13. 已知函数 $f(x)$ 在 $[0,1]$ 上连续, 在 $(0,1)$ 内可导, 且$f(0)=0, f(1)=1$。证明:**

**(1) 存在 $c \in (0,1)$, 使得 $f(c)=1-c$;**

**(2) 存在两个不同的数 $\xi, \eta \in (0,1)$, 使得 $f'(\xi)f'(\eta)=1$.**

(1)略

(2)在$[0,c], [c,1]$上分别使用拉格朗日中值定理：

存在$\xi\in(0,c)$使$f(c)-f(0) = f(c) = 1-c = f'(\xi)c$

存在$\eta\in(c,1)$使$f(1)-f(c) = 1-f(c) = c = f'(\eta)(1-c)$

相乘即证

---

**23.12. 设 $f(x)$ 在 $[0,1]$ 上连续，在 $(0, 1)$ 内可导，且 $f(0) = 0, f(1) = 1$.证明：**

**(1) $\exists c \in (0, 1)$ 使得 $f(c) = \dfrac{3}{2023}$;**

**(2) $\exists \xi \ne \eta \in (0, 1)$ 使得 $\dfrac{3}{f'(\xi)} + \dfrac{2020}{f'(\eta)} = 2023$.**


**(1)** 令 $g(x) = f(x) - \dfrac{3}{2023}$, 则 $g(0) = f(0) - \dfrac{3}{2023} = -\dfrac{3}{2023} < 0$.

$g(1) = f(1) - \dfrac{3}{2023} = 1 - \dfrac{3}{2023} > 0$, 则有 $g(0)g(1)<0$.

由零点存在定理, $\exists c \in (0,1)$ 使 $g(c)=0$.

即此时有 $f(c) - \dfrac{3}{2023} = 0$, 也即 $f(c) = \dfrac{3}{2023}$.

**(2)** 由拉格朗日中值定理,

$\exists \xi \in (0,c)$ 使 $f'(\xi) = \dfrac{f(c)-f(0)}{c-0} = \dfrac{3}{2023c}$.

$\exists \eta \in (c,1)$ 使 $f'(\eta) = \dfrac{f(1)-f(c)}{1-c} = \dfrac{1-3/2023}{1-c} = \dfrac{2020}{2023(1-c)}$.

则 $\dfrac{3}{f'(\xi)} = 2023c$, $\dfrac{2020}{f'(\eta)} = 2023(1-c)$.

因此 $\exists \xi \neq \eta \in (0,1)$, 使 $\dfrac{3}{f'(\xi)} + \dfrac{2020}{f'(\eta)} = 2023c + 2023(1-c) = 2023$ 成立.

---

设函数 $f(x)$ 在 $[0,1]$ 上连续，在 $(0,1)$ 内可导，且 $f(0)=0, f(1)=\dfrac{1}{2}$。证明：$\exists\xi, \eta \in (0, 1)$（$\xi \neq \eta$），使得
$$ f'(\xi) + f'(\eta) = \xi + \eta $$

令 $F(x) = f(x) - \dfrac{1}{2}x^2$，则 $F(x)$ 在 $[0,1]$ 上连续，在 $(0, 1)$ 内可导，且 $F'(x) = f'(x) - x$。
已知 $F(0) = f(0) - 0 = 0$， $F(1) = f(1) - \dfrac{1}{2} = \dfrac{1}{2} - \dfrac{1}{2} = 0$。

对 $F(x)$ 在区间 $[0, \dfrac{1}{2}]$ 和 $[\dfrac{1}{2}, 1]$ 上分别应用拉格朗日中值定理：

存在 $\xi \in (0, \dfrac{1}{2})$，使得$F'(\xi) = \dfrac{F(\frac{1}{2}) - F(0)}{\frac{1}{2} - 0} = 2F(\frac{1}{2})$

存在 $\eta \in (\frac{1}{2}, 1)$，使得$F'(\eta) = \dfrac{F(1) - F(\frac{1}{2})}{1 - \frac{1}{2}} = \dfrac{0 - F(\frac{1}{2})}{\frac{1}{2}} = -2F(\frac{1}{2})$

将以上两式相加，得：

$$ F'(\xi) + F'(\eta) = 2F(\frac{1}{2}) - 2F(\frac{1}{2}) = 0 $$

整理得：

$$ f'(\xi) + f'(\eta) = \xi + \eta $$


---

**例题 3** $f(x) \in C$，在 $(0, 1)$ 可导， $f(0)=0, f(1)=\dfrac{1}{4}$

证：$\exists\ \xi \neq \eta$, s.t. $f'(\xi) + f'(\eta) = \eta - \xi$


**证明**

> 将待证等式变形为 $f'(\xi) + \xi = \eta - f'(\eta)$。这提示我们构造两个不同的辅助函数。

令 $h(x) = f(x) + \dfrac{1}{2}x^2$ 且 $g(x) = f(x) - \dfrac{1}{2}x^2$。

则 $h'(x) = f'(x) + x$ 且 $g'(x) = f'(x) - x$。

待证等式可进一步化为 $h'(\xi) = -g'(\eta)$。

我们将区间 $[0,1]$ 拆分为 $[0, \dfrac{1}{2}]$ 和 $[\dfrac{1}{2}, 1]$，并应用拉格朗日中值定理：

对函数 $h(x)$ 在区间 $[0, \dfrac{1}{2}]$ 上应用拉格朗日中值定理，存在 $\xi \in (0, \dfrac{1}{2})$，使得：

$$ h'(\xi) = \frac{h(\frac{1}{2}) - h(0)}{\frac{1}{2} - 0} = \frac{(f(\frac{1}{2}) + \frac{1}{2}(\frac{1}{2})^2) - (f(0) + 0)}{\frac{1}{2}} = 2f(\frac{1}{2}) + \frac{1}{4} $$

对函数 $g(x)$ 在区间 $[\frac{1}{2}, 1]$ 上应用拉格朗日中值定理，存在 $\eta \in (\dfrac{1}{2}, 1)$，使得：

$$ g'(\eta) = \frac{g(1) - g(\frac{1}{2})}{1 - \frac{1}{2}} = \frac{(f(1) - \frac{1}{2}(1)^2) - (f(\frac{1}{2}) - \frac{1}{2}(\frac{1}{2})^2)}{\frac{1}{2}} = \frac{(\frac{1}{4} - \frac{1}{2}) - (f(\frac{1}{2}) - \frac{1}{8})}{\frac{1}{2}} = \frac{-\frac{1}{8} - f(\frac{1}{2})}{\frac{1}{2}} = -2f(\frac{1}{2}) - \frac{1}{4} $$


即

$$ f'(\xi) + \xi = - (f'(\eta) - \eta) = \eta - f'(\eta) $$
整理得：
$$ f'(\xi) + f'(\eta) = \eta - \xi $$

---


### 双中值问题2


设函数 $f(x)$ 在 $[a, b]$ 连续 ($a>0$)，在 $(a, b)$ 内可导，证明存在 $ξ, η ∈ (a, b)$，使得：

$$ f'(ξ) = \frac{a+b}{2η}f'(η) $$


证明：

设 $g(x) = x^2$，由柯西中值定理，$\exists\ \eta \in (a, b)$，使得：

$$ \frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f(b)-f(a)}{b^2-a^2} = \frac{f'(η)}{g'(η)} = \frac{f'(η)}{2η} $$

由拉格朗日中值定理，$\exists\ \xi \in (a, b)$，使得：

$$ \frac{f(b)-f(a)}{b-a} = f'(ξ) $$

将柯西中值定理的结论进行变形：

$$ \frac{f(b)-f(a)}{b-a} \cdot \frac{1}{a+b} = \frac{f'(η)}{2η} $$

将拉格朗日中值定理的结论代入上式：

$$ f'(ξ) \cdot \frac{1}{a+b} = \frac{f'(η)}{2η} $$

所以，

$$ f'(ξ) = \frac{a+b}{2η}f'(η) $$


---


设函数 $f(x)$ 在闭区间 $[a, b]$ 上连续，在开区间 $(a, b)$ 可导。又 $b > a > 0$。证明：存在 $\xi, \eta \in (a, b)$，使得

$$ f'(\xi) = \eta f'(\eta) \frac{\ln(\frac{b}{a})}{b-a} $$


**证明**

设 $g(x) = \ln x$，在闭区间 $[a, b]$ 上连续，在开区间 $(a, b)$ 可导。

根据柯西中值定理，$\exists\ \eta \in (a, b)$，使得

$$ \frac{f(b) - f(a)}{g(b) - g(a)} = \frac{f(b) - f(a)}{\ln b - \ln a} = \frac{f'(\eta)}{g'(\eta)} = \frac{f'(\eta)}{\frac{1}{\eta}} = \eta f'(\eta) $$

根据拉格朗日中值定理，$\exists\ \xi \in (a, b)$，使得

$$ \frac{f(b) - f(a)}{b-a} = f'(\xi) $$

相除得：

$$ \frac{f'(\xi)}{\eta f'(\eta)} = \frac{\frac{f(b) - f(a)}{b-a}}{\frac{f(b) - f(a)}{\ln b - \ln a}} = \frac{\ln b - \ln a}{b-a} $$

即：

$$ f'(\xi) = \eta f'(\eta) \frac{\ln(\frac{b}{a})}{b-a} $$

---

### k值问题

设$f$在$[a,b]$上连续, 在$(a,b)$上二阶可导，证明：存在$\eta\in(a,b)$,有：

$$
f(b) +f(a) -2f(\dfrac{a+b}{2})  = \dfrac{(b-a)^2}{4}f''(\eta)
$$

设$k = \dfrac{f(b) +f(a) -2f(\dfrac{a+b}{2})}{\dfrac{(b-a)^2}{4}}$

$\Rightarrow f(b) +f(a) -2f(\dfrac{a+b}{2})-\dfrac{(b-a)^2}{4}k = 0$

$F(x) = f(x)+f(a)-2f(\dfrac{x+a}{2})-\dfrac{k(x-a)^2}{4}$

$F(a) = F(b) = 0\Rightarrow F'(x_1) = 0(Rolle)$

$F'(x_1) = f'(x_1)-f'(\dfrac{x+a}{2})-k\dfrac{x_1-a}{2} = 0$

$\Rightarrow k = \dfrac{f'(x_1)-f'(\dfrac{x_1+a}{2})}{\dfrac{x_1-a}{2}} = f''(\eta)(Lagrange)$

即$f(b) +f(a) -2f(\dfrac{a+b}{2})  = \dfrac{(b-a)^2}{4}f''(\eta)$

---

### 其他

设$f(x)$在$[0,2]$上可导，且$f(0) = f(2) = 0，M = \max\limits_{x\in[0,2]}\{|f(x)|\}$，证明: $\exist\xi\in(0,2),|f'(\xi)|\ge M$

证: 设$|f(c)| = M$

(1)若$c\in(0,1],M = |f(c)| = |f(c)-f(0)| = c|f'(\xi)|$

则$|f'(\xi)| = \dfrac{M}{c}\ge M(c\in(0,1))$

(2)若$c\in(1,2),M = |f(c)| = |f(2)-f(c)| = (2-c)|f'(\xi)|$

则$|f'(\xi)| = \dfrac{M}{2-c}\ge M$


(3)若$c = 0或2, M = 0, f\equiv 0, f'\equiv0, 显然成立$ 
