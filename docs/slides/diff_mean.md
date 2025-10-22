### **微分中值定理**

**费马引理**

设 $x_0$ 是函数 $f$ 的极值点, 并且 $f$ 在 $x_0$ 处可微, 则:

$$ f'(x_0) = 0 $$

**罗尔定理**

设 $f(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, 且 $f(a) = f(b)$, 则 $\exists \xi \in (a,b)$, 使得 $f'(\xi)=0$.

> **证明:**

> (i) $f=C, \Rightarrow f'(\xi)=0, \forall \xi \in (a,b)$

> (ii) 不妨 $\exists x_0$ 满足 $f(x_0) < f(a) = f(b)$, 则 $f(x)$ 存在最小值, $f'(\xi)=0$.

**拉格朗日中值定理**

设 $f(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, $\exists \xi \in (a,b)$, 使得:

$$ f'(\xi) = \frac{f(b)-f(a)}{b-a} \quad \text{或者} \quad f(b)-f(a) = f'(\xi)(b-a) $$

> **证明:** 设 $k = \frac{f(b)-f(a)}{b-a} \iff$ 证明 $f'(\xi)=k$.

> 由上式得: $f(b)-f(a)-k(b-a)=0$.

> 设 $F(x) = f(x) - f(a) - k(x-a) \Rightarrow F(b)=F(a)=0$.

> 由罗尔定理: $\exists \xi \in (a,b), F'(\xi)=0 \iff f'(\xi)=k$.


**柯西中值定理**

设 $f(x), g(x)$ 在 $[a,b]$ 上连续, 在 $(a,b)$ 上可导, 且 $g'(x) \neq 0$, 则 $\exists \xi \in (a,b)$, 使得:

$$ \frac{f(b)-f(a)}{g(b)-g(a)} = \frac{f'(\xi)}{g'(\xi)} $$

> **证明:** 设 $k = \frac{f(b)-f(a)}{g(b)-g(a)} \Rightarrow f(b)-f(a)-k(g(b)-g(a))=0$.

> 设 $F(x) = f(x)-f(a)-k(g(x)-g(a)) \Rightarrow F(a)=F(b)=0$.

> $\therefore \exists \xi \in (a,b), F'(\xi)=0 \iff \frac{f'(\xi)}{g'(\xi)} = k = \frac{f(b)-f(a)}{g(b)-g(a)}$.