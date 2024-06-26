先前已经研究了域 $\mathbf F$ 上线性空间 $V$ 到 $V$ 上的映射，即线性变换
由于域 $\mathbf F$ 也是自身上的线性空间，即 $\mathbf F^{\mathbf F}$ , 故可以研究一个从 $V$ 到 $F$ 的线性映射，特别地，该映射输出值为纯量，故一般称之为函数

**定义**: 设 $V$ 为域 $\mathbf F$ 上的线性空间, $V$ 到 $F$ 的一个映射 $f$ 若满足$$\begin{align}f(\alpha+\beta)&=f(\alpha)+f(\beta),\qquad\forall\,\alpha,\beta\in V\\f(k\alpha)&=kf(\alpha),\qquad\qquad\forall\,\alpha\in V,k\in F\end{align}$$ 则称 $f$ 为 $V$ 上的一个**线性函数**

_例1：矩阵的迹：
	令 $$\begin{align}\mathrm{tr}:M_n(F)&\longrightarrow F\\A=(a_{ij})_{n\times n}&\longmapsto\sum_{i=1}^na_{ii}\end{align}$$ 由于 $\mathrm{tr}(A+B)=\mathrm{tr}(A)+\mathrm{tr}(B)$ , $\mathrm{tr}(kA)=k\mathrm{tr}(A)$ , $\forall\,A,B\in M_n(F)$ , $\forall\,k\in F$
	故 $\mathrm{tr}$ 为 $M_n(F)$ 上的一个线性函数，称之为**迹函数**_

