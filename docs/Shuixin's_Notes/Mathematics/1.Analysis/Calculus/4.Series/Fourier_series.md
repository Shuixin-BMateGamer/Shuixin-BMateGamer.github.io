# 引入
在学完了[[级数]]后，我们研究特殊级数
除了幂级数之外，还有一种常用的特殊函数项级数——三角级数
想法是这样的，不同周期波叠加（如：$\sin x+3\sin 3x$ ）有可能会得到更加复杂的周期波，那么猜想复杂的周期波或是说周期函数或许能够分解为若干简单的周期函数之和
即周期函数 $f$ 若如下表示：$$f(t)=\sum\limits_{n=0}^{\infty}A_n\sin(n\omega t+\varphi_n)\tag{1}$$
设 $g(t)$ 是周期为 $T$ 的周期函数，由于可以做如下替换：$$g(t)=g(\frac{T}{2\pi}x)\triangleq f(x)$$得到的 $f$ 是周期为 $2\pi$ 的周期函数，因此下面的讨论中讨论这种情况即可

对于周期为 $2\pi$ 的函数，圆频率 $\omega=\frac{2\pi}{T}=1$ ，那么 $(1)$ 就变为形如 $$f(x)=\sum\limits_{n=0}^{\infty}A_n\sin(nx+\varphi_n)\tag{2}$$$A_n\sin(nx+\varphi_n)=A_n\sin nx\cos \varphi_n+A_n\cos nx\sin \varphi_n$ ，
记 $a_n=A_n\sin\varphi_{n},\,b_n=A_n\cos\varphi_n$ , $(n=1,2,...)$ , 而 $a_0=2A_0\sin\varphi_0$ 
则 $(2)$ 式进一步改写为$$f(x)=\frac{a_0}{2}+\sum\limits_{n=1}^\infty(a_{n}\cos nx+b_{n}\sin nx)\tag{3}$$
那么下面要讨论的问题就变为**何时周期为 $2\pi$ 的函数可以展开为形如上面的级数**，需要满足什么条件


# Fourier级数

## 三角函数系

用线性空间的观点研究，下面将线性空间 $\mathfrak R_2([-\pi,\pi],\mathbb{C})$ 记作所有在 $X\subset R^n$ 上的局部可积函数的线性空间，同时这里函数满足模的平方也在 $X$ 上可积
再在空间中定义内积$$\langle f,g\rangle=\int_X(f\cdot\bar{g})(x)\mathrm{d}x$$如此定义合理是因为 $|f\cdot\bar{g}|\leq\frac{|f|^2+|g|^2}{2}$ ，右式收敛，故左边作积分绝对收敛
若只讨论实值函数即为$$\langle f,g\rangle=\int_{X}(f\cdot g)(x)\mathrm{d}x$$
**三角函数的正交性**: 三角函数系 $1,\cos x,\sin x,\cos 2x,\sin 2x,...,\cos nx,\sin nx,...$ 为空间 $\mathfrak R_2([-\pi,\pi],\mathbb{C})$ 中的正交向量组, 即 $$\langle\sin mx,\cos nx\rangle=0\qquad\langle\sin m_1x,\sin m_2x\rangle=0\quad(m_1\neq m_2)\qquad\langle\cos n_1x,\cos n_2x\rangle=0\quad(n_{1}\neq n_2)$$
事实上有 $$\begin{align}\int_{-\pi}^{\pi}\cos mx\cos nx\,\mathrm{d}x&=\pi\delta_{mn}\\\int_{-\pi}^{\pi}\sin mx\sin nx\,\mathrm{d}x&=\pi\delta_{mn}\\\int_{-\pi}^{\pi}\cos mx\sin nx\,\mathrm{d}x&=0\end{align}$$
## Fourier级数

