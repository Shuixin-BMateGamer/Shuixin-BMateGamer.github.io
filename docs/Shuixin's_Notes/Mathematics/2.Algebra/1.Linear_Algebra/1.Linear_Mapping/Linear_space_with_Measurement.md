
# 双线性函数

## 基本内容
**定义**: 设 $V$ 为域 $\mathbf F$ 上的线性空间, $V\times V$ 到 $F$ 的一个映射 $f$ 若满足 $\forall\,\alpha_1,\alpha_2,\alpha,\beta_1,\beta_2,\beta\in V,k_1,k_2\in F$ 有 $$\begin{align}&(1)\qquad f(k_1\alpha_1+k_2\alpha_2,\beta)=k_1f(\alpha_1,\beta)+k_2f(\alpha_2,\beta)\\&(2)\qquad f(\alpha,k_1\beta_1+k_2\beta_2)=k_1f(\alpha,\beta_1)+k_2f_2(\alpha,\beta_2)\end{align}$$ 则称 $f$ 为一个 $V$ 上的**双线性函数**, $f$ 也写成 $f(\alpha,\beta)$ .

_当 $\beta$ 固定时，$\alpha\longmapsto f(\alpha,\beta)$ 为 $V$ 上的一个线性函数，记作 $\beta_R$
当 $\alpha$ 固定时，$\beta\longmapsto f(\alpha,\beta)$ 为 $V$ 上的一个线性函数，记作 $\alpha_L$_

_例：
	$(1)$ $R^n$ 上的标准内积 $(\alpha,\beta)$ 为双线性函数
	$(2)$ 域 $\mathbf F$ 上 $n$ 维线性空间 $V$ , $V$ 上一组基 $\alpha_1,\alpha_2,...,\alpha_n$ , 设 $\alpha=\sum_{k=1}^na_i\alpha_i$ , $\beta=\sum_{k=1}^nb_k\beta_k$ 则 $f(\alpha,\beta)=\sum_{k=1}^na_kb_k$ 为 $V$ 上的一个双线性函数；特别地，当 $V=F^n$ 时，同 $R^n$ 一样，一般将 $f(\alpha,\beta)$ 记作 $(\alpha,\beta)$ 或 $\alpha\cdot\beta$
	$(3)$  在 $M_n(F)$ 上，令 $f(A,B)=\mathrm{tr}(AB)$ , $(A,B\in M_n(F))$ ，则 $f(A,B)$ 为双线性函数
	$(4)$ 在 $C[a,b]$ 上，令 $f(g(x),h(x))=\int_a^bg(x)h(x)\mathrm{dx}$ ，$(g(x),h(x)\in C[a,b])$ , 则 $f(g(x),h(x))$ 为双线性函数_


类似于线性函数，函数被线性空间的基的函数值唯一确定，单线性函数当时用 $F^n$ 中的元素与函数做对应，那么类似地，对于双线性函数或许需要 $F^{n\times n}$ 即 $M_n(F)$ 中的元素

**定义**: 域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 中取一组基 $\alpha_1,\alpha_2,...,\alpha_n$ , 若 $\alpha,\beta\in V$ 在基下的坐标分别为$$x=(x_1,x_2,\cdots,x_n)^{'}\qquad y=(y_1,y_2,\cdots,y_n)^{'}$$ 若 $f$ 为 $V$ 上的一个双线性函数, 则$$f(\alpha,\beta)=f(\sum_{k=1}^nx_k\alpha_k,\sum_{k=1}^ny_k\alpha_k)=\sum_{i=1}^n\sum_{j=1}^nx_iy_jf(\alpha_i,\alpha_j)$$ 令$$A=\begin{bmatrix}f(\alpha_1,\alpha_1)&f(\alpha_1,\alpha_2)&\cdots&f(\alpha_1,\alpha_n)\\f(\alpha_2,\alpha_1)&f(\alpha_2,\alpha_2)&\cdots&f(\alpha_2,\alpha_n)\\\vdots&\vdots&\ddots&\vdots\\f(\alpha_n,\alpha_1)&f(\alpha_n,\alpha_2)&\cdots&f(\alpha_n,\alpha_n)\end{bmatrix}$$ 称 $A$ 为双线性函数在基 $\alpha_1,\alpha_2,...,\alpha_n$ 下的**度量矩阵**, 由 $f$ 和基 $\alpha_1,\alpha_2,...,\alpha_n$ 唯一确定
该矩阵满足 $$f(\alpha,\beta)=\sum_{i=1}^n\sum_{j=1}^nx_iy_jf(\alpha_i,\alpha_j)=\sum_{i=1}^n\sum_{j=1}^nx^{'}(1\,;i)A(i\,;j)y(j\,;1)=\sum_{i=1}^nx^{'}(1\,;i)(Ay)(i\,;1)=x^{'}Ay$$ 反之, 若任取 $A=(a_{ij})\in M_n(F)$ , 定义 $$\begin{align}f:\quad V\times V&\longrightarrow F\\(\alpha,\beta)&\longmapsto f(\alpha,\beta)=x^{'}Ay=\sum_{i=1}^n\sum_{j=1}^na_{ij}x_iy_j\end{align}$$ 则 $f$ 为 $V$ 上的双线性函数, 且 $f$ 在基 $\alpha_1,\alpha_2,...,\alpha_n$ 下的度量矩阵就为 $A$ 

_由此可知，若 $x^{'}Ay=x^{'}By\,(\forall\,x,y\in F^n)$ , 则 $A=B$_

