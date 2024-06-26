
# Bernstein多项式

**定义**: 如果定义在有限闭区间 $[a,b]$ 上的函数, 对 $\forall\,\varepsilon>0$ , 存在多项式 $P$ , 使得 $\forall\,x\in[a,b]$ , 有 $$|f(x)-P(x)|<\varepsilon$$则称 $f$ 在 $[a,b]$ 上能用多项式**一致逼近**

显然如果 $f$ 能够幂级数展开，则可以用多项式一致逼近，但幂级数展开要求 $f$ 有任意阶导数，这个条件十分的强，因此希望能寻找更加弱的条件能够保证 $f$ 可以用多项式一致逼近，并最好找到构造这个多项式的方法，前人已经找到了该充要条件：

**Weierstrass逼近定理**: 闭区间 $[a,b]$ 上的函数 $f$ 能够用多项式一致逼近当且仅当 $f$ 在 $[a,b]$ 上连续
**[定义/证明]**:
	**(必要性)** 如果已知 $f$ 可以由多项式一致逼近, 那么 $\forall\,n\in\mathbb{N^{*}}$ , $\exists\,P_{n}(x)\in\mathbb{R}[x]$ , 使得 $$|f(x)-P_{n}(x)|<\frac{1}{n}$$因此连续函数列 $\{P_{n}(x)\}$ 在 $[a,b]$ 上一致收敛于 $f$ , 故 $f$ 在 $[a,b]$ 上连续
	**(充分性)** 为了证明, 构造Bernstein多项式, 先记 $$B_{i}^{n}(x)=C_{n}^{i}x^{i}(1-x)^{n-i}\qquad(i=0,1,\cdots,n)$$该多项式有如下性质: 
		$(i)$ $\forall\,x\in[a,b]$ , $$B_{i}^{n}(x)\geq0$$$(ii)$ $\forall\,x\in[a,b]$ , $$\sum\limits_{i=0}^{n}B_{i}^{n}(x)=1$$$(iii)$ 记 $$P(x)=\sum\limits_{i=0}^{n}a_{i}B_{i}^{n}(x)$$有 $$P^{'}(x)=n\sum\limits_{i=0}^{n-1}(a_{i+1}-a_{i})B_{i}^{n-1}(x)$$性质 $(i)$ 和 $(ii)$ 都十分显然, 下面证明 $(iii)$ , $$\begin{align}P^{'}(x)&=\big(\sum\limits_{i=0}^{n}a_{i}C_{n}^{i}x^{i}(1-x)^{n-i}\big)^{'}\\&=\sum\limits_{i=1}^{n}a_{i}\frac{n!}{(n-i)!i!}ix^{i-1}(1-x)^{n-i}-\sum\limits_{i=0}^{n-1}a_{i}\frac{n!}{(n-i)!i!}(n-i)x^{i}(1-x)^{n-i-1}\\&=\sum\limits_{i=1}^{n}a_{i}\frac{n!}{(n-i)!(i-1)!}x^{i-1}(1-x)^{n-i}-\sum\limits_{i=0}^{n-1}a_{i}\frac{n!}{(n-i-1)!i!}x^{i}(1-x)^{n-i-1}\\&=\sum\limits_{i=0}^{n-1}a_{i+1}\frac{n!}{(n-i-1)!i!}x^{i}(1-x)^{n-i-1}-\sum\limits_{i=0}^{n-1}a_{i}\frac{n!}{(n-i-1)!i!}x^{i}(1-x)^{n-i-1}\\&=n\sum\limits_{i=0}^{n-1}(a_{i+1}-a_{i})\frac{(n-1)!}{(n-i-1)!i!}x^{i}(1-x)^{n-i-1}\\&=n\sum\limits_{i=0}^{n-1}(a_{i+1}-a_{i})B_{i}^{n-1}(x)\end{align}$$即证
	现在定义**Bernstein多项式**: 
		设 $f:[0,1]\to\mathbb{R}$ 称 $$B_n(f;x)=\sum\limits_{i=0}^{n}f(\frac{i}{n})C_{n}^{i}x^{i}(1-x)^{n-i}=\sum\limits_{i=0}^{n}f(\frac{i}{n})B_{i}^{n}(x)$$为 $f$ 的 **$n$ 次Bernstein多项式**
	---------------------------------------------------------------------------------------
	先证一个关于Bernstein多项式的性质
	**引理**: 对于 $\forall\,x\in[0,1]$ , 有 $$\sum\limits_{i=0}^{n}(k-nx)^{2}B_{k}^{n}(x)\leq\frac{n}{4}$$**证明**: 
		先计算 $B_{n}(x;x)$ 和 $B_{n}(x^{2},x)$
		$(\mathrm{I})$ $$B_{n}(x;x)=\sum\limits_{i=0}^{n}\frac{i}{n}B_{i}^{n}(x)$$由性质 $(iii)$ 应有 $$B_{n}^{'}(x;x)=n\sum\limits_{i=0}^{n-1}\frac{i-(i-1)}{n}B_{i}^{n-1}(x)=\sum\limits_{i=0}^{n-1}B_{i}^{n-1}(x)=1$$故有 $$B_{n}(x;x)=x+c_{1}$$再代入 $x=0$ , 得到 $$c_{1}=B_{n}(x;0)=\sum\limits_{i=0}^{n}\frac{i}{n}B_{i}^{n}(0)=\sum\limits_{i=0}^{n}\frac{i}{n}C_{n}^{i}x^{i}(1-x)^{n-i}\bigg|_{x=0}=\frac{0}{n}C_{n}^{0}\cdot1\cdot1^{n}=0$$因此 $B_{n}(x;x)=x$
		$(\mathrm{II})$ $$B_{n}(x^2;x)=\sum\limits_{i=0}^{n}\frac{i^2}{n^2}B_{i}^{n}(x)$$由性质 $(iii)$ 得 $$\begin{align}B_{n}^{'}(x^2;x)&=n\sum\limits_{i=0}^{n-1}\frac{2i+1}{n^2}B_{i}^{n-1}(x)\\&=\frac{2n-2}{n}\sum\limits_{i=0}^{n-1}\frac{i}{n-1}B_{i}^{n-1}(x)+\frac{1}{n}\\&=\frac{2n-2}{n}B_{n-1}(x;x)+\frac{1}{n}\\&=2(1-\frac{1}{n})x+\frac{1}{n}\end{align}$$故有 $$B_{n}(x^{2};x)=(1-\frac{1}{n})x^2+\frac{x}{n}+c_2$$再代入 $x=0$ , 得到 $$c_2=B_{n}(x^{2};0)=0$$因此 $B_{n}(x^{2};x)=(1-\frac{1}{n})x^{2}+\frac{x}{n}$
		接下来可以证明不等式了, 直接计算
		$(\mathrm{III})$ $$\begin{align}\sum\limits_{k=0}^{n}(k-nx)^{2}B_{k}^{n}(x)&=\sum\limits_{k=0}^{n}k^{2}B_{k}^{n}(x)-2nx\sum\limits_{k=0}^{n}kB_{k}^{n}(x)+n^{2}x^{2}\sum\limits_{k=0}^{n}B_{k}^{n}(x)\\&=n^{2}B_{n}(x^{2};x)-2n^{2}xB_{n}(x;x)+n^{2}x^{2}B_{n}(1;x)\\&=n^2\big((1-\frac{1}{n})x^{2}+\frac{x}{n}\big)-2n^{2}x^{2}+n^{2}x^{2}\\&=nx-nx^2=nx(1-x)\leq\frac{n}{4}\end{align}$$即证
	---------------------------------------------------------------------------------------
	将接下来的证明分为两部分: 
	$(a)$ 我们证明 $[0,1]$ 上的连续函数 $f$ 的Bernstein多项式在 $[0,1]$ 上一致收敛于 $f$
	由于 $f$ 在 $[0,1]$ 上连续, 故必然一致连续, 那么 $\forall\,\varepsilon>0$ , $\exists\,\delta>0$ , $s.t.$ $\forall\,x_{1},x_{2}\in[0,1]$ , 满足 $|x_{1}-x_{2}|<\delta$ , 就有 $|f(x_{1})-f(x_{2})|<\frac{\varepsilon}{2}$ 
	由性质 $(ii)$ 可得到 $$f(x)=\sum\limits_{i=0}^{n}f(x)B_{i}^{n}(x)$$将 $i$ 的取值集如此划分: $$\{0,1,\cdots,n\}=\underbrace{\{i:|\frac{i}{n}-x|\geq\delta\}}_{E_1}\cup\underbrace{\{i:|\frac{i}{n}-x|<\delta\}}_{E_2}$$则 $$\begin{align}|B_{n}(f;x)-f(x)|&\leq\sum\limits_{i=0}^{n}|f(\frac{i}{n})-f(x)|B_{i}^{n}(x)\\&=\sum\limits_{i\in E_{1}}|f(\frac{i}{n})-f(x)|B_{i}^{n}(x)+\sum\limits_{i\in E_{2}}|f(\frac{i}{n})-f(x)|B_{i}^{n}(x)\\&\triangleq S_{1}+S_{2}\end{align}$$对 $S_{1}$ , $S_{2}$ 分别估计, 
	对 $S_{1}$ 估计, 由于 $f$ 为 $[0,1]$ 上的连续函数, 故其有界, 设 $|f|\leq M$ , 则$$\begin{align}S_{1}&\leq2M\sum\limits_{i\in E_{1}}B_{i}^{n}(x)\\&\leq\frac{2M}{\delta^{2}}\sum\limits_{i\in E_{1}}\delta^{2}B_{i}^{n}(x)\\&\leq\frac{2M}{\delta^{2}}\sum\limits_{i\in E_{1}}(\frac{i}{n}-x)^{2}B_{i}^{n}(x)\\&\leq\frac{2M}{\delta^{2}n^{2}}{\color{blue}\sum\limits_{i=0}^{n}(i-nx)^{2}B_{i}^{n}(x)}\leq\frac{2M}{\delta^{2}n^{2}}\cdot{\color{blue}\frac{n}{4}}\qquad{\color{blue}(引理)}\\&=\frac{M}{2\delta^{2}n}\end{align}$$再对 $S_{2}$ 估计, $$S_{2}<\sum\limits_{i\in E_{2}}\frac{\varepsilon}{2}B_{i}^{n}(x)\leq\frac{\varepsilon}{2}\sum\limits_{i=0}^{n}B_{i}^{n}(x)=\frac{\varepsilon}{2}$$那么当 $n$ 足够大, 确切来讲当 $n>\lceil\frac{M}{\varepsilon\delta^{2}}\rceil$ 时, 就有 $S_{1}<\frac{\varepsilon}{2}$
	进而有 $$S=S_{1}+S_{2}<\frac{\varepsilon}{2}+\frac{\varepsilon}{2}=\varepsilon$$这就说明了 $B_{n}(f;x)$ 在 $[0,1]$ 上一致收敛于 $f(x)$
	$(b)$ 下面只需要将 $[0,1]$ 拓展到任意有界闭区间 $[a,b]$ , 设 $f$ 在区间 $[a,b]$ 上连续, 作换元 $$x=a+t(b-a),\qquad t\in[0,1]$$记 $f(x)=f(a+t(b-a))=g(t)$ , 则 $g(t)$ 是 $[0,1]$ 上的连续函数, 那么 $\forall\,\varepsilon>0$ , $\exists\,P(t)\in\mathbb{R}[t]$ , 使得 $|g(t)-P(t)|<\varepsilon$ , 在换元式中反解出 $t$ $$t=\frac{x-a}{b-a}$$再代入刚得到的式子 $$\bigg|f(x)-P(\frac{x-a}{b-a})\bigg|=|g(t)-P(t)|<\varepsilon$$显然 $P(\frac{x-a}{b-a})$ 是关于 $x$ 的多项式, 故即证

# 三角多项式

**定义**: 称 $$T_{n}(x)=\frac{a_{0}}{2}+\sum\limits_{k=1}^{n}(\alpha_{k}\cos kx+\beta_{k}\sin kx)$$为 **$n$ 次三角多项式**, 

**定义**: 如果定义在有限闭区间 $[a,b]$ 上的函数, 对 $\forall\,\varepsilon>0$ , 存在三角多项式 $T$ , 使得 $\forall\,x\in[a,b]$ , 有 $$|f(x)-T(x)|<\varepsilon$$则称 $f$ 在 $[a,b]$ 上能用三角多项式**一致逼近**

**Weierstrass逼近定理**: 闭区间 $[-\pi,\pi]$ 上的连续函数 $f$ , 如果满足 $f(-\pi)=f(\pi)$ , 则必然能用三角多项式一致逼近
**[证明]**:
	由于 $f(-\pi)=f(\pi)$ , 故可以将 $f$ 延拓为 $\mathbb{R}$ 上以 $2\pi$ 为周期的连续函数 $\tilde{f}$ 
	根据**Fejér定理**可知, $\tilde{f}$ 必然可以在 $(-\infty,\infty)$ 上用序列 $\{\sigma_{n}(x)\}$ 一致逼近
	我们知道 $f$ 的Fourier级数的 $k$ 项部分和 $S_{k}(x)$ 为一个 $k$ 次的三角多项式
	因此$$\sigma_{n}(x)=\frac{1}{n}(S_{0}(x)+S_{1}(x)+\cdots+S_{n-1}(x))$$为一个 $n-1$ 次的三角多项式, 这就找到了一个一致逼近 $f$ 的三角多项式序列

# 平方平均逼近

上面讨论了对于周期为 $2\pi$ 的连续周期函数都可以用三角多项式一致逼近
现在将连续的条件进一步放弱，对于一般的可积函数，是否还可以做到都可以用序列一致逼近呢？
答案是否定的，一致逼近的实质便是下面这个式子 $$\sup_{-\pi\leq x\leq\pi}|f(x)-T_{n}(x)|\to0\quad(n\to\infty)$$它意味着 $f$ 和 $T_{n}$ 的差值在整个区间内都要**均匀地**趋近于 $0$ ，不允许有任何点是例外，连续函数点点之间邻近，相差很小，可以做到，但对于一般的可积函数而言，因为断点的存在，就不再一定能够做到了

于是放弃了一致逼近，转而只要求三角多项式 $T_{n}$ 能够**平均地**逼近 $f$ 即可，即要求有 $$\int_{-\pi}^{\pi}(f(x)-T_{n}(x))^{2}\,\mathrm{d}x\to0\quad(n\to\infty)$$下面是我们讨论的前提：
	如果 $f$ 为 $[-\pi,\pi]$ 上的有界函数，假定 $f$ Riemann可积，则必定有 $f^{2}$ Riemann可积
	如果 $f$ 为 $[-\pi,\pi]$ 上的无界函数，假定 $f^{2}$ 反常可积，则必有 $|f|$ 反常绝对可积
	记这样的函数类为 $\mathbf{R}^{2}[-\pi,\pi]$

**定义**: 设 $f\in\mathbf{R}^{2}[-\pi,\pi]$ , 如果存在三角多项式序列 $\{T_{n}\}$ , 使得 $$\lim_{n\to\infty}\int_{-\pi}^{\pi}(f(x)-T_{n}(x))^{2}\,\mathrm{d}x=0$$则称 $\{T_{n}\}$ **平方平均收敛于 $f$** , 或是称 $f$ 可用三角多项式**平方平均逼近**

该结论的证明关键也与 $f$ 的Fourier级数密切相关，事实上与Fourier级数的部分和相关的**极值性质**有关，为证明**三角函数系**下的Fourier级数相关结论，其实不妨考虑**一般的正交函数系**下的Fourier级数的结论
$\mathbf{R}^{2}[a,b]$ 是 $[a,b]$ 上可积且平方可积的函数集，可以证明其构成一个**线性空间**，引入**内积** $$\langle f,g\rangle=\int_{a}^{b}f(x)g(x)\,\mathrm{d}x$$更是构成了**内积空间**，内积空间有关定义这里不再陈述，见[[有度量的线性空间]]
但是这个内积空间的基我们实则还并不清楚，看起来好像是其中的正交函数系：$$\{\varphi_{0},\varphi_{1},\cdots,\varphi_{n},\cdots\}$$但其实并未知是否空间内的函数都可用它们线性表出，即不能确定这是一组基，恰好的，其实这正是我们本身要研究的问题，如果 $\mathbf{R}^{2}[a,b]$ 中的函数都可以用该函数系表出，就说明了可以用这样的正交函数系平方平均逼近

**定义**: 设 $\{\varphi_{k}\}$ 为 $\mathbf{R}^{2}[a,b]$ 上的规范正交系, $\forall\,f\in\mathbf{R}^{2}[a,b]$ , 称 $$c_{k}=\langle f,\varphi_k\rangle=\int_{a}^{b}f(x)\varphi_{k}(x)\,\mathrm{d}x\quad(k=0,1,\cdots)$$为 $f$ 关于正交系 $\{\varphi_{k}\}$ 的**Fourier系数**, 将由此产生的级数 $\sum\limits_{k=1}^{\infty}c_{k}\varphi_{k}(x)$ 称为 $f$ 关于正交系 $\{\varphi_{k}\}$ 的 **Fourier级数**, 记作 $$f(x)\sim\sum\limits_{k=1}^{\infty}c_{k}\varphi_{k}(x)$$
_# 之前讨论的三角函数系下的Fourier级数其实都是规范正交系 $$\{\frac{1}{\sqrt{2\pi}},\frac{\cos x}{\sqrt{\pi}},\frac{\sin x}{\sqrt{\pi}},\cdots,\frac{\cos nx}{\sqrt{\pi}},\frac{\sin nx}{\sqrt{\pi}},\cdots\}$$下的结果_

记部分和 $$S_{n}(x)=\sum\limits_{k=0}^{n}c_{k}\varphi_{k}(x)$$称 $$T_{n}(x)=\sum\limits_{k=0}^{n}\alpha_{k}\varphi_{k}(x)$$为 $n$ 次 $\varphi$ 多项式，$\alpha_{k}$ 为给定的实数

现在需要探究的问题便成为：
对于给定的空间内的函数 $f$ 和给定的正整数 $n$ ，如何找到一个 $n$ 次 $\varphi$ 多项式 $T_{n}(x)$ ，使得 $$||f-T_{n}||=\bigg(\int_{a}^{b}(f(x)-T_{n}(x))^{2}\,\mathrm{d}x\bigg)^{\frac{1}{2}}$$尽可能的小

可以通过规范正交系及Fourier系数相关性质直接计算：
$$\begin{align}||f-T_{n}||^{2}&=\int_{a}^{b}(f(x)-T_{n}(x))^{2}\,\mathrm{d}x\\&=\int_{a}^{b}f^{2}(x)\,\mathrm{d}x-2\int_{a}^{b}f(x)\sum\limits_{k=0}^{n}\alpha_{k}\varphi_{k}(x)\,\mathrm{d}x+\int_{a}^{b}\big(\sum\limits_{k=0}^{n}\alpha_{k}\varphi_{k}(x)\big)^{2}\,\mathrm{d}x\\&=||f||^{2}-2\sum\limits_{k=0}^{n}\alpha_{k}\int_{a}^{b}f(x)\varphi_{k}(x)\,\mathrm{d}x+\sum\limits_{i=0}^{n}\sum\limits_{j=0}^{n}\alpha_{i}\alpha_{j}\int_{a}^{b}\varphi_{i}(x)\varphi_{j}(x)\,\mathrm{d}x\\&=||f||^{2}-2\sum\limits_{k=0}^{n}\alpha_{k}c_{k}+\sum\limits_{i=0}^{n}\sum\limits_{j=0}^{n}\alpha_{i}\alpha_{j}\delta_{ij}\\&=||f||^{2}-2\sum\limits_{k=0}^{n}\alpha_{k}c_{k}+\sum\limits_{k=0}^{n}\alpha_{k}^{2}\\&=||f||^{2}+\sum\limits_{k=0}^{n}(\alpha_{k}-c_{k})^{2}-\sum\limits_{k=0}^{n}c_{k}^{2}\\&\geq||f||^{2}-\sum\limits_{k=0}^{n}c_{k}^2\end{align}$$等号成立当且仅当 $$\alpha_{k}=c_{k}\qquad(k=0,1,\cdots,n)$$这时 $||f-T_{n}||^{2}$ 取到最小值
这就是**Fourier级数部分和的极值性质**
由上面的推导过程可以直接得到 $$\sum\limits_{k=0}^{n}c_{k}^{2}\leq||f||^{2}$$这就是**Bessel不等式**
由于上式右边与 $n$ 无关，对 $n$ 取极限可得到 $$\sum\limits_{k=0}^{\infty}c_{k}^{2}\leq||f||^{2}<+\infty$$即级数 $\sum\limits_{k=0}^{\infty}c_{k}^{2}$ 收敛，可知 $c_{k}\to0\:(k\to\infty)$
上面的结论总结下来便是下面的定理

**定理**: 设 $f\in\mathbf{R}^{2}[a,b]$ , $\{\varphi_{k}\}$ 为 $\mathbf{R}^{2}[a,b]$ 中的规范正交系, $\{c_{k}\}$ 为 $f$ 关于 $\{\varphi_{k}\}$ 的Fourier系数, 则有: 
	$(1)$ 对任意的正整数 $n$ 和实数 $\alpha_{0},\alpha_{1},\cdots,\alpha_{n}$ , 有 $$||f-\sum\limits_{k=0}^{n}\alpha_{k}\varphi_{k}(x)||\geq||f-\sum\limits_{k=0}^{n}c_{k}\varphi_{k}(x)||$$$(2)$ $$||f-\sum\limits_{k=0}^{n}c_{k}\varphi_{k}(x)||=||f||^{2}-\sum\limits_{k=0}^{n}c_{k}^{2}$$$(3)$ $$\sum\limits_{k=0}^{\infty}c_{k}^{2}\leq||f||^{2}$$

注意上面提到的式子 $$\sum\limits_{k=0}^{\infty}c_{k}^{2}\leq||f||^{2}$$如果等号成立，我们其实就找到了我们要的结果
将等式 $$\sum\limits_{k=0}^{\infty}c_{k}^{2}=||f||^{2}$$称为**Perseval等式**或**Perseval封闭性方程**
几何意义十分明显，如果规范正交函数系 $\{\varphi_{k}\}$ 可以作为空间的基，若 $f$ 展开为Fourier级数 $$f(x)=c_{0}\varphi_{0}(x)+c_{1}\varphi_{1}(x)+\cdots+c_{n}\varphi_{n}(x)+\cdots$$则 $(c_{0},c_{1},\cdots,c_{n},\cdots)$ 便为 $f$ 在该组基下的坐标，**Perseval等式**便意为无穷维空间中的勾股定理

**定义**: 设 $\{\varphi_{k}\}$ 为 $\mathbf{R}^{2}[a,b]$ 中的一个规范正交系, 如果 $\forall\,f\in\mathbf{R}^{2}[a,b]$ , Perseval等式成立, 此时称该组规范正交系 $\{\varphi_{k}\}$ 是**完备**的

**推论**: 规范正交系 $\{\varphi_{k}\}$ 是完备的当且仅当对 $\forall\,f\in\mathbf{R}^{2}[a,b]$ , 有 $$\lim_{n\to\infty}||f-\sum\limits_{k=0}^{n}c_{k}\varphi_{k}||^{2}=0$$即 $f$ 可用 $\{\varphi_{k}\}$ 的Fourier级数平方平均逼近

现在来看 $\mathbf{R}^{2}[-\pi,\pi]$ 上三角规范正交系$$\{\frac{1}{\sqrt{2\pi}},\frac{\cos x}{\sqrt{\pi}},\frac{\sin x}{\sqrt{\pi}},\cdots,\frac{\cos nx}{\sqrt{\pi}},\frac{\sin nx}{\sqrt{\pi}},\cdots\}$$的Bessel不等式和Perseval等式
记 $$\varphi_{0}(x)=\frac{1}{\sqrt{2\pi}},\quad\varphi_{2k-1}(x)=\frac{\cos kx}{\sqrt{\pi}},\quad\varphi_{2k}(x)=\frac{\sin kx}{\sqrt{\pi}}$$设 $f\in\mathbf{R}^{2}[-\pi,\pi]$ ，有 $$\begin{align}&c_{0}=\int_{-\pi}^{\pi}f(x)\varphi_{0}(x)\,\mathrm{d}x=\frac{1}{\sqrt{2\pi}}\int_{-\pi}^{\pi}f(x)\,\mathrm{d}x=\sqrt{\frac{\pi}{2}}a_{0}\\&c_{2k-1}=\int_{-\pi}^{\pi}f(x)\varphi_{2k-1}(x)\,\mathrm{d}x=\frac{1}{\sqrt{\pi}}\int_{-\pi}^{\pi}f(x)\cos kx\,\mathrm{d}x=\sqrt{\pi}a_{k}\\&c_{2k}=\int_{-\pi}^{\pi}f(x)\varphi_{2k}(x)\,\mathrm{d}x=\frac{1}{\sqrt{\pi}}\int_{-\pi}^{\pi}f(x)\sin kx\,\mathrm{d}x=\sqrt{\pi}b_{k}\end{align}$$因此 $$\sum\limits_{k=0}^{2n}c_{k}\varphi_{k}(x)=\frac{c_{0}}{2}+\sum\limits_{k=1}^{n}(a_{k}\cos kx+b_{k}\sin kx)$$这里 $a_{k}$ 和 $b_{k}$ 都是同[[Fourier级数]]中的定义的Fourier系数
如此 $f$ 的Bessel不等式写作 $$\frac{a_{0}^2}{2}+\sum\limits_{k=1}^{n}(a_{k}^{2}+b_{k}^{2})\leq\frac{1}{\pi}\int_{-\pi}^{\pi}f^{2}(x)\,\mathrm{d}x\tag{B}$$对应 $f$ 的Perseval等式写作 $$\frac{a_{0}^2}{2}+\sum\limits_{k=1}^{n}(a_{k}^{2}+b_{k}^{2})=\frac{1}{\pi}\int_{-\pi}^{\pi}f^{2}(x)\,\mathrm{d}x\tag{P}$$
**定理**: 设 $f\in\mathbf{R}^{2}[-\pi,\pi]$ , $a_{n},b_{n}$ 是 $f$ 关于三角函数系的Fourier系数, 那么 $f$ 可用它的Fourier级数的部分和平方平均逼近, 即Perseval等式 $(\mathrm{P})$ 成立
**[证明]**:
	(待)

**推论**: 如果 $[-\pi,\pi]$ 上的连续函数 $f$ 和三角函数系 $$\{1,\cos x,\sin x,\cdots,\cos nx,\sin nx,\cdots\}$$中的每个函数都正交, 则必然有$f=0$
**[证明]**:
	(待)

**推论**: 如果两个连续函数有相同的Fourier级数, 则这两个连续函数必然恒等
**[证明]**:
	(待)

**定理**: 设 $f,g\in\mathbf{R}^{2}[-\pi,\pi]$ , $a_{n}$ , $b_{n}$ , 和 $\alpha_{n}$ , $\beta_{n}$ 分别是 $f$ 和 $g$ 的Fourier系数, 那么 $$\frac{1}{\pi}\int_{-\pi}^{\pi}f(x)g(x)\,\mathrm{d}x=\frac{a_{0}\alpha_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\alpha_{n}+b_{n}\beta_{n})$$**[证明]**:
	(待)

**定理**: 设 $f\in\mathbf{R}^{2}[-\pi,\pi]$ , 其Fourier级数为 $$f(x)\sim\frac{a_{0}}{2}+\sum\limits_{n=1}^{\infty}(a_{n}\cos nx+b_{n}\sin nx)$$那么对包含 $[-\pi,\pi]$ 的任意区间 $[a,b]$ , 有 $$\int_{a}^{b}f(x)\,\mathrm{d}x=\int_{a}^{b}\frac{a_{0}}{2}\,\mathrm{d}x+\sum\limits_{n=1}^{\infty}\int_{a}^{b}(a_{n}\cos nx+b_{n}\sin nx)\,\mathrm{d}x$$**[证明]**:
	(待)

该定理说明了**无论Fourier级数收敛与否，一定可以逐项积分**