通过三角函数系的性质，若先假定 $(3)$ 式成立，即$$f(x)=\frac{a_0}{2}+\sum\limits_{k=1}^{\infty}(a_{k}\cos kx+b_{k}\sin kx)$$在等式两边同时乘 $\cos nx$ ，再在两边同时积分得到$$\begin{align}\int_{-\pi}^{\pi}f(x)\cos nx\,\mathrm{d}x&=\int_{-\pi}^{\pi}\frac{a_{0}}{2}\cos nx\mathrm{d}x+\sum\limits_{k=1}^{\infty}\bigg(\int_{-\pi}^{\pi}a_{k}\cos kx\cos nx\,\mathrm{d}x+\int_{-\pi}^{\pi}b_{k}\sin kx\cos nx\,\mathrm{d}x\bigg)\\&=\begin{cases}a_0\qquad\qquad&,n=0\\\pi a_n\qquad\qquad&,n\in\mathbb{N^*}\end{cases}\end{align}$$同理可同时乘 $\sin nx$ ，再同时积分得到$$\begin{align}\int_{-\pi}^{\pi}f(x)\sin nx\,\mathrm{d}x&=\int_{-\pi}^{\pi}\frac{a_{0}}{2}\sin nx\mathrm{d}x+\sum\limits_{k=1}^{\infty}\bigg(\int_{-\pi}^{\pi}a_{k}\cos kx\sin nx\,\mathrm{d}x+\int_{-\pi}^{\pi}b_{k}\sin kx\sin nx\,\mathrm{d}x\bigg)\\&=\begin{cases}0\qquad\qquad&,n=0\\\pi b_n\qquad\qquad&,n\in\mathbb{N^*}\end{cases}\end{align}$$由此可得到 $$\begin{cases}a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos nx\,\mathrm{d}x\qquad&(n=0,1,\cdots)\\b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin nx\,\mathrm{d}x\qquad&(n=1,2,\cdots)\end{cases}\tag{4}$$
**定义**: 设 $f\in R[-\pi,\pi]$ , 由公式 $(4)$ 确定的 $a_n,b_n$ 称为 $f$ 的 **Fourier系数**, 由 $a_n,b_n$ 确定的级数 $(3)$ 称为 $f$ 的**Fourier级数**, 记作 $$f\sim\frac{a_0}{2}+\sum\limits_{n=1}^\infty(a_{n}\cos nx+b_{n}\sin nx)$$
**Riemann-Lebesgue引理**: 设 $f$ 在 $[a,b]$ 上绝对可积, 则 $$\begin{align}&\lim_\limits{\lambda\to+\infty}\int_{a}^{b}f(x)\cos \lambda x\,\mathrm{d}x=0\\&\lim_\limits{\lambda\to+\infty}\int_{a}^{b}f(x)\sin \lambda x\,\mathrm{d}x=0\end{align}$$**[证明]**:
	$(a)$ 先证对于连续函数 $\psi(x)$ 成立, 由于 $\psi(x)$ 在 $[a,b]$ 上连续, 故一致连续, 因此
	$\forall\,\varepsilon>0$ , $\exists\,\delta>0$ , $s.t.$ $\forall\,y_1,y_2\in[a,b]$ , 只要 $|y_1-y_2|<\delta$ , 就有 $|\psi(y_1)-\psi(y_2)|<\frac{\varepsilon}{2(b-a)}$
	另一方面, 由连续性可知 $\psi(x)$ 在 $[a,b]$ 上有界, 设 $|\psi(x)|\leq M$ , $x\in[a,b]$
	在 $[a,b]$ 上做分割 $\pi:a=x_0<x_1<\cdots<x_n=b$ , $\Delta x_k=x_k-x_{k-1}$ , $||\pi||<\delta$
	则有 $$\begin{align}\bigg|\int_{a}^{b}\psi(x)\cos\lambda x\,\mathrm{d}x\bigg|&\leq\bigg|\sum\limits_{k=1}^{n}\int_{x_{k-1}}^{x_k}(\psi(x)-\psi(x_{k-1}))\cos\lambda x\,\mathrm{d}x\bigg|+\bigg|\sum\limits_{k=1}^{n}\int_{x_{k-1}}^{x_{k}}\psi(x_{k-1})\cos\lambda x\,\mathrm{d}x\bigg|\\&\leq\sum\limits_{k=1}^{n}\int_{x_{k-1}}^{x_k}|\psi(x)-\psi(x_{k-1})||\cos\lambda x|\,\mathrm{d}x+\frac{|\psi(x_{k-1})||\sin\lambda x_k-\sin\lambda x_{k-1}|}{|\lambda|}\\&\leq\sum\limits_{k=1}^{n}\frac{\varepsilon}{2(b-a)}\Delta x_k+\frac{2M}{|\lambda|}\\&只要\:\lambda>\frac{4M}{\varepsilon},就有\\&\bigg|\int_{a}^{b}\psi(x)\cos\lambda x\,\mathrm{d}x\bigg|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon\end{align}$$这就说明了 $$\lim_\limits{\lambda\to+\infty}\int_{a}^{b}\psi(x)\cos\lambda x\,\mathrm{d}x=0$$
	$(b)$ $[a,b]$ 上的可积函数 $f(x)$ 满足 $\forall\,\varepsilon>0$ , $\exists\,\varphi(x)\in C[a,b]$ , 使得 $\int_{a}^{b}|f(x)-\varphi(x)|\,\mathrm{d}x<\frac{\varepsilon}{2}$
	由于 $\varphi(x)\in C[a,b]$ , 故 $\exists\,A>0$ , $s.t.$ $\lambda>A$ 时, 有 $\bigg|\int_{a}^{b}\varphi(x)\cos\lambda x\mathrm{d}x\bigg|<\frac{\varepsilon}{2}$
    于是	$$\begin{align}\bigg|\int_{a}^{b}f(x)\cos\lambda x\,\mathrm{d}x\bigg|&\leq\bigg|\int_{a}^{b}(f(x)-\varphi(x))\cos\lambda x\mathrm{d}x\bigg|+\bigg|\int_{a}^{b}\varphi(x)\cos\lambda x\mathrm{d}x\bigg|\\&<\int_a^b|f(x)-\varphi(x)|\,\mathrm{d}x+\bigg|\int_{a}^{b}\varphi(x)\cos\lambda x\mathrm{d}x\bigg|\\&<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon\end{align}$$至此, 可知 $$\lim_\limits{\lambda\to+\infty}\int_{a}^{b}f(x)\cos\lambda x\,\mathrm dx=0$$同理也可证 $$\lim_\limits{\lambda\to+\infty}\int_{a}^{b}f(x)\sin\lambda x\,\mathrm dx=0$$对任意的 $f\in R[a,b]$ 成立

**推广**: 上述结论对于 $b=+\infty$ 也成立
**[证明]**:
	(暂略)