将 $x^{'}Ay$ 称为 $x_1,x_2,...,x_n$ 与 $y_1,y_2,...,y_n$ 的**双线性型**，利用 $V$ 中向量 $\alpha,\beta$ 在基下的坐标的双线性型可以诱导出一个双线性函数

**定理**: 若 $f$ 为 $n$ 维线性空间 $F^V$ 上的一个双线性函数, 若 $V$ 中基 $\alpha_1,\alpha_2,...,\alpha_n$ 到基 $\beta_1,\beta_2,...,\beta_n$ 的过渡矩阵为 $P$ , 而基 $\alpha_1,\alpha_2,...,\alpha_n$ 下 $f$ 的度量矩阵为 $A$ , 基 $\beta_1,\beta_2,...,\beta_n$ 下 $f$ 的度量矩阵为 $B$ , 则有 $$B=P^{'}AP$$
因此，双线性函数在不同基下的度量矩阵是合同的，自然也是相抵的

相反也易知两个合同的矩阵可以看成一个双线性函数在两组基下的度量矩阵

**定义**: 将 $V$ 上的双线性函数 $f$ 的度量矩阵的秩称为 $f$ 的**矩阵秩**, 记作 $\mathrm{rank}_mf$ 

**定义**: 设 $f$ 为域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 上的双线性函数, $V^*$ 有一个子空间为$$\langle\alpha_L,\beta_R\,|\alpha,\beta\in V\rangle=\{k_1\alpha_L+k_2\beta_R:k_1,k_2\in\mathbf F\}$$ 将其称为 $f$ 的**秩空间**, 空间的维数称为 $f$ 的**秩**, 记作 $\mathrm{rank}\,f$ 

_（可以证明，$\mathrm{rank}_m\,f\leq \mathrm{rank}\,f$ ）_

**定义**: 设 $f$ 为域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 上的双线性函数, $V$ 的子集 $$\{\alpha\in V|f(\alpha,\beta)=0,\:\forall\beta\in V\}$$ 称为 $f$ 在 $V$ 中的**左根**, 记作 $\mathrm{rad}_L\,V$ , 同理可以定义**右根**, $$\mathrm{rad}_R\,V=\{\beta\in V|f(\alpha,\beta)=0,\:\forall\,\alpha\in V\}$$ 
_不难证明左根和右根都是 $V$ 的子空间_

**定义**: 若双线性函数 $f$ 的左根和右根都是零子空间, 则称 $f$ 是**非退化的**

**定理**: 域 $\mathbf F$ 上 $n$ 维线性空间 $V$ 上的双线性函数 $f$ 是非退化的当且仅当 $f$ 在 $V$ 中的度量矩阵满秩

## 对称双线性函数与非对称双线性函数

**定义**: 设 $f$ 为域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 的双线性函数
	若满足 $f(\alpha,\beta)=f(\beta,\alpha)$ , $(\forall\,\alpha,\beta\in V)$ 则称为**对称函数**
	若满足 $f(\alpha,\beta)=-f(\beta,\alpha)$ , $(\forall\,\alpha,\beta\in V)$ 则称为**斜(反)对称函数**

_$f$ 为（斜）对称函数当且仅当 $f$ 在 $V$ 中的度量矩阵为（斜）对称矩阵_

**定理**:  特征不为 $2$ 的域 $\mathbf F$ 上 $n$ 维线性空间 $V$ 上的对称双线性函数 $f$ 必然有一组基下的度量矩阵为对角矩阵

_该定理旨在简化双线性函数在一对向量上的函数值运算_

**定理**:  特征不为 $2$ 的域 $\mathbf F$ 上 $n$ 维线性空间 $V$ 上的斜对称双线性函数 $f$ 必然有一组基 $\delta_1,\delta_{-1},...,\delta_r,\delta_{-r},\eta_1,...,\eta_s\:(r\leq\frac{n}{2},s=n-2r)$ 下的度量矩形如$$\mathrm{diag}\Bigg\{\begin{pmatrix}0&1\\-1&0\end{pmatrix},\cdots,\begin{pmatrix}0&1\\-1&0\end{pmatrix},0,\cdots,0\Bigg\}$$ 
**推论**: 若 $V$ 上的斜对称双线性函数 $f$ 非退化, 则存在一个 $V$ 中的基使得 $f$ 在该基下的度量矩阵形如$$\mathrm{diag}\Bigg\{\begin{pmatrix}0&1\\-1&0\end{pmatrix},\begin{pmatrix}0&1\\-1&0\end{pmatrix},\cdots,\begin{pmatrix}0&1\\-1&0\end{pmatrix}\Bigg\}$$ 这说明了 $\dim V$ 必为偶数



## 对称双线性函数与二次型

**定义**: 设 $V$ 为域 $\mathbf F$ 上线性空间, 如果存在 $V$ 上的一个对称双线性函数 $f$ 使得 $$q(\alpha)=f(\alpha,\alpha)\quad(\forall\,\alpha\in V)$$ 这里 $q$ 为一个 $V$ 到 $F$ 的映射, 则称 $q$ 为 $V$ 上的**二次函数**

可以知道，当 $f$ 给定，则确定了一个 $q$
通常相反也成立

**定理**: 设特征不为 $2$ 的域 $\mathbf F$ 上的线性空间 $V$ , $q$ 为 $V$ 上的一个二次函数, 则存在 $V$ 上唯一的对称双线性函数 $f$ , 使得$$q(\alpha)=f(\alpha,\alpha)\quad(\forall\,\alpha\in V)$$ 
若 $\alpha,\beta$ 在 $V$ 的一组基 $\alpha_1,\alpha_2,...,\alpha_n$ 下的坐标分别为 $x=(x_1,x_2,...,x_n)^{'},y=(y_1,y_2,...,y_n)^{'}$
对称双线性函数 $f$ 在该基下的度量矩阵为 $A=(a_{ij})$ , 那么 $f(\alpha,\beta)=x^{'}Ay$ ，由此可知，若有二次函数 $q(\alpha)=f(\alpha,\alpha)$ ，则 $q(\alpha)=x^{'}Ax$ 为 $n$ 元二次型 $x^{'}Ax$ ，那么其中 $A$ 就称为二次函数 $q$ 在**基 $\alpha_1,\alpha_2,...,\alpha_n$ 下的矩阵** 

利用对称双线性函数理论，可以给出研究二次型时核心的惯性定理的第二个证明
 
**惯性定理**: 实数域上任意一个 $n$ 元二次型都可以经过非退化线性替换化成唯一的规范形 $$y_1^2+\cdots+y_p^2-y_{p+1}^2-\cdots-y_r^2$$
**Witt消去定理**: 设特征不为 $2$ 的域 $\mathbf F$ , $A_1$ 和 $A_2$ 为该域上的 $n$ 级对称矩阵, $B_1$ 和 $B_2$ 为该域上的 $m$ 级对称矩阵, 若 $$\begin{bmatrix}A_1&O\\O&B_1\end{bmatrix}\simeq\begin{bmatrix}A_2&O\\O&B_2\end{bmatrix}$$且 $A_1\simeq A_2$ , 则有 $B_1\simeq B_2$


## 双线性函数空间

**定义**: 设 $V$ 为域 $\mathbf{F}$ 上的线性空间, 将 $V$ 上所有双线性函数组成的集合记作 $T_{2}(V)$ , 易验证 $T_{2}(V)$ 对于函数加法与纯量乘法构成线性空间, 将 $T_{2}(V)$ 称为 $V$ 上的**双线性函数空间**



# 内积空间
## 实内积空间
### 基本内容

**定义**: $f$ 为 $n$ 维实线性空间 $V$ 上的对称双线性函数 , 若 $\forall\,\alpha\in V$ , 有 $f(\alpha,\alpha)\geq0$ , 并且等号成立当且仅当 $\alpha=1$ , 则称 $f$ 为**正定的**

**命题**: $f$ 为 $n$ 维实线性空间 $V$ 上的对称双线性函数 , $f$ 在 $V$ 的一个基 $\alpha_1,\alpha_2,...,\alpha_n$ 下的度量矩阵为 $A$ , 则 $f$ 为正定的当且仅当 $A$ 为正定矩阵

**命题**: $f$ 为 $n$ 维实线性空间 $V$ 上的正定对称双线性函数 , 则 $V$ 中存在一个基 $\eta_1,\eta_2,...,\eta_n$ 使得 $f$ 在此基下的度量矩阵为 $I$ , 进而 $f$ 在此基下的表达式为 $$f(\alpha,\beta)=x_1y_1+x_2y_2+\cdots+x_ny_n$$这里 $\alpha=\sum_{i=1}^nx_i\eta_i$ , $\beta=\sum_{i=1}^ny_i\eta_i$

**定义**: 设 $V$ 为实数域上的一个线性空间, $V$ 上的一个正定的对称双线性函数 $f$ 称为 $V$ 上的一个**内积**, 如果给定了 $V$ 上的一个内积, 则将 $V$ 连同其内积成为一个**实内积空间**, 特别地, 有限维的实内积空间 $V$ 称为**Euclid空间**, 并且将线性空间 $V$ 的维数称为Euclid空间 $V$ 的**维数**

_例：
	$(1)$ $R^n$ 上的**标准内积** $(\alpha,\beta):=x_1y_1+x_2y_2+\cdots+x_ny_n$ , 这里 $\alpha=\sum_{i=1}^nx_i\varepsilon_i$ , $\beta=\sum_{i=1}^ny_i\varepsilon_i$
	$(2)$ $M_n(R)$ 上可定义内积 $(A,B):=\mathrm{tr}(AB^{\mathrm T})$ 
	$(3)$ 实数域上的 $C[a,b]$ , 可定义内积 $(f,g):=\int_a^bf(x)g(x)\mathrm{dx}$_

**定义**: 非负实数 $\sqrt{(\alpha,\alpha)}$ 称为实内积空间 $V$ 中向量 $\alpha$ 的**长度**, 记作 $|\alpha|$ 或 $||\alpha||$ 

显然有 $|k\alpha|=|k||\alpha|$ , $\forall\,\alpha\in V,\forall\,k\in R$  

**定义**: 长度为 $1$ 的向量称为**单位向量**, 如果 $\alpha\neq0$ , 则 $\frac{1}{|\alpha|}\alpha$ 为一个单位向量, 将 $\alpha$ 变为 $\frac{1}{|\alpha|}$ 的过程称为将 $\alpha$ **单位化**

**Cauchy-буняковский-Schwarz不等式**: 实内积空间中, 有对于任意向量 $\alpha,\beta$ 成立的不等式$$|(\alpha,\beta)|\leq|\alpha||\beta|$$等号成立当且仅当 $\alpha$ 与 $\beta$ 线性相关

要注意的是，由于该不等式的成立，才可以在更高维的空间中有下面夹角的定义，而非用所谓的几何意义反过来证明该不等式

**定义**: 实内积空间 $V$ 中, 非零向量 $\alpha,\beta$ 间的**夹角**定义并记作为: $$\langle\alpha,\beta\rangle:=\arccos\frac{(\alpha,\beta)}{|\alpha||\beta|}$$有 $0\leq\langle\alpha,\beta\rangle\leq\pi$ , 以及 $(\alpha,\beta)=0\iff\langle\alpha,\beta\rangle=\frac{\pi}{2}$

由该定义可以引出概念：

**定义**: 在实内积空间 $V$ 中, 如果 $(\alpha,\beta)=0$ , 那么称 $\alpha$ 与 $\beta$ **正交**, 记作 $\alpha\perp\beta$

由内积的正定性立即得到 $\alpha$ 若与自身正交, 则必然 $\alpha$ 为零向量, 另一方面, 若 $\alpha$ 与 $V$ 中的一切向量都正交, 则必然有 $\alpha$ 为零向量, 因此**内积为非退化的正定对称双线性函数**

在实内积空间中，勾股定理与余弦定理同样成立，利用基本定义和运算法则，都是平凡的结论

**命题**: 在实内积空间 $V$ 中, 由两两正交的非零向量组成的集合是线性无关的

**推论**: 在 $n$ 维Euclid空间 $V$ 中, 彼此正交的非零向量的个数不超过 $n$

**定义**: 在 $n$ 维Euclid空间 $V$ 中, 由 $n$ 个两两正交的非零向量组成的基称为 $V$ 的一个**正交基**, 由 $n$ 个两两正交的单位向量组成的基称为 $V$ 的一个**标准(规范)正交基**

先前提到过，内积作为正定的对称双线性函数必然存在一组基 $\eta_1,\eta_2,...,\eta_n$ 使得该基下的度量矩阵为单位阵 $I_n$ , 因此有 $\eta_i\eta_j=\delta_{ij}$ ($\mathrm{Kronecker}$ 记号) , 由此可验证 $\eta_1,\eta_2,...,\eta_n$ 为 $V$ 的一组标准正交基

## 酉空间
### 基本内容

**定义**: 设 $V$ 是复数域上的线性空间, 若存在一个二元函数 $(\alpha,\beta)$ , 如果满足 $\forall\,\alpha,\beta,\gamma\in V,k\in C$ , 有: 
	$(1)$ $(\alpha,\beta)=\overline{(\beta,\alpha)}$  (Hermite性)
	$(2)$ $(\alpha+\gamma,\beta)=(\alpha,\beta)+(\gamma,\beta)$  (L1)
	$(3)$ $(k\alpha,\beta)=k(\alpha,\beta)$  (L2)
	$(4)$ $(\alpha,\alpha)\geq0$ , 取等当且仅当 $\alpha=0$ (正定性)
则将 $(\alpha,\beta)$ 称为 $V$ 上的一个**内积**

具有Hermite性的内积对于两个变元具有**共轭线性性**, 即 $\forall\,\alpha_1,\alpha_2,\alpha,\beta_1,\beta_2,\beta\in V,k_1,k_2\in C$ 有: $$\begin{align}(k_1\alpha_1+k_2\alpha_2,\beta)=\overline{(\beta,k_1\alpha_1+k_2\alpha_2)}&=\overline{(\beta,k_1\alpha_1)}+\overline{(\beta,k_2\alpha_2)}=\overline{k_1}(\alpha_1,\beta)+\overline{k_1}(\alpha_2,\beta)\\(\alpha,k_1\beta_1+k_2\beta_2)=\overline{(k_1\beta_1+k_2\beta_2,\alpha)}&=\overline{(k_1\beta_1,\alpha)}+\overline{(k_2\beta_2,\alpha)}=\overline{k_1}(\alpha,\beta_1)+\overline{k_2}(\alpha,\beta_2)\end{align}$$也即**共轭双线性函数**

**定义**: 若复线性空间 $V$ 上指定了内积, 将 $V$ 以及其内积运算称作**复内积空间**或**酉空间**

_$C^n$ 可以定义内积 $(x,y):=x_1\overline{y_1}+x_2\overline{y_2}+\cdots+x_n\overline{y_n}$ , 这里 $x=(x_1,x_2,\cdots,x_n)^{'},y=(y_1,y_2,\cdots,y_n)^{'}$
其称为**标准内积**, 于是 $C^n$ 为酉空间_

**定义**: 常记 $\overline{x^{\mathrm T}}\triangleq x^*$ , 将 $x^*$ 称为 $x$ 的**共轭转置**, (有时称为**伴随**或**Hermite伴随**)

那么 $(x,y)=y^*x$


## 求解标准正交基

为理解下面的定理，先考虑低维时的几何意义

**一维**：略

**二维**：已知线性无关的向量 $\alpha_1,\alpha_2$ 
如图:

```tikz
\begin{document}
	\begin{tikzpicture}
		\draw[->,thick] (1,1)--(2,4) node[left]{$\alpha_2$};
		\draw[->,thick] (1,1)--(4,3) node[right]{$\alpha_1$};
	\end{tikzpicture}
\end{document}
``` 

以 $\alpha_1$ 为基准 $(\beta_1=\alpha_1)$ , 试通过 $\alpha_2$ 求一个与 $\beta_1$ 正交的向量 $\beta_2$ , 最直接的方法是求出 $\alpha_2$ 在 $\beta_1$ 上的投影向量 $\alpha_2^{(1)}$ , 那么 $\alpha_2-\alpha_2^{(1)}$ 是与 $\beta_1$ 垂直的: 

```tikz
\begin{document}
	\begin{tikzpicture}
		\draw[->,thick] (1,1)--(2,4) node[left]{$\alpha_2$};	
		\draw[->,thick] (1,1)--(40/13,31/13) node[below]{$\alpha_2^{(1)}$};
		\draw[-,thick,dashed] (40/13,31/13)--(2,4);
		\draw[->,thick,color=red] (1,1)--(4,3) node[right]{$\alpha_1=\beta_1$};
	\end{tikzpicture}
\end{document}
``` 

具体过程为: 设 $\alpha_2^{(1)}=\lambda_1\beta_1$ , $\lambda_1\in R$ , 应有 $(\alpha_2,\beta_1)=(\alpha_2^{(1)},\beta_1)$ , 因此 $(\alpha_2,\beta_1)=(\lambda_1\beta_1,\beta_1)=\overline{\lambda_1}(\beta_1,\beta_1)=\lambda_1(\beta_1,\beta_1)$ , 得到 $$\lambda_1=\frac{(\alpha_2,\beta_1)}{(\beta_1,\beta_1)}$$得到 $\alpha_2^{(1)}=\frac{(\alpha_2,\beta_1)}{(\beta_1,\beta_1)}\beta_1$ , 这里可以将 $\lambda_1$ 看作一个伸缩比, 即将 $\beta_1$ 伸缩变换为 $\alpha_2^{(1)}$ 所需要乘的伸缩系数
接下来依照几何意义, 可以猜测 $\alpha_2-\alpha_2^{(1)}$ 为一个正交于 $\beta_1$ 的向量, 记为 $\beta_2$ : 

```tikz
\begin{document}
	\begin{tikzpicture}
		\draw[->,thick] (1,1)--(2,4) node[left]{$\alpha_2$};	
		\draw[->,thick] (1,1)--(40/13,31/13) node[below]{$\alpha_2^{(1)}$};
		\draw[-,thick,dashed] (40/13,31/13)--(2,4);
		\draw[->,thick,color=red] (1,1)--(4,3) node[right]{$\alpha_1=\beta_1$};
		\draw[->,thick,dashed,color=red] (1,1)--(-1/13,34/13) node[left]{$\beta_2=\alpha_2-\alpha_2^{(1)}$};
	\end{tikzpicture}
\end{document}
``` 

**麻雀虽小五脏俱全**
在这个简单的例子中体现了下面定理的要点: 
	已有一组线性无关的向量 $\alpha_1,\alpha_2,...,\alpha_s$
	$(1)$ 选取一个基向量 $\alpha_1$ 作为不动的基准 $\beta_1$
	$(2)$ 逐个将其余“零散”的基向量 $\alpha_k\,(k\leq s)$ **调整替换**至与已得到的正交向量组 $\beta_1,...,\beta_{k-1}$ 垂直, 调整结果为 $\beta_k$
	具体调整过程就是: 
	$(i)$ 求得这一步要调整的向量 $\alpha_k$ 在已调整得到的正交向量组 $\beta_1,...,\beta_{k-1}$ 上面的一系列投影向量 $\alpha_{k}^{(1)},...,\alpha_{k}^{(k-1)}$ , 应满足 $(\alpha_k,\alpha_j)=(\alpha_k^{(j)},\alpha_j)$ , $(j=1,...,k-1)$ , 求得了 $\alpha_k^{(j)}=\frac{(\alpha_k,\alpha_j)}{(\alpha_j,\alpha_j)}\alpha_j$
	$(ii)$ 那么将 $\alpha_k$ 调整为 $\beta_k=\alpha_k-\alpha_k^{(1)}-\cdots-\alpha_k^{(k-1)}$ , 可以验证 $(\beta_k,\beta_i)=0$ , $(i=1,...,k-1)$
	当将这过程不断进行直至 $\alpha_1,\alpha_2,...,\alpha_s$ 都替换为 $\beta_1,\beta_2,...,\beta_s$ 后, 后者便是我们要得到的结果

这便是: 

**Gram-Schmidt正交化**: 设 $\alpha_1,\alpha_2,...,\alpha_s$ 为内积空间中的一个线性无关的向量组, 令$$\begin{align}\beta_1\,&=\,\alpha_1\\\beta_2\,&=\,\alpha_2\,-\,\frac{(\alpha_2,\beta_1)}{(\beta_1,\beta_1)}\beta_1\\&\cdots\\\beta_s\,&=\,\alpha_s\,-\,\sum_{j=1}^{s-1}\frac{(\alpha_s,\beta_j)}{(\beta_j,\beta_j)}\beta_j\end{align}$$则 $\beta_1,\beta_2,...,\beta_s$ 为正交向量组, 并且向量组 $\beta_1,\beta_2,...,\beta_s$ 和向量组 $\alpha_1,\alpha_2,...,\alpha_s$ 等价

如若再对 $\beta_1,\beta_2,...,\beta_s$ 单位化，则得到一组正交单位向量组

由上可知，**任取一组基→Schmidt正交化→单位化→得到一组标准正交基**

使用标准正交基有许多便捷之处
若 $\eta_1,\eta_2,...,\eta_n$ 为**实**内积空间 $V$ 的一组标准正交基，则有
	$(1)$ $(\eta_i,\eta_j)=\delta_{ij}$
	$(2)$ 基 $\eta_1,\eta_2,...,\eta_n$ 的度量矩阵为 $I$
	$(3)$ 内积在基 $\eta_1,\eta_2,...,\eta_n$ 下的表达式为 $(\alpha,\beta)=x^{\mathrm T}y=x_1y_1+x_2y_2+\cdots+x_ny_n$ , 这里 $x=(x_1,x_2,\cdots,x_n)^{\mathrm T}$ , $y=(y_1,y_2,\cdots,y_n)^{\mathrm T}$ 分别是 $\alpha$ 和 $\beta$ 在基 $\eta_1,\eta_2,...,\eta_n$ 下的坐标
若 $\eta_1,\eta_2,...,\eta_n$ 为**酉**空间 $V$ 的一组标准正交基，则有
	$(1)$ $(\eta_i,\eta_j)=\delta_{ij}$
	$(2)$ 基 $\eta_1,\eta_2,...,\eta_n$ 的度量矩阵为 $I$
	$(3)$ 内积在基 $\eta_1,\eta_2,...,\eta_n$ 下的表达式为 $(\alpha,\beta)=y^*x=x_1\overline{y_1}+x_2\overline{y_2}+\cdots+x_n\overline{y_n}$ , 这里 $x=(x_1,x_2,\cdots,x_n)^{\mathrm T}$ , $y=(y_1,y_2,\cdots,y_n)^{\mathrm T}$ 分别是 $\alpha$ 和 $\beta$ 在基 $\eta_1,\eta_2,...,\eta_n$ 下的坐标

**命题**: 设 $\eta_1,\eta_2,...,\eta_n$ 为 $n$ 维内积空间 $V$ 的一组标准正交基, 则对于 $\forall\,\alpha\in V$ , 有 $$\alpha=\sum_{i=1}^n(\alpha,\eta_i)\eta_i$$即 $\alpha$ 在标准正交基 $\eta_1,\eta_2,...,\eta_n$ 下的坐标的第 $i$ 个坐标下的分量为 $(\alpha,\eta_i)$ , $(i=1,2,...,n)$
上面的式子称为 $\alpha$ 的 **$\mathrm{\mathbf{Fourier}}$ 展开** , 各基向量的系数 $(\alpha,\eta_i)$ 都称为 $\alpha$ 的 **$\mathrm{\mathbf{Fourier}}$ 系数**

**命题**: 设 $\eta_1,\eta_2,...,\eta_n$ 为**实内积空间** $V$ 的一个标准正交基, 且有 $$(\beta_1,\beta_2,\cdots,\beta_n)=(\eta_1,\eta_2,\cdots,\eta_n)P$$则 $\beta_1,\beta_2,...,\beta_n$ 为 $V$ 的标准正交基当且仅当 $P$ 为**正交矩阵**

**命题**: 设 $\eta_1,\eta_2,...,\eta_n$ 为**酉空间** $V$ 的一个标准正交基, 且有 $$(\beta_1,\beta_2,\cdots,\beta_n)=(\eta_1,\eta_2,\cdots,\eta_n)P$$则 $\beta_1,\beta_2,...,\beta_n$ 为 $V$ 的标准正交基当且仅当 $P$ 为**酉矩阵**

## 正交补空间

**定义**: 设 $U$ 是内积空间 $V$ 的子空间, 令 $$U^{\perp}=\{v\in V|(v,U)=0\}=\{v\in V|(v,u)=0,\forall\,u\in U\}$$显然 $U^{\perp}$ 为 $U$ 的子空间, 将 $U^{\perp}$ 称为 $U$ 的**正交补空间**

**定理**: 设 $V$ 为 $n$ 维内积空间, $U$ 为 $V$ 的子空间, 则:
	$(1)$ $V=U\oplus U^{\perp}$
	$(2)$ $U$ 的任意一组标准正交基均可扩展为 $V$ 的一组标准正交基

**定义**: 设 $V$ 为 $n$ 维内积空间, $V_1,V_2,...,V_k$ 为 $V$ 的子空间, 若 $\forall\,\alpha\in V_i$ , $\forall\,\beta\in V_j$ , 有 $(\alpha,\beta)=0$ , 则称子空间 $V_i$ 和 $V_j$ **正交**, 若 $V=V_{1}+V_{2}+\cdots+V_{k}$ , 且 $V_{i}$ 两两正交, 称 $V$ 为 $V_{1},V_{2},...,V_{k}$ 的**正交和**, 记作 $$V=V_{1}\perp V_{2}\perp \cdots\perp V_{k}$$
**引理**: 正交和必为直和且任意 $V_{i}$ 都与其余子空间的和正交

**定义**: 设 $V=V_{1}\perp V_{2}\perp \cdots\perp V_{k}$ , 定义 $V$ 上的线性变换 $E_{i}$ : 若 $v=v_{1}+\cdots+v_{i}+\cdots+v_{k}$ , 令 $E_{i}(v)=v_{i}$ , 则称 $E_{i}$ 为 $V$ 到 $V_{i}$ 上的**正交投影**

**性质**:
	$(\mathrm{I})$ $E_{i}^{2}=E_{i}$
	$(\mathrm{II})$ $E_{i}E_{j}=\delta_{ij}E_{i}$
	$(\mathrm{III})$ $\sum_{i=1}^{k}E_{i}=I$

**命题**: 设 $U$ 为内积空间 $V$ 的子空间, $V=U\perp U^{\perp}$ , 设 $E$ 为 $V$ 到 $U$ 的正交投影, 则对 $\forall\,\alpha,\beta\in V$
有 $$(E(\alpha),\beta)=(\alpha,E(\beta))$$
下面的定理是一般的内积空间中“斜边大于直角边”

**Bessel不等式**: 设 $v_{1},v_{2},...,v_{m}$ 为内积空间 $V$ 中的正交非零向量组, $y$ 为 $V$ 中的任意向量, 则有 $$\sum\limits_{k=1}^{m}\frac{|(y,v_{k})|^{2}}{||v_{k}||^{2}}\leq||y||^{2}$$取等的充要条件为 $y\in\langle v_{1},v_{2},\cdots,v_{m}\rangle$

该不等式在分析中有重要的应用，见[[级数逼近]]

### 最佳逼近元

**定理**: 设 $U$ 是实内积空间 $V$ 的一个子空间, 且 $V=U\oplus U^{\perp}$ , 则对于 $\alpha\in V$ , $\alpha_{1}\in U$ 是 $\alpha$ 在 $U$ 上的正交投影的充要条件为 $$d(\alpha,\alpha_{1})\leq d(\alpha,\gamma),\qquad\forall\,\gamma\in U$$**[证明]**:
	(必要性) 设 $\alpha_{1}$ 为 $\alpha$ 在 $U$ 上的正交投影, 则 $d(\alpha,\gamma)=|\alpha-\gamma|=|\alpha-\alpha_{1}+\alpha_{1}-\gamma|\geq|\alpha-\alpha_{1}|+|\alpha_{1}-\gamma|\geq|\alpha-\alpha_{1}|=d(\alpha,\alpha_{1})$
	(充分性) 设 $\alpha$ 在 $U$ 上的投影为 $\delta$ , 则应有 $d(\alpha,\delta)\leq d(\alpha,\alpha_{1})$
	那么 $d(\alpha,\alpha_{1})\geq d(\alpha,\delta)=|\alpha-\delta|=|\alpha-\alpha_{1}|+|\alpha_{1}-\delta|\geq|\alpha-\alpha_{1}|=d(\alpha,\alpha_{1})$ 当且仅当 $\alpha_{1}=\delta$ 时成立, 故 $\alpha_{1}$ 为 $\alpha$ 在 $U$ 上的正交投影

**定义**: 设 $U$ 是实内积空间 $V$ 的一个子空间, 对于 $\alpha\in V$ , 如果存在 $\delta\in U$ , 使得 $$d(\alpha,\delta)\leq d(\alpha,\gamma),\qquad\forall\,\gamma\in U$$那么称 $\delta$ 是 $\alpha$ 在 $U$ 上的**最佳逼近元**
若内积空间的**无限维子空间**存在唯一最佳逼近元 $\delta$ , 就将 $\delta$ 称为 $\alpha$ 在该子空间上的的**正交投影**

### 最小二乘法

旨在研究变量 $y$ 随变量 $x_{1},x_{2},...,x_{n}$ 间关系，认定用线性拟合合理的情况下，假定线性关系为 $$y=k_{1}x_{1}+k_{2}x_{2}+\cdots+k_{n}x_{n}$$此处 $k_{1},k_{2},...,k_{n}$ 待定，给定若干组 $y$ 和 $(x_{1},x_{2},\cdots,x_{n})$ 的值可以求出 $k_{1},k_{2},...,k_{n}$ 
设给定的不等价的数据组数为 $m$ 
当 $m=n$ 时，可以完全解出待定参数，但必定存在与实际关系的误差
当增加数据量时，得出的关系会更加可靠，但 $m>n$ 时却不一定能够解出 $k_{1},k_{2},...,k_{n}$ 
因此用可以最小化误差的一组参数用以拟合

设 $y$ 的 $m$ 个取值为 $b_{1},...,b_{m}$ 
$(x_{1},x_{2},\cdots,x_{n})$ 的 $m$ 个取值为 $(a_{11},a_{12},\cdots,a_{1n})$ , $(a_{21},a_{22},\cdots,a_{2n})$ , $\cdots$ , $(a_{m1},a_{m2},\cdots,a_{mn})$
即有线性方程组 $$\begin{cases}a_{11}k_{1}+a_{12}k_{2}+\cdots+a_{1n}k_{n}=b_{1}\\a_{21}k_{1}+a_{22}k_{2}+\cdots+a_{2n}k_{n}=b_{2}\\\cdots\qquad\cdots\qquad\cdots\qquad\cdots\\a_{m1}k_{1}+a_{m2}k_{2}+\cdots+a_{mn}k_{n}=b_{m}\end{cases}\tag{E}$$
若能找到一组数 $c_{1},c_{2},...,c_{n}$ 使得: $$\sum\limits_{i=1}^{m}(a_{i1}c_{1}+a_{i2}c_{2}+\cdots+a_{in}c_{n}-b_{i})^{2}\leq\sum\limits_{i=1}^{m}(a_{i1}k_{1}+a_{i2}k_{2}+\cdots+a_{in}k_{n}-b_{i})^{2},\quad\forall\,k_{1},k_{2},\cdots,k_{n}\in\mathbb{R}$$则将 $(c_{1},c_{2},\cdots,c_{n})^{'}$ 称为线性方程组 $(\mathrm{E})$ 的**最小二乘解**

**解决**: 将表达式看作 $\mathbb{R}^{m}$ 中的向量的长度的平方, 此向量的第 $i$ 个分量为 $$a_{i1}c_{1}+a_{i2}c_{2}+\cdots+a_{in}c_{n}-b_{i},\qquad i=1,2,...,m\tag{Ri}$$若记 $(\mathrm{E})$ 的系数矩阵为 $A$ , $A$ 的列向量组为 $\alpha_{1},\alpha_{2},...,\alpha_{n}$ , 行向量组为 $\gamma_{1},\gamma_{2},...,\gamma_{m}$ , 再令 $$x=(k_{1},k_{2},\cdots,k_{n})^{'},
\beta=(b_{1},b_{2},\cdots,b_{m})^{'},\alpha=(c_{1},c_{2},\cdots,c_{n})^{'}$$那么 $(\mathrm{Ri})$ 为 $\gamma_{i}\alpha-b_{i}$ , 所要考虑的向量就是 $$\begin{bmatrix}(\mathrm{R1})\\(\mathrm{R2})\\\vdots\\(\mathrm{Rm})\end{bmatrix}=\begin{bmatrix}\gamma_{1}\alpha-b_{1}\\\gamma_{2}\alpha-b_{2}\\\vdots\\\gamma_{m}\alpha-b_{m}\end{bmatrix}=\begin{bmatrix}\gamma_{1}\\\gamma_{2}\\\vdots\\\gamma_{m}\end{bmatrix}\alpha-\begin{bmatrix}b_{1}\\b_{2}\\\vdots\\b_{m}\end{bmatrix}=A\alpha-\beta$$因此, 只需 $$|A\alpha-\beta|\leq|Ax-\beta|$$记 $U=\langle\alpha_{1},\alpha_{2},\cdots,\alpha_{n}\rangle$ , 则 $Ax=k_{1}\alpha_{1}+k_{2}\alpha_{2}+\cdots+k_{n}\alpha_{n}\in U$ , 那么: $$\begin{align}&\qquad\alpha是线性方程组Ax=\beta的最小二乘解\\&\iff|A\alpha-\beta|^{2}\leq|Ax-\beta|^{2}\\&\iff d(A\alpha,\beta)\leq d(Ax,\beta)\\&\iff d(A\alpha,\beta)\leq d(\gamma,\beta),\:\forall\,\gamma\in U\\&\iff A\alpha是 \beta在U上的正交投影\\&\iff\beta-A\alpha\in U^{\perp}\\&\iff(\beta-A\alpha,\alpha_{i})=0,\:i=1,2,...,n\\&\iff\alpha_{i}^{T}(\beta-A\alpha)=0\\&\iff A^{T}(\beta-A\alpha)=0\\&\iff A^{T}A\alpha=A^{T}\beta\\&\iff\alpha为线性方程组A^{T}Ax=A^{T}\beta的解\end{align}$$方程组 $A^{T}Ax=A^{T}\beta$ 解的存在性取决于增广矩阵与系数矩阵的秩
而 $\mathrm{rank}(A^{T}A)\leq\mathrm{rank}(A^{T}A,A^{T}\beta)=\mathrm{rank}(A^{T}(A,\beta))\leq\mathrm{rank}(A,\beta)\leq\mathrm{rank}(A)=\mathrm{rank}(A^{T}A)$
故 $\mathrm{rank}(A^{T}A,A^{T}\beta)=\mathrm{rank}(A^{T}A)$ , 方程组必然有解

## 内积空间的同构

**定义**: 设 $V$ 和 $V^{'}$ 都是内积空间, 若存在 $V$ 到 $V^{'}$ 的一个满射 $\sigma$ , 使得 $$(\sigma(\alpha),\sigma(\beta))=(\alpha,\beta)$$则称 $\sigma$ 为 $V$ 到 $V^{'}$ 的一个**保距同构(映射)**, 称 $V$ 和 $V^{'}$ 是**保距同构的**, 记作 $V\cong V^{'}$

**性质**: 
	$(1)$ $\sigma$ 保持向量长度不变, 即 $\sqrt{(\sigma(\alpha),\sigma(\alpha))}=\sqrt{(\alpha,\alpha)}$ 
	$(2)$ $\sigma$ 是 $V$ 到 $V^{'}$ 的一个线性映射, 即 $\sigma\in\mathrm{Hom}(V,V^{'})$ 
	$(3)$ $\sigma$ 为单射 (结合定义因此 $\sigma$ 为满射)

因此，保距同构还有一个等价的定义：

**定义**: 设内积空间 $V$ 和 $V^{'}$ , 如果存在一个 $V$ 到 $V^{'}$ 的双射 $\sigma$ , 使得 $\forall\,\alpha,\beta\in V$ , $k\in\mathbb F$ , 有 $$\begin{align}\sigma(\alpha+\beta)&=\sigma(\alpha)+\sigma(\beta)\\\sigma(k\alpha)&=k\sigma(\alpha)\\(\sigma(\alpha),\sigma(\beta))&=(\alpha,\beta)\end{align}$$则称 $\sigma$ 为 $V$ 到 $V^{'}$ 的一个**保距同构(映射)**, 称 $V$ 和 $V^{'}$ 是**保距同构的**, 记作 $V\cong V^{'}$ 

简而言之，保距同构就是在线性同构的基础上由附加了保内积的条件，也即

**命题**: 设 $V$ 和 $V^{'}$ 都是 $n$ 维内积空间, 若 $V$ 到 $V^{'}$ 的一个同构映射 $\sigma$ 保持向量的内积不变, 即 $$(\sigma(\alpha),\sigma(\beta))=(\alpha,\beta),\qquad\forall\,\alpha,\beta\in V$$那么 $\sigma$ 是 $V$ 到 $V^{'}$ 的一个保距同构

**命题**: 设 $\sigma$ 为内积空间 $V$ 到 $V^{'}$ 的保持范数不变的线性映射, 则它同样保内积, 进而为保距同构
**[证明]**:
	任取 $x,y\in V$ , 由题应有 $$\begin{align}||x+y||^{2}&=(x+y,x+y)=(x,x)+(x,y)+(y,y)+(y,x)\\||x-y||^{2}&=(x-y,x-y)=(x,x)-(x,y)+(y,y)-(y,x)\end{align}$$两式相减, 由此得到 $$||x+y||^{2}-||x-y||^{2}=2(x,y)+2(y,x)=2(x,y)+2\overline{(x,y)}$$另一方面 $$\begin{align}||x+iy||^{2}&=(x+iy,x+iy)=(x,x)+i(x,y)-(y,y)+i(y,x)\\||x-iy||^{2}&=(x-iy,x-iy)=(x,x)-i(x,y)-(y,y)-i(y,x)\end{align}$$两式相减, 由此得到 $$||x+iy||^{2}-||x-iy||^{2}=2i(x,y)+2i\overline{(x,y)}$$现在可以解得 $$(x,y)=\frac{||x+y||^{2}-||x-y||^{2}+i||x+iy||^{2}-i||x-iy||^{2}}{4}$$这说明内积可以由范数表示, 自然由保范数可得到保内积

**定理**: 两个内积空间保距同构的充要条件是它们的维数相等

_保距同构 $\cong$ 为所有实内积空间组成的集合上的一个等价关系_

由上可知
$(1)$ 所有 $n$ 维Euclid空间都与 $R^n$ 保距同构
这个保距同构映射即为 $$
\begin{align}\sigma:\qquad V&\longrightarrow R^n\\\\alpha=\sum_{i=1}^nx_i\eta_i&\longmapsto(x_1,x_2,\cdots,x_n)^{'}\end{align}
$$这里 $\eta_1,\eta_2,...,\eta_n$ 为 $V$ 的一个标准正交基
$(2)$ 所有 $n$ 维酉空间都与 $C^n$ 保距同构
这个保距同构映射即为 $$\begin{align}\sigma:\qquad V&\longrightarrow C^n\\\alpha=\sum_{i=1}^nx_i\eta_i&\longmapsto(x_1,x_2,\cdots,x_n)^{'}\end{align}$$这里 $\eta_1,\eta_2,...,\eta_n$ 为 $V$ 的一个标准正交基

若 $\sigma$ 为保距同构，则 $\sigma^{-1}$ 也为保距同构

**推论**: 设 $V$ 为 $n$ 维内积空间, 则 $V$ 上的线性变换 $\mathscr A$ 是 $V$ 到自身的保距同构当且仅当 $\mathscr A$ 将 $V$ 的标准正交基映射为标准正交基
**[证明]**:

**定义**: 设 $\sigma$ 为内积空间 $V$ 上保内积的线性变换, 若 $V$ 为欧式空间, 则称 $\sigma$ 为**正交变换**或是**正交算子**; 若 $V$ 为酉空间, 则称 $\sigma$ 为**酉变换**或**酉蒜子**

**定理**: 设 $\sigma$ 是欧式空间或酉空间上的线性变换, 则 $\sigma$ 为正交变换或酉变换的充要条件是 $\sigma$ 非异, 并且有 $$\sigma^{*}=\sigma^{-1}$$
**定义**: 设 $A$ 为 $n$ 阶实方阵, 若 $A^{'}=A^{-1}$ , 则称 $A$ 为**正交矩阵**; 若 $C$ 为 $n$ 阶复方阵, 若 $C^{*}=C^{-1}$ , 这里 $*$ 表示共轭转置, 则称 $C$ 为**酉矩阵**

**定理**: 设 $\sigma$ 为欧式空间(酉空间) $V$ 上的正交变换(酉变换), 则在 $V$ 的任意一组标准正交基下的矩阵为正交矩阵(酉矩阵)

**定理**: 设 $A=(a_{ij})$ 为 $n$ 阶方阵, 则
	$(1)$ 若 $A$ 为实矩阵, 则 $A$ 为正交矩阵当且仅当 $$\sum\limits_{k=1}^{n}a_{ki}a_{kj}=\delta_{ij}\qquad或\qquad\sum\limits_{k=1}^{n}a_{ik}a_{jk}=\delta_{ij}$$$(2)$ 若 $A$ 为复方阵, 则 $A$ 为酉矩阵当且仅当 $$\sum\limits_{k=1}^{n}a_{ki}\overline{a_{kj}}=\delta_{ij}\qquad或\qquad\sum\limits_{k=1}^{n}a_{ik}\overline{a_{jk}}=\delta_{ij}$$即它们的行(列)向量组都必须为对应 $n$ 维空间内的标准正交基

**定理**: 若 $n$ 阶实矩阵 $A$ 为正交矩阵, 则
	$(1)$ $|A|=1或-1$
	$(2)$ $A$ 的特征值的模长为 $1$

**定理**: 若 $n$ 阶复矩阵 $A$ 为酉矩阵, 则
	$(1)$ $|A|$ 的模长为 $1$
	$(2)$ $A$ 的特征值的模长为 $1$

**定理·QR分解**: 设 $A$ 为 $n$ 阶实(复)矩阵, 则 $A$ 可分解为 $$A=QR$$其中 $Q$ 为正交(酉)矩阵, $R$ 为一个主对角线上的元素均大于等于零的上三角阵, 如果 $A$ 是非奇异阵, 则该分解方式唯一


## 伴随

设 $V$ 为 $n$ 维内积空间，不妨设其为酉空间，取 $V$ 的一组标准正交基 $e_1,e_2,...,e_n$ , 设 $\varphi$ 为 $V$ 上的线性变换，且其在该基下的矩阵为 $A=(a_{ij})_{n\times n}$ 
设 $\alpha=\sum_{i=1}^nx_ie_i$ , $\beta=\sum_{i=1}^ny_ie_i$ , 记 $x=(x_1,x_2,\cdots,x_n)^{'}$ , $y=(y_1,y_2,\cdots,y_n)^{'}$ , 则$$(\varphi(\alpha),\beta)=y^*Ax=(A^{'}\overline{y})^{'}x=(\overline{(A^{'}\overline{y})})^*x=(A^*y)^*x$$
这里 $A^*$ 表示共轭转置
记 $\psi$ 为 $A^*$ 表示的线性变换，设 $\psi(\beta)=\sum_{i=1}^nz_ie_i=(e_1,e_2,\cdots,e_n)z$ ，
这里**定义有** $z_k=\sum_{i=1}^n\overline{A}(i;k)y_i=\sum_{i=1}^n\overline{a}_{ik}y_i$ 
则 $$(z_1,z_2,\cdots,z_n)^{'}=A^*(y_1,y_2,\cdots,y_n)^{'}=A^*y$$总之有 $z=A^*y$ ，因此 $\psi(\beta)=IA^*y=A^*y$  
于是 $$(\varphi(\alpha),\beta)=(A^*y)^*x=(\psi(\beta))^*x=(\alpha,\psi(\beta))$$该式对一切 $\alpha,\beta$ 成立，这里就证明了下面定理中**伴随算子**的存在性
并且伴随算子在基 $e_{1},e_{2},...,e_{n}$ 下表示的矩阵恰为 $A^{*}$

**定义**: 设 $\varphi$ 为内积空间 $V$ 上的线性算子, 若存在 $V$ 上的线性算子 $\varphi^*$ , 使得 $$(\varphi(\alpha),\beta)=(\alpha,\varphi^*(\beta))$$对任意 $\alpha,\beta\in V$ 成立, 则称 $\varphi^*$ 为 $\varphi$ 的**伴随算子**, 简称为 $\varphi$ 的**伴随**

**定理**: 设 $V$ 为 $n$ 维的内积空间, $\varphi$ 为 $V$ 上的线性变换, 则存在 $V$ 上的唯一线性变换 $\varphi^*$ , 使得 $\forall\,\alpha,\beta\in V$ , 有下式成立 $$(\varphi(\alpha),\beta)=(\alpha,\varphi^*(\beta))$$**[证明]**:
	存在性开头已经说明, 下面证明唯一性
	如若还存在线性变换 $\varphi^{**}$ 为 $\varphi$ 的伴随, 那么 $\forall\,\alpha,\beta\in V$ , 有 $$(\varphi(\alpha),\beta)=(\alpha,\varphi^{*}(\beta))=(\alpha,\varphi^{**}(\beta))$$进而得到 $$(\alpha,\varphi^{*}(\beta)-\varphi^{**}(\beta))=0$$取 $\alpha=\varphi^{*}(\beta)-\varphi^{**}(\beta)$ , 得到 $$(\varphi^{*}(\beta)-\varphi^{**}(\beta),\varphi^{*}(\beta)-\varphi^{**}(\beta))=||\varphi^{*}(\beta)-\varphi^{**}(\beta)||^{2}=0$$由正定性立即得到 $\varphi^{*}(\beta)=\varphi^{**}(\beta)$ , 由 $\beta$ 的任意性即得 $\varphi^{*}=\varphi^{**}$

在实内积空间中，在同一组基下，伴随算子的矩阵为原算子的矩阵的转置矩阵
在酉空间中，在同一组基下，伴随算子的矩阵为原算子的矩阵的共轭转置矩阵

**定理**: 若 $V$ 为有限维内积空间, 若 $\varphi$ 以及 $\psi$ 为 $V$ 上的线性变换, $c$ 为常数, 则: 
	$(1)$ $(\varphi+\psi)^*=\varphi^*+\psi^*$ 
	$(2)$ $(c\varphi)^*=\overline{c}\varphi^*$ 
	$(3)$ $(\varphi\psi)^*=\psi^*\varphi^*$ 
	$(4)$ $(\varphi^*)^*=\varphi$

**命题**: 设 $V$ 为 $n$ 维内积空间, $\varphi$ 是 $V$ 上的线性算子
	$(1)$ 若 $U$ 为 $\varphi$ 的不变子空间, 则 $U^{\perp}$ 为 $\varphi^*$ 的不变子空间
	$(2)$ 若 $\varphi$ 的全体特征值为 $\lambda_1,\lambda_2,...,\lambda_n$ , 则 $\varphi^*$ 的全体特征值为 $\overline{\lambda_1},\overline{\lambda_2},...,\overline{\lambda_n}$
**[证明]**:
	$(1)$ 任取 $\alpha\in U$ , $\beta\in U^{\perp}$ , 由于 $$(\alpha,\varphi^{*}(\beta))=(\varphi(\alpha),\beta)=0$$故 $U^{\perp}$ 为 $\varphi^{*}$ 的不变子空间
	$(2)$ 取 $V$ 的一组标准正交基, 设 $\varphi$ 在该基下表示矩阵为 $A$ , 则 $\varphi^{*}$ 的表示矩阵总为 $\bar{A}^{'}$ 
	应有
	$|\lambda I_{n}-A|=(\lambda-\lambda_{1})(\lambda-\lambda_{2})\cdots(\lambda-\lambda_{n})$
	验证可得
	$|\lambda I_{n}-\bar{A}^{'}|=(\lambda-\overline{{\lambda_{1}}})(\lambda-\overline{\lambda_{2}})\cdots(\lambda-\overline{\lambda_{n}})$
	即证

## 自伴随算子

**引理**: 欧式空间中两组标准正交基间的过渡矩阵是正交矩阵, 酉空间中两组标准正交基间的过渡矩阵是酉矩阵


**定义**: 设 $A,B$ 是 $n$ 阶实矩阵, 若存在正交矩阵 $P$ , 使 $B=P^{'}AP$ , 则称 $B$ 和 $A$ **正交相似**; 若 $A,B$ 是 $n$ 阶复矩阵, 若存在酉矩阵 $P$ , 使 $B=P^{*}AP$ , 则称 $B$ 和 $A$ **酉相似**

可以证明，正交相似和酉相似都是等价关系

**定义**: 设 $\varphi$ 为内积空间 $V$ 上的线性变换, $\varphi^{*}$ 为 $\varphi$ 的伴随, 若 $\varphi^{*}=\varphi$ , 则称 $\varphi$ 为**自伴随算子**. 当 $V$ 是欧式空间时, $\varphi$ 也称为**对称算子**或是**对称变换**; 当 $V$ 为酉空间时, $\varphi$ 也称为**Hermite算子**或**Hermite变换**

_例：若 $V=U\oplus U^{\perp}$ ，则 $V$ 到 $U$ 的投影变换为一个自伴随算子（见正交补空间中命题）_

**定理**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 是 $V$ 上的自伴随算子, 则 $\varphi$ 的特征值全是实数且属于不同特征值的特征向量相互正交
**[证明]**:
	设 $\lambda$ 为 $\varphi$ 的特征值, $x$ 是属于 $\lambda$ 的特征向量, 则 $$\lambda(x,x)=(\lambda x,x)=(\varphi(x),x)=(x,\varphi(x))=(x,\lambda x)=\overline{(\lambda x,x)}=\overline{\lambda}(x,x)$$由于 $x\neq0$ , 故 $(x,x)\neq0$ , 因此 $\lambda=\overline{\lambda}$ , 这就得到了 $\lambda\in\mathbb{R}$
	设 $\mu$ 为异于 $\lambda$ 的特征值, $y$ 为属于 $\mu$ 的特征向量, 则 $$(\lambda-\mu)(x,y)=(\lambda x-\mu x,y)=(\lambda x,y)-(\mu x,y)=(\varphi(x),y)-(x,\mu y)=(x,\varphi(y))-(x,\varphi(y))=0$$由于 $(\lambda-\mu)\neq0$ , 故 $(x,y)=0$ , 即 $x$ 和 $y$ 正交

**推论**: Hermite矩阵的特征值全为实数, 实对称阵的特征值也全为实数, 且这两种矩阵属于不同特征值下的特征向量互相正交

**定理**: 设 $V$ 为 $n$ 为内积空间, $\varphi$ 为 $V$ 上的自伴随算子, 则存在 $V$ 的一组标准正交基, 使 $\varphi$ 在这组基下的矩阵为实对角阵, 且这组基恰为 $\varphi$ 的 $n$ 个线性无关的特征向量

**定理**: 设 $A$ 为 $n$ 阶实对称阵, 则存在正交矩阵 $P$ , 使得 $P^{'}AP$ 为对角矩阵, 且 $P$ 的 $n$ 个列向量恰为 $A$ 的 $n$ 个两两正交的单位特征向量; 设 $A$ 为 $n$ 阶Hermite阵, 则存在酉矩阵 $P$ , 使得 $P^{*}AP$ 为实对角矩阵, 且 $P$ 的 $n$ 个列向量恰为 $A$ 的 $n$ 个两两正交的单位特征向量
即**实对称矩阵必然可以正交相似对角化**, **Hermite阵必然可以酉相似对角化**

**推论**: 实对称阵(Hermite阵)的全体特征值是实对阵矩阵(Hermite阵)在正交相似(酉相似)关系下的全系不变量

**定理**: 设 $f(x)=x^{'}Ax$ 为 $n$ 元实二次型, 系数矩阵 $A$ 的特征值为 $\lambda_{1},\lambda_{2},...,\lambda_{n}$ , 则 $f$ 经过正交变换 $x=Py$ 可以化为下列标准型: $$\lambda_{1}y_{1}^{2}+\lambda_{2}y_{2}^{2}+\cdots+\lambda_{n}y_{n}^{2}$$因此, $f$ 的正惯性指数就为 $A$ 的正特征值的个数, 负惯性指数就为 $A$ 的负特征值的个数, $f$ 的秩就为 $A$的非零特征值的个数
**[证明]**:
	因为正交相似关系显然包含了相似和合同, 故显然

## 正规算子

### 复正规算子

如果一个 $n$ 维酉空间上的线性变换 $\varphi$ 在一组标准正交基下的矩阵为对角阵，需要 $\varphi$ 满足什么条件？
设 $V$ 的标准正交基为 $\{e_{1},e_{2},\cdots,e_{n}\}$ ，并假设 $\varphi$ 在该组基下的矩阵为 $$A=\mathrm{diag}\{c_{1},c_{2},\cdots,c_{n}\}$$则有 $$\varphi(e_{i})=c_{i}e_{i}$$也即 $\varphi$ 以 $c_{1},c_{2},...,c_{n}$ 为特征值，以 $e_{1},e_{2},...,e_{n}$ 为对应的特征向量，设 $\varphi^{*}$ 为 $\varphi$ 的伴随，则已知 $\varphi^{*}$ 在该组基下的矩阵为 $A^{*}=\mathrm{diag}\{\bar{c_{1}},\bar{c_{2}},\cdots,\bar{c_{n}}\}$ ，于是有 $$A^{*}A=AA^{*},\:\varphi\varphi^{*}=\varphi^{*}\varphi$$
**定义**: 设 $\varphi$ 为内积空间 $V$ 上的线性变换, $\varphi^{*}$ 为其伴随, 若 $\varphi\varphi^{*}=\varphi^{*}\varphi$ , 则称 $\varphi$ 为 $V$ 上的**正规算子**, 特别地, 通常称酉空间(欧式空间) $V$ 上的正规算子为**复正规算子**(**实正规算子**). 同样的, 若复矩阵 $A$ 符合 $A^{*}A=AA^{*}$ , 则称 $A$ 为**复正规矩阵**; 若实矩阵 $A$ 符合 $A^{'}A=AA^{'}$ , 则称 $A$ 为**实正规矩阵**

**引理**: 设 $\varphi$ 为内积空间 $V$ 上的正规算子, 则对任意的 $\alpha\in V$ , 有 $$||\varphi(\alpha)||=||\varphi^{*}(\alpha)||$$**[证明]**:
	由于 $\varphi\varphi^{*}=\varphi^{*}\varphi$ , 故 $$||\varphi(\alpha)||^{2}=(\varphi(\alpha),\varphi(\alpha))=(\alpha,\varphi^{*}\varphi(\alpha))=(\alpha,\varphi\varphi^{*}(\alpha)=(\varphi^{*}(\alpha),\varphi^{*}(\alpha))=||\varphi^{*}(\alpha)||^{2}$$即证

**命题**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 为 $V$ 上的正规算子
	$(1)$ 向量 $u$ 是 $\varphi$ 的属于特征值 $\lambda$ 的特征向量的充要条件为 $u$ 是属于 $\varphi^{*}$ 的特征值 $\bar{\lambda}$ 的特征向量
	$(2)$ 属于 $\varphi$ 不同特征值的特征向量必然正交
**[证明]**
	$(1)$ 若 $\lambda$ 为数域内的数, 则 $(\lambda I-\varphi)^{*}=\bar{\lambda}I-\varphi^{*}$ , 且 $$(\lambda I-\varphi)(\bar{\lambda}I-\varphi^{*})=(\bar{\lambda}I-\varphi^{*})(\lambda I-\varphi)$$说明 $(\lambda I-\varphi)$ 也为正规算子
	那么对任意的 $\alpha\in V$ , 有 $$||(\lambda I-\varphi)(\alpha)||=||(\bar{\lambda}I-\varphi^{*})(\alpha)||$$这就说明 $$(\lambda I-\varphi)(u)=0\iff(\bar{\lambda}I-\varphi^{*})(u)$$即证
	$(2)$ 设 $\lambda,\mu$ 为 $\varphi$ 的不同特征值, $x$ 和 $y$ 分别为属于特征值 $\lambda$ , $\mu$ 的特征向量, 那么 $$\lambda(x,y)=(\lambda x,y)=(\varphi(x),y)=(x,\varphi^{*}(y))=(x,\bar{\mu} y)=\mu(x,y)$$由于 $\lambda\neq\mu$ , 故 $(x,y)=0$

**引理**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 是 $V$ 上的线性变换, 又 $\{e_{1},e_{2},\cdots,e_{n}\}$ 是 $V$ 的一组标准正交基, 设 $\varphi$ 在这组基下的矩阵 $A$ 为上三角阵, 则 $\varphi$ 是正规算子的充要条件是 $A$ 为对角阵
**[证明]**:
	设 $A=(a_{ij})$ , $a_{ij}=0\,(i>j)$ , 则应有 $\varphi(e_{1})=a_{11}e_{1}$ , $\varphi^{*}(e_{1})=\overline{a_{11}}e_{1}$ , 又有 $$\overline{a_{11}}e_{1}=\varphi^{*}(e_1)=\sum\limits_{i=1}^{n}\overline{A^{'}(i;1)}e_{i}=\sum\limits_{i=1}^{n}\overline{a_{1i}}e_{i}$$得到 $$\overline{a_{12}}e_{2}+\cdots+\overline{a_{1n}}e_{n}=0$$故 $a_{1k}=0$ , $k\neq1$
	其实可以对矩阵阶数(空间维数)归纳, $1$ 阶时显然成立, 假设 $k-1$ 阶成立, 则对于 $k$ 阶矩阵 $$\begin{bmatrix}a_{11}&a_{12}&\cdots&a_{1k}\\0&a_{22}&\cdots&a_{2k}\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&a_{kk}\end{bmatrix}$$由上面的讨论得出 $a_{1k}=0$ , $k\neq1$ , 即形如 $$\begin{bmatrix}a_{11}&0&\cdots&0\\0&a_{22}&\cdots&a_{2k}\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&a_{kk}\end{bmatrix}=\begin{bmatrix}a_{11}&\mathbf{0}\\\mathbf{0}&A_{k-1}\end{bmatrix}$$由归纳假设, 对于 $e_{2},...,e_{k}$ 生成的 $k-1$ 维空间成立, 即 $A_{k-1}$ 应为对角阵, 故对于 $k$ 维时的 $k$ 阶矩阵成立, 进而对于任意阶矩阵成立

**定理·Schur分解**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 是 $V$ 上的线性算子, 则存在 $V$ 的一组标准正交基, 使 $\varphi$ 在该组基下的矩阵为上三角阵, 即**复矩阵必然可正交相似上三角化**
**[证明]**
	对 $V$ 的维数归纳, $n=1$ 时显然成立
	假设对 $n-1$ 维的酉空间结论成立, 那么对于 $n$ 维酉空间, $\varphi^{*}$ 总有特征值和特征向量, 设 $$\varphi^{*}(e)=\lambda e$$记 $W=\langle e\rangle^{\perp}$ , 则 $V=\langle e\rangle\oplus W$ , $W$ 为 $(\varphi^{*})^{*}=\varphi$ 的不变子空间, 由归纳假设, $\varphi|_{W}$ 在 $n-1$ 维空间 $W$ 上存在一组标准正交基 $e_{1},...e_{n-1}$ 使得 $\varphi|_{W}$ 在该组基下的矩阵为 $n-1$ 阶的上三角矩阵, 在记 $e_{n}=\frac{e}{||e||}$ , 则 $\varphi$ 在基 $e_{1},e_{2},...,e_{n}$ 下的矩阵为上三角矩阵
	即证

**定理**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 是 $V$ 上的线性算子, 则 $\varphi$ 为正规算子的充要条件是存在一组 $V$ 的标准正交基, 使得 $\varphi$ 在该组基下的矩阵为对角矩阵, 这组基恰为 $\varphi$ 的 $n$ 个线性无关的特征向量
**[证明]**
	上面两个定理的直接推论

**定理**: 复矩阵 $A$ 为复正规矩阵当且仅当 $A$ 酉相似于对角阵

**命题**: 设 $\varphi$ 是 $n$ 维酉空间 $V$ 上的线性算子, $\lambda_{1},\lambda_{2},...,\lambda_{k}$ 是 $\varphi$ 的全体不同特征值, $V_{1},V_{2},...,V_{k}$ 为对应的特征子空间, 则 $\varphi$ 为正规算子当且仅当 $$V=V_{1}\perp V_{2}\perp\cdots\perp V_{k}$$**[证明]**:
	设 $\varphi$ 为正规算子, 则 $\varphi$ 可对角化, 故 $$V=V_{1}\oplus V_{2}\oplus\cdots\oplus V_{k}$$而不同特征值的特征向量正交, 故有 $V_{i}\perp V_{j}$ , $i\neq j$
	反之, 可以在每个特征子空间里选取一组标准正交基, 将它们合起来会成为 $V$ 的一组标准正交基, 由于它们都是特征向量, 因而 $\varphi$ 在该基下的矩阵即为对角矩阵, 故 $\varphi$ 为正规算子

**定理**: 任意 $n$ 阶酉矩阵必定酉相似于如下对角阵 $$\mathrm{diag}\{c_{1},c_{2},\cdots,c_{n}\}$$其中 $c_{i}$ 为模长为 $1$ 的复数
**[证明]**:
	因为复正规矩阵必然酉相似于其特征值的对角矩阵, 而酉矩阵的特征值模长均为 $1$ , 即证

总之，对于复正规矩阵，酉相似标准型便为对角矩阵，对于实正规矩阵，其正交相似标准型是否还会如此简洁？

### 实正规算子

**引理**: 设 $V$ 为 $n$ 维欧式空间, $f(x)$ 为一个实系数多项式, 若 $\varphi$ 是 $V$ 上的正规算子, 则 $f(\varphi)$ 也为 $V$ 上的正规算子
**[证明]**:
	通过正规算子与其伴随算子的可交换性, 可知它们的多项式可交换, 总之结论是显然的

**引理**: 设 $\varphi$ 是欧式空间 $V$ 上的正规算子, 实系数多项式 $f(x),g(x)$ 满足 $(f(x),g(x))=1$ , 则若 $u\in\mathrm{Ker}\,f(\varphi)$ , $v\in\mathrm{Ker}\,g(\varphi)$ , 那么就有 $$(u,v)=0$$

## 谱分解与极分解

设 $n$ 维酉空间，$\varphi$ 是 $V$ 上的正规算子，$\lambda_{1},\lambda_{2},\cdots,\lambda_{k}$ 为 $\varphi$ 的全体不同特征值, 则必然存在 $V$ 上的一组标准正交基，使得 $\varphi$ 在这组基下的表示矩阵为对角阵 $$A=\mathrm{diag}\{\lambda_1,\cdots,\lambda_{1};\lambda_{2},\cdots,\lambda_{2};\lambda_{k},\cdots,\lambda_{k}\}$$假设特征值 $\lambda_{i}$ 的重数为 $r_{i}$ ，则在分解式 $$V=W_{1}\perp W_{2}\perp\cdots\perp W_{k}$$中，$W_{i}$ 是 $\varphi$ 的 $r_{i}$ 维特征子空间，记矩阵 $$D_{i}=\mathrm{diag}\{0,\cdots,0;\cdots;\underbrace{1,\cdots,1}_{r_{i}个1};\cdots;0,\cdots,0\}$$即应有 $$A=\lambda_{1}D_{1}+\lambda_{2}D_{2}+\cdots+\lambda_{k}D_{k}$$并且满足 $$D_{i}D_{j}=\delta_{ij}D_{i}\qquad\qquad\sum\limits_{i=1}^{k}D_{i}=I_{n}$$_$D_{i}$ 和投影变换有相同的性质，实际上可以看到 $D_{i}$ 正是投影变换_

总之，这就是下面的定理：

**定理·谱分解**: 设 $V$ 为有限维内积空间, $\varphi$ 是 $V$ 上的线性算子, 当 $V$ 是酉空间时, $\varphi$ 为正规算子; 当 $V$ 是欧式空间时, $\varphi$ 为自伴随算子. 设 $\lambda_{1},\lambda_{2},...,\lambda_{k}$ 是 $\varphi$ 的全体不同特征值, $W_{i}$ 为 $\varphi$ 属于 $\lambda_{i}$ 的特征子空间, 则 $V$ 为 $W_{1},W_{2},...,W_{k}$ 的正交直和, 设 $E_{i}$ 是 $V$ 到 $W_{i}$ 上的正交投影, 则有分解式 $$\varphi=\lambda_{1}E_{1}+\lambda_{2}E_{2}+\cdots+\lambda_{k}E_{k}$$**[证明]**: 
	已知有 $$V=W_{1}\perp W_{2}\perp\cdots\perp W_{k}$$而 $E_{i}$ 为 $W$ 到 $W_{i}$ 的正交投影, 故有 $$I=E_{1}+E_{2}+\cdots+E_{k}$$而另一方面实际上有 $\varphi E_{i}=\lambda_{i}E_{i}$ , 这是因为 $\forall\,\alpha\in V$ , $\alpha=\alpha_{1}+\alpha_{2}+\cdots+\alpha_{k}$ , $\alpha_{i}\in W_{i}$
	有 $$\varphi E_{i}(\alpha)=\varphi E_{i}(\alpha_{1})+\cdots+\varphi E_{i}(\alpha_{i})+\cdots+\varphi E_{i}(\alpha_{k})=\varphi E_{i}(\alpha_{i})=\lambda_{i}E_{i}(\alpha_{i})=\lambda_{i}E_{i}(\alpha)$$那么就有 $$\varphi=\varphi E_{1}+\varphi E_{2}+\cdots+\varphi E_{k}=\lambda_{1}E_{1}+\lambda_{2}E_{2}+\cdots+\lambda_{k}E_{k}$$

_为什么 $V$ 为不同空间时，符合定理条件 $\varphi$ 的类型不一样？因为酉空间中的复正规算子一定可以酉相似对角化，而欧式空间中的实正规算子却不一定有实特征值和实特征向量，也就不一定可以正交相似对角化；但欧式空间中的自伴随算子（实对称矩阵）却一定可以正交相似对角化_


## 奇异值分解

[[矩阵分解]]技巧还有很多，奇异值分解更是其中的明珠，在图片压缩、主成分分析等方面应用广泛

**定义**: 设 $A$ 为 $m\times n$ 实矩阵, 如果存在非负实数 $\sigma$ 及 $n$ 维非零实列向量 $\alpha$ , $m$ 维非零实列向量 $\beta$ , 使得 $$A\alpha=\sigma\beta,\qquad A^{\mathrm T}\beta=\sigma\alpha$$将 $\sigma$ 称为 $A$ 的**奇异值**, $\alpha$ , $\beta$ 分别称为 $A$ 关于 $\sigma$ 的**右奇异值向量**和**左奇异值向量**, 

下面将从几何意义上描述奇异值的问题，类似于线性变换中的伴随概念，下面给出一般的线性映射的伴随概念

**定义**: 设 $V,U$ 分别为 $n$  维, $m$ 维Euclid空间, $\varphi$ 是 $V\to U$ 的线性映射, 若有 $U\to V$ 的线性映射 $\varphi^*$ , 使对任意的 $v\in V,u\in U$ , 都有$$(\varphi(v),u)=(v,\varphi^*(u))$$成立, 则称 $\varphi^*$ 是 $\varphi$ 的**伴随**

**定理**: 设 $V,U$ 分别是 $n$ 维, $m$ 维Euclid空间, $\varphi$ 是 $V\to U$ 的线性映射, 则 $\varphi$ 的伴随 $\varphi^*$ 存在且唯一

若取定 $V$ 的基 $v_1,v_2,...,v_n$ ， $U$ 的基 $u_1,u_2,...,u_m$ ，设 $\varphi$ 在这两组基下的矩
：阵为 $A=(\alpha_1,\alpha_2,\cdots,\alpha_n)$ ，则可证明 $\varphi^*$ 在这两组基下的矩阵为 $A^{\mathrm T}$ ，直接构造出即可证明存在性，唯一性类似于线性变换的情况也容易证明

于是奇异值和奇异向量也可以带有几何意义的如下定义$$\varphi(v)=\sigma u,\quad\varphi^*(u)=\sigma v$$这里 $\sigma\geq0$ , $v\in V$ , $u\in U$ 均为非零向量，可以验证 $\varphi^{*}\varphi$ 为 $V$ 上的半正定自伴随算子，$\varphi\varphi^{*}$ 为 $U$ 上的半正定自伴随算子，并且有 $$\begin{align}\varphi^{*}\varphi(v)&=\varphi^{*}(\sigma u)=\sigma^{2}v\\\varphi\varphi^{*}(u)&=\varphi(\sigma v)=\sigma^{2}u\end{align}$$这就说明了 $v$ 为属于特征值 $\sigma^{2}$ 的 $\varphi^{*}\varphi$ 的特征向量， $u$ 为属于特征值 $\sigma^{2}$ 的 $\varphi\varphi^{*}$ 的特征向量

**定理·奇异值分解**: $(i)$ 设 $V,U$ 分别为 $n$ 维, $m$ 维欧式空间, $\varphi$ 是 $V\to U$ 的线性映射, 则存在 $V$ 和 $U$ 的标准正交基, 使得 $\varphi$ 在这两组基下的矩阵为 $$\begin{bmatrix}S&O\\O&O\end{bmatrix}$$其中 $$S=\begin{bmatrix}\sigma_{1}& \ & \ & \ \\ \ &\sigma_{2}&\ &\ \\ \ & \ &\ddots&\ \\ \ &\ &\ &\sigma_r\end{bmatrix}$$是一个 $r$ 阶对角阵, $\sigma_{1}\geq\sigma_{2}\geq\cdots\geq\sigma_{r}>0$ 为 $\varphi$ 的非零奇异值;
$(ii)$ 对于任意的 $m\times n$ 的实矩阵 $A$ , 存在 $m$ 阶正交矩阵 $P$ 及 $n$ 阶正交矩阵 $Q$ , 使得 $$P^{'}AQ=\begin{bmatrix}S&O\\O&O\end{bmatrix}$$其中 $$S=\begin{bmatrix}\sigma_{1}& \ & \ & \ \\ \ &\sigma_{2}&\ &\ \\ \ & \ &\ddots&\ \\ \ &\ &\ &\sigma_r\end{bmatrix}$$是一个 $r$ 阶对角阵, $\sigma_{1}\geq\sigma_{2}\geq\cdots\geq\sigma_{r}>0$ 为 $A$ 的非零奇异值
**[证明]**:
	$(i)$ 由于 $\varphi^{*}\varphi$ 是 $V$ 上的半正定自伴随算子, 故存在 $V$ 上的一组标准正交基 $e_{1},e_{2},...,e_{n}$ 使得 $\varphi^{*}\varphi$ 在该组基下的矩阵为 $n$ 阶对角阵 $\mathrm{diag}\{\lambda_{1},\cdots,\lambda_{r},0,\cdots,0\}$ , 其中 $r=\mathrm{rank}(\varphi^{*}\varphi)=\mathrm{rank}(\varphi)$ 且 $\lambda_{1}\geq\lambda_{2}\geq\cdots\geq\lambda_{r}>0$ 为 $\varphi^{*}\varphi$ 的正特征值, 因而有 $$\varphi^{*}\varphi(e_{i})=\begin{cases}\lambda_{i}e_{i}\qquad&, 1\leq i\leq r\\0\qquad&,r+1\leq i\leq n\end{cases}$$记 $\sigma_{i}=\sqrt{\lambda_{i}}$ , $(i=1,2,...,r)$ , 
	当 $1\leq i\leq r$ 时, 注意到 $$||\varphi(e_{i})||^{2}=(\varphi(e_{i}),\varphi(e_{i}))=(\varphi^{*}\varphi(e_{i}),e_{i})=\lambda_{i}(e_{i},e_{i})=\sigma_{i}^{2}$$得到 $||\varphi(e_{i})||=\sigma_{i}$
	当 $r+1\leq j\leq n$ 时, 有 $$||\varphi(e_{j})||^{2}=(\varphi(e_{j}),\varphi(e_{j}))=(\varphi^{*}\varphi(e_{j}),e_{j})=(0,e_{j})=0$$即 $\varphi(e_{j})=0$
	记 $$f_{i}=\frac{1}{\sigma_{i}}\varphi(e_{i}),\quad i=1,2,...,r$$则 $f_{1},f_{2},...,f_{r}$ 为单位化的两两正交的单位向量组, 将其扩充为 $U$ 的一组标准正交基 $$\{f_{1},f_{2},\cdots,f_{r},f_{r+1},\cdots,f_{m}\}$$现在得到 $$\varphi(e_{i})=\begin{cases}\sigma_{i}f_{i}\qquad&,1\leq i\leq r\\0\qquad&,r+1\leq i\leq n\end{cases}$$以及 $$\varphi^{*}(f_{i})=\begin{cases}\sigma_{i}e_{i}\qquad&,1\leq i\leq r\\0\qquad&,r+1\leq i\leq m\end{cases}$$由于有 $$\varphi(e_{1},e_{2},\cdots,e_{n})=(f_{1},f_{2},\cdots,f_{m})\begin{bmatrix}S&O\\O&O\end{bmatrix}_{m\times n}$$于是 $\varphi$ 在这两组基下的矩阵为 $$S=\begin{bmatrix}\sigma_{1}& \ & \ & \ \\ \ &\sigma_{2}&\ &\ \\ \ & \ &\ddots&\ \\ \ &\ &\ &\sigma_r\end{bmatrix}$$即证
	$(ii)$ 关于矩阵的结论则立即可以得到

将矩阵 $A$ 分解为 $P\begin{bmatrix}S&O\\O&O\end{bmatrix}Q^{'}$ ，称为 $A$ 的**奇异值分解(SVD)**，表示成 $P^{'}AQ=\begin{bmatrix}S&O\\O&O\end{bmatrix}$ , 则叫做 $A$ 的**正交相抵标准型**

**计算奇异值分解的步骤**：
	对于给定的 $m\times n$ 阶矩阵 $A$ , 求出矩阵 $A^{T}A$ 的正交相似标准型 $$Q^{T}A^{T}AQ=\Lambda=\mathrm{diag}\{\lambda_{1},\lambda_2,\cdots,\lambda_{r},0,\cdots,0\}$$这里 $Q=(\alpha_{1},\cdots,\alpha_{n})$ 为正交矩阵, 并且列向量组满足 $A^{T}A\alpha_{k}=\lambda_{k}\alpha_{k}$
	记 $\sigma_{k}=\sqrt{\lambda_{k}}$ , $\beta_{k}=\frac{1}{\sigma_{k}}A\alpha_{k}$ , $(k=1,...,r)$ ,
	当 $r<k\leq m$ 时, $\beta_{k}$ 由 $\beta_{1},...,\beta_{r}$ 任意的扩充得到一组标准正交基 $\beta_{1},...,\beta_{m}$
	再记 $P=(\beta_{1},\cdots,\beta_{m})$ , 就应有 $AQ=P\Sigma$ , 其中 $\Sigma=\mathrm{diag}\{\sigma_{1},\cdots,\sigma_{r},0,\cdots,0\}$ , 就有了 $$A=P\Sigma Q^{T}$$这里一般可排序 $\sigma_{1}\geq\sigma_{2}\geq\cdots\geq\sigma_{r}>0$ , 显然 $\Sigma$ 唯一, 但 $P,Q$ 都不唯一