_例2：
	令$$\begin{align}f:\qquad\qquad F^n&\longrightarrow F\\\alpha=(x_1,x_2,\cdots,x_n)^{'}&\longmapsto\sum_{i=1}^na_ix_i\end{align}$$同样，也可以证明 $f$ 为 $F^n$ 上的线性函数_

在例2中，$F^n$ 上的线性函数 $f$ 的表达式是明确的，即 $f(x_1,x_2,\cdots,x_s)=\sum_{i=1}^na_ix_i$ 

那么对于一般情况，如何求出域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 的线性函数 $f$ 的表达式呢
由于 $f$ 说到底是一个 $V$ 到 $F$ 上的线性映射，该映射被 $V$ 上的一个基 $\alpha_1,\alpha_2,...,\alpha_n$ 的作用结果所完全确定，故只需要确定 $f(\alpha_1),f(\alpha_2),...,f(\alpha_n)$ 即可
因为由此即知 $V$ 中任一向量 $\alpha=\sum_{i=1}^nx_i\alpha_i$ 在 $f$ 的像 $f(\alpha)$ 为：$f(\alpha)=\sum_{i=1}^nx_if(\alpha_i)$ ，这便为 $f$ 在基 $a_1,a_2,...,a_n$ 下的表达式，为 $\alpha$ 的在该基下的坐标 $x_1,x_2,...,x_n$ 的一次齐次函数；
另一方面，若已知 $\forall\,\alpha\in V$ ，都有 $f(\alpha)=\sum_{i=1}^nx_ia_i$ ，则 $f(\alpha_i)=a_i$ ，即已知基下 $f$ 的表达式可以；得到基在 $f$ 作用下的像

从上面可知，**$f$ 为 $V$ 上的线性函数当且仅当 $f$ 在 $V$ 的一个基下的表达式为 $\alpha$ 在该基下的坐标 $x_1,x_2,...,x_n$ 的一次线性函数**

将 $\mathrm{Hom}(V,F)$ 称为 $V$ 上的**线性函数空间**

由于有 $\dim\mathrm{Hom}(V,F)=(\dim\,V)(\dim\,F)=n\cdot1=n=\dim\,F^n$ 
故有$\mathrm{Hom}(V,F)\cong F^n$ 

**定义**: 设 $F$ 上的线性空间 $V$ 有一组基 $\alpha_1,\alpha_2,...,\alpha_n$ , 任取 $f\in\mathrm{Hom}(V,F)$ , 由于 $f$ 被 $f(\alpha_1),f(\alpha_2),...,f(\alpha_n)$ 完全确定, 故可以建立映射: $$\begin{align}\sigma:\qquad\mathrm{Hom}(V,F)&\longrightarrow F^n\\f&\longmapsto(f(\alpha_1),f(\alpha_2),\cdots,f(\alpha_n))\end{align}$$ 可以证明, $\sigma$ 为一个 $\mathrm{Hom}(V,F)$ 到 $F^n$ 到的同构映射, 那么 $\sigma^{-1}$ 也是 $F^n$ 到 $\mathrm{Hom}(V,F)$ 的同构映射, 如若在 $F^n$ 中取标准基 $\varepsilon_1,\varepsilon_2,...,\varepsilon_n$ , 记 $f_i=\sigma^{-1}(\varepsilon_i)$ , 则 $\sigma(f_i)=\varepsilon_i$ . 
在式$$\sigma(f)=f(\alpha_1)\varepsilon_1+f(\alpha_2)\varepsilon_2+\cdots+f(\alpha_n)\varepsilon_n$$ 中, 取 $f=f_i$ , 得到 $$\varepsilon_i=\sigma(f_i)=f_i(\alpha_1)\varepsilon_1+f_i(\alpha_2)\varepsilon_2+\cdots+f_i(\alpha_i)\varepsilon_i+\cdots+f_i(\alpha_n)\varepsilon_n$$ 故有$$f_i(\alpha_j)=\delta_{ij}=\begin{cases}1\qquad,i=j\\0\qquad,i\neq j\end{cases}$$ 将 $\mathrm{Hom}(V,F)$ 的该组基 $f_1,f_2,...,f_n$ 称为 $V$ 的基 $\alpha_1,\alpha_2,...,\alpha_n$ 的**对偶基**, 其满足 $f_i(\alpha_j)=\delta_{ij}$, 将 $\mathrm{Hom}(V,F)$ 称为 $V$ 的**对偶空间**, 记作 $V^*$ (注: 该种对偶空间的记法一般仅限于有限维线性空间) .

_$\forall\,\alpha=\sum_{i=1}^nx_i\alpha_i$ , $f_i(\alpha)=\sum_{j=1}^nx_jf_i(\alpha_j)=x_i$ 
故 $\alpha=\sum_{i=1}^nf_i(\alpha)\alpha_i$_

**定理**: 设 $V$ 为域 $\mathbf F$ 上的 $n$ 维线性空间, 在 $V$ 中取两个基 $\alpha_1,\alpha_2,...,\alpha_n$ 和 $\beta_1,\beta_2,...,\beta_n$ ,它们在 $V^*$ 中的对偶基分别为 $f_1,f_2,...,f_n$ 和 $g_1,g_2,...,g_n$ , 若 $\alpha_1,\alpha_2,...,\alpha_n$ 到 $\beta_1,\beta_2,...,\beta_n$ 的过渡矩阵为 $A$ 即有 $(\beta_1,\beta_2,\cdots,\beta_n)=(\alpha_1,\alpha_2,\cdots,\alpha_n)A$ , 则 $f_1,f_2,...,f_n$ 到 $g_1,g_2,...,g_n$ 的过渡矩阵为$$B=(A^{-1})^{'}$$ 
考虑映射: $$\begin{align}\sigma:\qquad\qquad V&\longrightarrow V^*\\\alpha=\sum_{i=1}^nx_i\alpha_i&\longmapsto\sum_{i=1}^nx_if_i\end{align}$$ 其为一个同构映射，将 $\sigma(\alpha)$ 记为 $f_{\alpha}$ ，对于 $\forall\,\beta=\sum_{i=1}^ny_i\alpha_i$ ，有 $f_i(\beta)=\sum_{j=1}^ny_jf_i(\alpha_j)=\sum_{j=1}^ny_j\delta_{ij}=y_i$ 
故$$f_{\alpha}(\beta)=(\sum_{i=1}^nx_if_i)(\beta)=\sum_{i=1}^nx_if_i(\beta)=\sum_{i=1}^nx_iy_i$$ 
_# 更多地，对于 $F$ 上的线性空间 $V$ ，其对偶空间 $V^*$ 也是 $F$ 上的线性空间，于是可以有 $V^*$ 的对偶空间 $(V^*)^*$ ，记为 $V^{**}$ ，称作 $V$ 的**双重对偶空间**，由于 $V\cong V^*$ ，$V^*\cong V^{**}$ ，进而有 $V\cong V^{**}$ 。_