由上面的结论可知，$(3)$ 式的三角级数要作为**Fourier级数**的必要条件为 $$\lim_{n\to\infty}a_n=\lim_{n\to\infty}b_n=0$$
下面用一个经典的例子，作为**Riemanna-Lebesgue引理**的一个应用

**Dirichlet积分**: $$\int_{0}^{+\infty}\frac{\sin x}{x}\,\mathrm{d}x=\frac{\pi}{2}$$**[证明]**:
	注意到[[三角恒等式]]$$\frac{1}{2}+\sum\limits_{k=1}^{n}\cos kt=\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}$$在该式两边在 $[0,\pi]$ 上积分得 $$\frac{\pi}{2}=\frac{\pi}{2}+\sum\limits_{k=1}^{n}\int_{0}^{\pi}\cos kt\,\mathrm{d}t=\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}\,\mathrm{d}t$$而又有 $$\begin{align}\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}\,\mathrm{d}t&=\int_{0}^{\pi}\bigg(\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}-\frac{\sin(n+\frac{1}{2})t}{t}\bigg)\,\mathrm{d}t+\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{t}\,\mathrm{d}t\\&={\underbrace{\int_{0}^{\pi}{\color{red}\bigg(\frac{1}{2\sin\frac{t}{2}}-\frac{1}{t}\bigg)}\sin(n+\frac{1}{2})t\,\mathrm{d}t}_{由\mathrm{Riemann}引理可知,该项趋于0}}+\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{t}\,\mathrm{d}t\\\lim_{t\to0}\bigg(\frac{1}{2\sin\frac{t}{2}}-\frac{1}{t}\bigg)=0,\:&故h(t)=\frac{1}{2\sin\frac{t}{2}}-\frac{1}{t}在(0,\pi]上可积,\:\\另外&还有\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{t}\,\mathrm{d}t=\int_0^{(n+\frac{1}{2})\pi}\frac{\sin t}{t}\,\mathrm{d}t\\总之,\qquad\qquad\qquad\qquad\qquad\\\int_{0}^{+\infty}\frac{\sin t}{t}\,\mathrm{d}t=&\lim_{n\to\infty}\int_{0}^{(n+\frac{1}{2})\pi}\frac{\sin t}{t}\mathrm{d}t=\lim_{n\to\infty}\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}\,\mathrm{d}t=\frac{\pi}{2}\end{align}$$这就得到了一个原先不能算的积分的值
	如若再做变量替换 $t=\lambda x$ , $\lambda>0$
	代入该式, 就得到了事实上有 $$\int_{0}^{+\infty}\frac{\sin\lambda x}{x}\,\mathrm{d}x=\frac{\pi}{2}$$注意这对 $\forall\,\lambda>0$ 都成立

## Fourier级数收敛性讨论

### Dirichlet核与局部化定理
在 $(3)$ 式 $f(x)=\frac{a_0}{2}+\sum\limits_{n=1}^\infty(a_{n}\cos nx+b_{n}\sin nx)$ 中固定 $x=x_0$ ，并取其部分和为 $$S_n(x_0)=\frac{a_0}{2}+\sum\limits_{k=1}^{n}(a_{k}\cos kx_0+b_{k}\sin kx_0)$$再代入 $$a_k=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\cos kx\,\mathrm{d}x,\qquad b_k=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\sin kx\,\mathrm{d}x$$得到 $$\begin{align}S_n(x_0)&=\frac{1}{2}\cdot\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\,\mathrm{d}x+\sum\limits_{k=1}^{n}\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)(\cos kx\cos kx_{0}+\sin kx\sin kx_{0})\,\mathrm{d}x\\&=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\bigg(\frac{1}{2}+\sum\limits_{k=1}^{n}\cos k(x-x_{0})\bigg)\,\mathrm{d}x\end{align}$$而有[[三角恒等式]] $$\frac{1}{2}+\sum\limits_{k=1}^{n}\cos k(x-x_{0})=\frac{\sin(n+\frac{1}{2})(x-x_0)}{2\sin\frac{x-x_0}{2}}$$故 $$S_n(x_0)=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)\frac{\sin(n+\frac{1}{2})(x-x_0)}{2\sin\frac{x-x_0}{2}}\,\mathrm{d}x$$出于周期为 $2\pi$ ，将原先的积分区间 $[-\pi,\pi]$ **改为** $[x_{0}-\pi,x_{0}+\pi]$ 讨论 **(注意是改为，而不是说相等)**
得到 $$\begin{align}S_n(x_0)&=\frac{1}{\pi}\int_{x_{0}-\pi}^{x_{0}+\pi}f(x)\frac{\sin(n+\frac{1}{2})(x-x_0)}{2\sin\frac{x-x_0}{2}}\,\mathrm{d}x\\&=\frac{1}{\pi}\int_{-\pi}^{\pi}f(x+x_0)\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}\,\mathrm{d}x\\&=\frac{1}{\pi}\bigg(\int_{-\pi}^{0}+\int_{0}^{\pi}\bigg)f(x+x_0)\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}\,\mathrm{d}x\\&=\frac{1}{\pi}\int_{0}^{\pi}f(x+x_0)\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}\,\mathrm{d}x+{\color{blue}\frac{1}{\pi}\int_{0}^{\pi}f(-x+x_0)\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}\,\mathrm{d}x}\\&=\frac{1}{\pi}\int_{0}^{\pi}\big(f(x_0+x)+f(x_0-x)\big){\color{red}\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}}\,\mathrm{d}x\end{align}$$这样的积分都叫做**Dirichlet积分**，这里 $$\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}$$称作**Dirichlet核**，可记作 $D_n(x)$

将 $S_n(x_0)$ 分段考虑 $$S_n(x_0)=\frac{1}{\pi}\bigg(\int_{0}^{\delta}+\int_{\delta}^{\pi}\bigg)$$这里 $\delta>0$ ，可以说是一个比较小的数
由于 $$\frac{f(x_0+x)+f(x_0-x)}{2\sin\frac{x}{2}}$$必然在 $[\delta,\pi]$ 上可积且绝对可积，故由**Riemann-Lebesgue引理**即知 $n\to\infty$ 时，有 $$\lim_{n\to\infty}\int_{\delta}^{\pi}\frac{f(x_0+x)+f(x_0-x)}{2\sin\frac{x}{2}}{\color{red}\sin(n+\frac{1}{2})x}\,\mathrm{d}x=0$$故只需要讨论 $\int_{0}^{\delta}$ ，也就是说这个积分的值在 $n\to\infty$ 时完全的取决于 $f(x)$ 在 $(x_{0}-\delta,x_{0}+\delta)$ 上的值，这就是

**Fourier级数的局部化定理**: 设 $f\in R[-\pi,\pi]$ , 则 $f$ 的Fourier级数在 $x_0$ 处的性态, 即收敛与否, 收敛于何值完全取决于 $f$ 在 $x_0$ 附近的行为

上面的结论说明了一个一点都不显然的结论：**即如果 $f,g$ 在 $x_0$ 附近，即足够小的邻域上有相同的值，尽管该邻域外 $f$ 与 $g$ 有差异，但并不影响它们的Fourier级数在 $x_0$ 处的敛散性以及收敛到的值是相同的，这个结论出乎意料是因为，它们的Fourier系数本身都是在 $[-\pi,\pi]$ 上的积分值确定的**

### 敛散性判别

利用**Riemann-Lebesgue引理**可以得到 $f$ 的Fourier级数收敛的充分判别条件

**Dini判别法**: 设 $f\in R[-\pi,\pi]$ , 对某个实数 $s$ , 令 $$\varphi(t)=f(x_0-t)+f(x_0+t)-2s$$若存在 $\delta>0$ , 使得函数 $\frac{\varphi(t)}{t}$ 在 $[0,\delta]$ 上可积且绝对可积, 则 $f$ 的Fourier级数在 $x_0$ 处收敛于 $s$
**[证明]**:
	由于 $$\frac{2}{\pi}\int_{0}^{\pi}\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}\,\mathrm{d}t=1$$故 $\forall\,x_0\in[-\pi,\pi]$ , $$\begin{align}S_n(x_0)-s&=\frac{1}{\pi}\int_{0}^{\pi}\big(f(x_0+x)+f(x_0-x)-2s\big)\frac{\sin(n+\frac{1}{2})x}{2\sin\frac{x}{2}}\,\mathrm{d}x\\&=\frac{1}{\pi}\int_{0}^{\pi}{\color{blue}\frac{\varphi(x)}{2\sin\frac{x}{2}}}\sin(n+\frac{1}{2})x\,\mathrm{d}x\end{align}\tag{5}$$而这里有 $$\frac{\varphi(x)}{2\sin\frac{x}{2}}\sim\frac{\varphi(x)}{x},\quad x\to0$$故如若 $\frac{\varphi(x)}{x}$ 在 $[0,\delta]$ 上可积且绝对可积, 立即即可得到 $\frac{\varphi(x)}{2\sin\frac{x}{2}}$ 在 $[0,\delta]$ 上可积且绝对可积
	由Riemann-Lebesgue引理, $(5)$ 式令 $n\to\infty$ , 右边的式子趋于零, 故 $S_{n}(x_{0})\to s$

**定义/推论**: 设 $f\in R[-\pi,\pi]$ , 如 $f$ 在 $x_0$ 附近满足 $\alpha$ 阶**Lipschitz条件**, 即 $\exists\,\delta>0$ , $L>0$ , $\alpha\in(0,1]$ , 使得 $t\in(0,\delta]$ 时, 有 $$|f(x_{0}+t)-f(x_{0}+0)|\leq Lt^{\alpha},\qquad|f(x_{0}-t)-f(x_{0}-0)|\leq Lt^{\alpha}$$则 $f$ 的Fourier级数在 $x_0$ 处收敛于 $\frac{f(x_0+0)+f(x_0-0)}{2}$ 
**[证明]**:
	令 $s=\frac{f(x_0+0)+f(x_0-0)}{2}$ , $\varphi(t)=f(x_0+t)+f(x_0-t)-2s$ , 只需证 $\frac{\varphi(t)}{t}$ 在 $[0,\delta]$ 上可积且绝对可积, 这里 $\delta$ 为某个正数
	由于 $$\begin{align}\bigg|\frac{\varphi(t)}{t}\bigg|&=\bigg|\frac{f(x_{0}+t)-f(x_0+0)}{t}+\frac{f(x_0-t)-f(x_0-0)}{t}\bigg|\\&\leq\frac{|f(x_0+t)-f(x_0+0)|}{t}+\frac{|f(x_0-t)-f(x_0-0)|}{t}\\&\leq\frac{2L}{t^{1-\alpha}}\end{align}$$当 $\alpha\in(0,1]$ 时, $\frac{2L}{t^{1-\alpha}}$ 在 $(0,\delta]$ 上可积, 于是 $\frac{\varphi(t)}{t}$ 绝对可积, 由Dini判别法可知级数收敛于 $s$

**推论**: 设 $f\in R[-\pi,\pi]$ ,
	$(1)$ 若 $f$ 在 $x_0$ 处有导数 $f^{'}(x)$ , **或是**有两个有限的单侧导数 $$f_{+}^{'}(x_0)=\lim_{x\to x_{0}^{+}}\frac{f(x)-f(x_{0})}{x-x_{0}},\qquad f_-^{'}(x_0)=\lim_{x\to x_{0}^{-}}\frac{f(x)-f(x_{0})}{x-x_{0}}$$则 $f$ 的Fourier级数在 $x_0$ 处收敛于 $f(x_0)$
	$(2)$ 如果 $f$ 在 $x_0$ 处仅有两个有限的广义单侧导数 $$\lim_{x\to x_{0}^+}\frac{f(x)-f(x_0+0)}{x-x_{0}},\qquad\lim_{x\to x_{0}^{-}}\frac{f(x)-f(x_0-0)}{x-x_0}$$则 $f$ 的Fourier级数在 $x_0$ 处收敛于 $\frac{f(x_{0}+0)+f(x_{0}-0)}{2}$ 

**定义**: 如果存在 $[a,b]$ 的分割 $$a=t_0<t_1<\cdots<t_n=b$$使得下面的定义在每个子区间 $[t_{k-1},t_k]$ 上的函数 $$g_k(x)=\begin{cases}f(t_{k+1}+0)\qquad&,x=t_{k-1}\\f(x)\qquad&,x\in(t_{k-1},t_k)\\f(t_k-0)\qquad&,x=t_k\end{cases}$$是可微的(端点处单侧可微), 则称 $f$ 在 $[a,b]$ 上是**分段可微**的

**定理**: 如果周期为 $2\pi$ 的函数 $f$ 在 $[-\pi,\pi]$ 上分段可微, 则 $f$ 的Fourier级数在每点 $x_0$ 处收敛于 $\frac{f(x_{0}+0)+f(x_{0}-0)}{2}$ , 特别地, 在连续点处收敛于 $f(x_0)$

**对于Fourier级数而言，对函数的可微性仅要求一阶可微**

对于上面的结论，用一个例子来验证
_例：周期为 $2\pi$ 的函数 $$f(x)=x,\quad(-\pi<x<\pi)\quad,f(-\pi)=\pi$$先计算它的Fourier系数，$$\begin{align}a_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x\cos nx\,\mathrm{d}x=0\\b_n=\frac{1}{\pi}\int_{-\pi}^{\pi}x\sin nx\,\mathrm{d}x&=\frac{1}{n\pi}\bigg((-x\cos nx)\bigg|^{\pi}_{-\pi}+\int_{\pi}^{-\pi}\cos nx\,\mathrm{d}x\bigg)=\frac{2\cdot(-1)^{n}}{n}\end{align}$$故 $f$ 的Fourier级数为$$\sum\limits_{n=1}^{\infty}\frac{2\cdot(-1)^{n}}{n}\sin nx$$这里由于 $f(x)$ 在 $(-\pi,\pi)$ 上可微，而 $(-\pi,\pi)$ 上都是连续点，故Fourier级数在 $(-\pi,\pi)$ 上收敛于 $f(x)$ ，而在不连续点，如 $\pi$ 处，由于 $f(\pi+0)=-\pi$ ，$f(\pi-0)=\pi$ ，故级数在 $\pi$ 处收敛于 $\frac{f(\pi+0)+f(\pi-0)}{2}=0$ ，同理，在 $-\pi$ 处也收敛于 $0$
另外，取连续点 $x=\frac{\pi}{2}$ ，得到 $$\frac{\pi}{2}=f(\frac{\pi}{2})=\sum\limits_{n=1}^{\infty}\frac{2\cdot(-1)^n}{n}\sin\frac{n\pi}{2}=\sum\limits_{n=1}^{\infty}\frac{2\cdot(-1)^{n-1}}{2n-1}$$这便再次可得到**Leibniz恒等式** $$\frac{\pi}{4}=1-\frac{1}{3}+\frac{1}{5}-\frac{1}{7}+\cdots$$（通过幂级数也可以得到）
_
再来看另一个例子
_例：将函数 $f(x)=x^2,\quad(-\pi\leq x\leq\pi)$ 展开为Fourier级数
将 $f$ 的定义域延伸至 $\mathbb{R}$ ，即 $$\tilde{f}(x)=f(x-2n\pi)\qquad,x\in[(2n-1)\pi,(2n+1)\pi)\quad(n\in\mathbb{Z})$$
先求Fourier系数 $$\begin{align}a_0&=\frac{1}{\pi}\int_{-\pi}^{\pi}x^{2}\,\mathrm{d}x=\frac{2}{3}\pi^{2}\\a_n=\frac{1}{\pi}\int_{-\pi}^{\pi}x^{2}\cos nx\,\mathrm{d}x&=\frac{2}{n\pi}\int_{-\pi}^{\pi}-x\sin nx\,\mathrm{d}x=\frac{2}{n^{2}\pi}\int_{-\pi}^{\pi}x\,\mathrm{d}(\cos nx)=\frac{4\cdot(-1)^{n}}{n^{2}},\quad n\in\mathbb{N^{*}}\\b_n&=\frac{1}{\pi}\int_{-\pi}^{\pi}x^{2}\sin nx\,\mathrm{d}x=0\end{align}$$由此得到Fourier级数 $$\frac{1}{3}\pi^{2}+\sum\limits_{n=1}^{\infty}\frac{4\cdot(-1)^{n}}{n^{2}}\cos nx$$由于 $f$ 在定义域内分段可微，并且全定义域内连续，则 $$\tilde{f}(x)=\frac{1}{3}\pi^{2}+\sum\limits_{n=1}^{\infty}\frac{4\cdot(-1)^{n}}{n^{2}}\cos nx$$将定义域限定在 $[-\pi,\pi]$ 上，此时 $\tilde{f}(x)=f(x)=x^2$ ，故有 $$x^{2}=\frac{1}{3}\pi^{2}+\sum\limits_{n=1}^{\infty}\frac{4\cdot(-1)^{n}}{n^{2}}\cos nx,\qquad -\pi\leq x\leq\pi$$特别地，令 $x=\pi$ ，就得到了恒等式 $$\pi^{2}=\frac{1}{3}\pi^{2}+\sum\limits_{n=1}^{\infty}\frac{4}{n^{2}}$$也即**巴塞尔问题**中的恒等式 $$\sum\limits_{n=1}^{\infty}\frac{1}{n^2}=\frac{\pi^2}{6}\tag{6}$$类似地，令 $x=0$ ，就得到了恒等式 $$\sum\limits_{n=1}^{\infty}\frac{(-1)^{n-1}}{n^2}=\frac{\pi^{2}}{12}$$他们都是收敛的级数，因此结合可得到 $$\begin{align}\sum\limits_{n=1}^{\infty}\frac{1}{(2n-1)^{2}}=\frac{\pi^2}{8}\\\sum\limits_{n=1}^{\infty}\frac{1}{(2n)^2}=\frac{\pi^2}{24}\end{align}$$即 **巴塞尔级数** $(6)$ 中的奇数项和与偶数项的比值满足 $3:1$
_

### Cesàro和

前面知道了 $f$ 的Fourier级数在 $x_0$ 处收敛于 $f(x_0)$ ，需要 $f$ 在 $x_0$ 处有一阶导数或是有左右导数，那么如若 $f$ 只有了连续性的条件，其Fourier级数是否还会收敛于 $f$ 呢
但是否定的

通常会在连续的条件上进一步加强 $f$ 的条件，但前人在该问题的研究上不再修改 $f$ 连续的条件，而是另辟蹊径，**修改了级数求和收敛的定义**
这个新的定义需要满足原先收敛意义下的级数在新的收敛定义下仍然收敛于相同的值，而原先发散的一些级数在新的定义下却是收敛的

**定义**: 设 $\sum\limits_{n=1}^{\infty}a_n$ 为无穷级数, $\{S_n\}$ 为部分和, 若记 $$\sigma_n=\frac{S_1+\cdots+S_n}{n}$$为一个收敛数列, $\lim_{n\to\infty}\sigma_n=\sigma$ , 就称级数 $\sum\limits_{n=1}^{\infty}a_n$ 在**Cesàro意义下收敛(均值意义下收敛)**, 称 $\sigma$ 为级数 $\sum\limits_{n=1}^{\infty}a_n$ 的**Cesàro和**, 记为 $\sum\limits_{n=1}^{\infty}a_n=\sigma\:(\mathrm{C})$ , 这时称级数 $\sum\limits_{n=1}^{\infty}a_{n}$ **可以Cesàro求和**

可以证明：**连续函数 $f$ 的Fourier级数在Cesàro意义下求和必然是收敛于自身的**
在此之前，我们先证明

**定理**: 设 $f\in R[-\pi,\pi]$ , 如果 $f$ 在 $x_{0}$ 处有左右极限 $f(x_{0}-0)$ 和 $f(x_{0}+0)$ , 则它的Fourier级数在 $x_{0}$ 处的Cesàro和为$$\frac{1}{2}\big(f(x_{0}+0)+f(x_{0}-0)\big)$$特别地, 当 $f$ 在 $x_0$ 连续时, 其Fourier级数在 $x_{0}$ 的Cesàro和为 $f(x_{0})$
**[证明]**:
	设 $$f(x)\sim\frac{a_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\cos nx+b_{n}\sin nx)$$之前已经算得其在某点 $x_{0}$ 的部分和为 $$S_n(x_{0})=\frac{1}{\pi}\int_{0}^{\pi}\big(f(x_{0}+t)+f(x_{0}-t)\big)\frac{\sin(n+\frac{1}{2})t}{2\sin \frac{t}{2}}\,\mathrm{d}t$$求其算术平均 $$\begin{align}\sigma_n(x_{0})&=\frac{1}{n}\sum\limits_{k=0}^{n-1}S_{k}(x_{0})\\&=\frac{1}{n\pi}\int_{0}^{\pi}\big(f(x_{0}+t)+f(x_{0}-t)\big)\sum\limits_{k=0}^{n-1}\frac{\sin(n+\frac{1}{2})t}{2\sin\frac{t}{2}}\,\mathrm{d}t\\&=\frac{1}{2n\pi}\int_{0}^{\pi}\big(f(x_{0}+t)+f(x_{0}-t)\big)\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t\end{align}$$这里用到[[三角恒等式]]: $$\sum\limits_{k=0}^{n-1}\sin(k+\frac{1}{2})t=\frac{\sin^2(\frac{nt}{2})}{\sin{\frac{t}{2}}}$$
	该式对任意的可积且绝对可积的 $f$ 都成立
	特别地, 令 $f=1$ , 得到[[积分恒等式]] $$\frac{1}{n}\int_{0}^{\pi}\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^2\,\mathrm{d}t=1$$记 $$s=\frac{f(x_{0}+0)+f(x_{0}-0)}{2}$$那么 $$\begin{align}\sigma_n(x_{0})-s&=\frac{1}{2n\pi}\int_{0}^{\pi}\big(f(x_{0}+t)+f(x_{0}-t)-2s\big)\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t\\&=\frac{1}{2n\pi}\int_{0}^{\pi}\varphi(t)\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t\end{align}$$左右极限 $f(x_{0}-0)$ 和 $f(x_{0}+0)$ 存在, 故 $\forall\,\varepsilon>0$ , $\exists\,\delta(x_{0},\varepsilon)\in(0,\pi)$ , 使得 $t\in(0,\delta(x_{0},\varepsilon))$ 时 $$|f(x_{0}+t)-f(x_{0}+0)|<\frac{\varepsilon}{2},\qquad|f(x_0-t)-f(x_{0}-0)|<\frac{\varepsilon}{2}$$那么 $$|\varphi(t)|=|f(x_0+t)+f(x_0-t)-2s|=|f(x_0+t)-f(x_0+0)+f(x_0-t)-f(x_0-0)|<\varepsilon$$对 $\sigma_{n}(x_{0})-s$ 分段估计 $$\sigma_{n}(x_{0})-s=\frac{1}{2n\pi}\big(\int_{0}^{\delta}+\int_{\delta}^{\pi}\big)\triangleq I_1+I_2$$对 $I_1$ 估计 $$|I_1|\leq\frac{1}{2n\pi}\int_{0}^{\delta}|\varphi(t)|\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{\varepsilon}{2n\pi}\int_{0}^{\delta}\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{\varepsilon}{2n\pi}\int_{0}^{\pi}\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t=\frac{\varepsilon}{2n\pi}$$对 $I_2$ 估计 $$|I_2|\leq\frac{1}{2n\pi}\int_{\delta}^{\pi}|\varphi(t)|\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{1}{2n\pi\sin^{2}\frac{\delta}{2}}\int_{0}^{\pi}|\varphi(t)|\,\mathrm{d}t$$记 $$A=\frac{\int_{0}^{\pi}|\varphi(t)|\,\mathrm{d}t}{2\pi\sin^{2}\frac{\delta}{2}},\qquad A为一个常数$$即有 $$|I_2|<\frac{A}{n}$$那么只要 $n>\frac{2A}{\varepsilon}$ , 就有 $$|\sigma_{n}(x_{0})-s|=|I|\leq|I_1|+|I_2|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}<\varepsilon$$即证

**推论**: 设 $f\in R[-\pi,\pi]$ , 若 $f$ 在 $x_0$ 处有左右极限, 且其Fourier级数在 $x_{0}$ 处收敛, 那么必定收敛于 $$\frac{f(x_0+0)+f(x_0-0)}{2}$$**[证明]**:
	若Fourier级数收敛于 $s$ , 即级数的常义和为 $s$, 则应有Cesàro和也为 $s$ , 而有上面的定理可知 $$s=\frac{f(x_0+0)+f(x_0-0)}{2}$$即证

_# 这一点也是Fourier级数与Taylor级数间的不同_

特别地，如果 $f$ 为连续函数之外还为周期函数，那么结论进一步加强

**Ferjér定理**: 如果 $f$ 是周期为 $2\pi$ 的连续函数, 则它的Fourier级数在Cesàro意义下, 于 $(-\infty,+\infty)$ 上一致收敛于 $f$ 
**[证明]**:
	前面已知 $$\sigma_n(x)-f(x)=\int_{0}^{\pi}\varphi_{x}(t)\bigg(\frac{\sin^{2}\frac{nt}{2}}{\sin \frac{t}{2}}\bigg)\,\mathrm{d}t$$对任意 $x\in\mathbb{R}$ 都成立, 由于 $f(x)$ 在 $[-2\pi,2\pi]$连续, 进而可知它在 $[-2\pi,2\pi]$ 上一致连续, 因此 $\forall\,\varepsilon>0$ , $\exists\,\delta(\varepsilon)>0$ , $s.t.$ $\forall\,t\in (0,\delta)$ , 有 $$|f(x+t)-f(x)|<\frac{\varepsilon}{2},\qquad|f(x-t)-f(x)|<\frac{\varepsilon}{2}$$**下面的估计思路和之前大致一样, 主要的区别在于 $\delta$ 与 $x$ 不再有关**$$|\varphi_{x}(t)|=|f(x+t)+f(x-t)-2f(x)|=|f(x+t)-f(x)+f(x-t)-f(x)|<\varepsilon$$对 $\sigma_{n}(x)-s$ 分段估计 $$\sigma_{n}(x)-f(x)=\frac{1}{2n\pi}\big(\int_{0}^{\delta}+\int_{\delta}^{\pi}\big)\triangleq I_1+I_2$$对 $I_1$ 估计 $$|I_1|\leq\frac{1}{2n\pi}\int_{0}^{\delta}|\varphi_{x}(t)|\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{\varepsilon}{2n\pi}\int_{0}^{\delta}\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{\varepsilon}{2n\pi}\int_{0}^{\pi}\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t=\frac{\varepsilon}{2n\pi}$$对 $I_2$ 估计 $$|I_2|\leq\frac{1}{2n\pi}\int_{\delta}^{\pi}|\varphi(t)|\bigg(\frac{\sin\frac{nt}{2}}{\sin\frac{t}{2}}\bigg)^{2}\,\mathrm{d}t<\frac{1}{2n\pi\sin^{2}\frac{\delta}{2}}\int_{0}^{\pi}|\varphi(t)|\,\mathrm{d}t$$注意 $f(x)$ 为连续函数, 那么在 $[-\pi,\pi]$ 上有界
	设 $$|f(x)|\leq M$$进而 $$|\varphi_{x}(t)|=|f(x+t)+f(x-t)-2f(x)|\leq4M$$因此 $$|I_2|\leq\frac{2M}{n\sin^{2}\frac{\delta}{2}}$$那么只要 $n>\frac{4M}{\varepsilon\sin^{2}\frac{\delta}{2}}$ , 就有 $$|\sigma_{n}(x)-f(x)|=|I|\leq|I_1|+|I_2|<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}<\varepsilon$$对 $\forall\,x\in[-\pi,\pi]$ 成立, 而 $f$ 是 $\mathbb{R}$ 上周期为 $2\pi$ 的函数, 其实也可得到 $\sigma_{n}(x)$ 也是周期为 $2\pi$ 的函数, 总之 $$\forall\,x\in\mathbb{R},\:\exists\,x_0\in[-\pi,\pi],\:\exists\,n_{0}\in\mathbb{N},\:s.t.\,x=x_0+2n_{0}\pi$$因此 $$|\sigma_{n}(x)-f(x)|=|\sigma_{n}(x_{0}+2n_{0}\pi)-f(x_{0}+2n\pi)|=|\sigma_{n}(x_{0})-f(x_{0})|<\varepsilon$$故对于 $\forall\,x\in\mathbb{R}$ 该式成立, 立即可得到    $\sigma_{n}(x)\rightrightarrows f(x)\qquad (n\to\infty)\qquad(x\in\mathbb{R})$

连续函数在闭区间上不一定能够幂级数展开，同样的也不一定能够Fourier展开，但作为幂级数的替代，连续函数却可以由多项式逼近，那么或许也可以由Fourier级数对应的三角函数式逼近我们已知的函数，这就是**三角多项式一致逼近闭区间上的连续函数**
作为Fejér定理的应用，研究用三角多项式逼近连续函数的问题的部分见[[级数逼近]]

# Fourier积分

经过前面的讨论，我们知道如果函数 $f$ 在区间 $[-l,l]$ 上满足一些性质（如分段可微），则可以将 $f$ 在 $[-l,l]$ 上展开为Fourier级数：$$f(x)=\frac{a_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\cos\frac{n\pi}{l}x+b_{n}\sin\frac{n\pi}{l}x)\tag{7}$$这里 $$a_{n}=\frac{1}{l}\int_{-l}^{l}f(x)\cos\frac{n\pi}{l}x\,\mathrm{d}x,\qquad b_{n}=\frac{1}{l}\int_{-l}^{l}f(x)\sin\frac{n\pi}{l}x\,\mathrm{d}x$$如果 $f$ 定义在 $\mathbf{R}$ 上，且在任意的有限区间内满足级数收敛的条件，并且在 $\mathbf{R}$ 上绝对可积，那么对于取定的 $x$ ，可以找到充分大的 $l$ ，使得 $l>|x|$ ，即时 $f(x)$ 可以用 $(7)$ 的展开式合法表示，但对于 $\mathbf{R}$ 中任意的 $x$ 来说，一个确定的 $l$ 总是不可能充分大的，进而不同的 $x$ ，用的表达式也必然会可能不同，故由此引出下面的通用表达式：
设 $f$ 在 $(-\infty,+\infty)$ 上绝对可积，对任意的实数 $u$ ，定义 $$a(u)=\frac{1}{\pi}\int_{-\infty}^{+\infty}f(t)\cos ut\,\mathrm{d}t,\qquad b(u)=\frac{1}{\pi}\int_{-\infty}^{+\infty}f(t)\sin ut\,\mathrm{d}t\tag{8}$$这两个积分显然也是绝对收敛的，类似于Fourier级数的形式，将 $$\int_{0}^{+\infty}(a(u)\cos ux+b(u)\sin ux)\,\mathrm{d}u$$称为 $f$ 的**Fourier积分**，记为 $$f(x)\sim\int_{0}^{+\infty}(a(u)\cos ux+b(u)\sin ux)\,\mathrm{d}u$$类似于Fourier级数时的情形，$f$ 的Fourier积分是否收敛，是否收敛于 $f$ ，这些都尚未可知，这就是接下来要研究的内容
类似于级数的部分和，记 $$S(\lambda,x)=\int_{0}^{\lambda}(a(u)\cos ux+b(u)\sin ux)\,\mathrm{d}u$$