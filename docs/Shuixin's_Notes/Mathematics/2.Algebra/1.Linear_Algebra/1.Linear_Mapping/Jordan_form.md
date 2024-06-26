 为了寻找线性变换的最简基表示，先前研究了可对角化的线性变换/方阵，然而这样的方法不具有普遍性，对于不一定可对角化的线性变换/方阵，Jordan标准型便为最简表示。
### 准对角阵（分块对角阵）

对于可对角化的线性变换 $\mathscr A:V\rightarrow V$ ,存在一组基 $\alpha_1,\alpha_2,...,\alpha_n$ 使得 $\mathscr A(\alpha_1,\alpha_2,...,\alpha_n)=(\alpha_1,\alpha_2,...,\alpha_n)A$ 其中 $A$ 为对角阵, 即 $$A=\begin{bmatrix}\lambda_1&0&\cdots&0\\0&\lambda_2&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&\lambda_n\end{bmatrix}$$
那么若线性变换 $\mathscr B:V\rightarrow V$ 不一定可对角化, 试着找到一组基 $\beta_1,\beta_2,...,\beta_n$ 使得 $$\mathscr B(\beta_1,\beta_2,...,\beta_n)=(\beta_1,\beta_2,...,\beta_n)B$$ 这里: $$B=\begin{bmatrix}B_1&0&\cdots&0\\0&B_2&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&B_n\end{bmatrix}$$ $B_k\:(k=1,2,...,n)$ 为方阵
### 不变子空间

**定义:** 线性空间 $V$ 有子空间 $W$ , $\mathscr A\in \mathrm{Hom}(V)$ 若对于 $\forall \alpha \in W, \mathscr A\alpha\in W$ , 则称 $W$ 为线性变换 $\mathscr A$ 的不变子空间, 称为 **$\mathscr A-$子空间** .

(平凡不变子空间: 零空间与 $V$ 易验证为不变子空间, 它们称作平凡不变子空间)
(非平凡不变子空间: 平凡不变子空间之外的不变子空间)
\[如: 核空间 $\mathrm{Ker}\mathscr A$ ,像空间 $\mathrm{Im}\mathscr A$ , 特征子空间 $V_{\lambda}$\]

**定理:** $\mathscr A$ 的非平凡不变子空间 $W$ 有一组基 $\alpha_1,\alpha_2,...,\alpha_r\:(r=\mathrm{dim}W)$ , 若将其扩充为 $V$ 的一组基 $\alpha_1,\alpha_2,...,\alpha_r,\alpha_{r+1},...,\alpha_n\:(n=\mathrm{dim}V)$ , 则 $\mathscr A$ 在该 $V$ 的基下的矩阵为准对角阵 $A$ $$A=\begin{bmatrix}A_1&A_3\\O&A_2\end{bmatrix}$$ 其中 $A_1$ 为 $\mathscr A|_W$ 在基 $\alpha_1,\alpha_2,...,\alpha_r$ 下的矩阵, $A_2$ 为 $\widetilde{\mathscr A}\,\triangleq\mathscr A|_{(V/W)}:V/W\rightarrow V/W$ 在 $V/W$ 的基 $\alpha_{r+1}+W,...,\alpha_n+W$ 下的矩阵

相反也有:

**定理**: $\mathscr A$ 在 $V$ 的一组基 $\alpha_1,\alpha_2,...,\alpha_r,\alpha_{r+1},...,\alpha_n$ 下的矩阵为准上三角阵 $A$ $$A=\begin{bmatrix}A_1&A_3\\O&A_2\end{bmatrix}$$ 这里 $A_1$ 为 $r$ 阶方阵, $A_2$ 为 $(n-r)$ 阶方阵, 则 $W=\langle\alpha_1,\alpha_2,...,\alpha_r\rangle$ 为 $\mathscr A$ 的一个非平凡不变子空间

在这样的启示下，可以推广至一般: 

**定理**: $\mathscr A$ 在 $V$ 的某个基下的方阵为准对角阵 $A$ 当且仅当 $V$ 有直和分解 $V=W_1\oplus W_2\oplus\cdots\oplus W_s$ , $W_k\:(k=1,2,...,s)$ 均为 $\mathscr A$ 的非平凡不变子空间, 且 $A_k$ 为 $\mathscr A|_{W_k}$ 在 $W_k$ 的一个基下的矩阵.
其中: $$A=\begin{bmatrix}A_1&O&\cdots&O\\O&A_2&\cdots&O\\\vdots&\vdots&\ddots&\vdots\\O&O&\cdots&A_s\end{bmatrix}$$ 
至此将矩阵准对角化的问题就转化为了线性空间 $V$ 分解为 $\mathscr A$ 的非平凡不变子空间直和的问题

### 最小多项式

思路是这样的，考虑[[多项式]] $f_k(x)\in \mathbf F[x]\:(k=1,2,...,s)$ 则 $f_k(\mathscr A)$ 也为 $V$ 上的线性变换，且易证 $\mathrm{Ker}f_k(\mathscr A)$ 为 $\mathscr A$ 的不变子空间，那么试找若干个多项式 $f_1(\mathscr A),f_2(\mathscr A),...,f_s(\mathscr A)$ 使得: $$V=\mathrm{Ker}f_1(\mathscr A)\oplus\mathrm{Ker}f_2(\mathscr A)\oplus\cdots\oplus\mathrm{Ker}f_s(\mathscr A)$$需要多项式满足一些条件: 

**定理**: 若 $f_1(x),f_2(x)\in \mathbf F[x], (f_1(x),f_2(x))=1, f(x)=f_1(x)f_2(x)$ , 则 $\mathrm{Ker}f(\mathscr A)=\mathrm{Ker}f_1(\mathscr A)\oplus\mathrm{Ker}f_2(\mathscr A)$ .

更一般的，有:

**定理**: 若两两互素的多项式 $f_1(x),f_2(x),...,f_s(x)\in F[x]$ , $f(x)=f_1(x)f_2(x)\cdots f_s(x)$ , 则 $\mathrm{Ker}f(\mathscr A)=\mathrm{Ker}f_1(\mathscr A)\oplus\mathrm{Ker}f_2(\mathscr A)\oplus\cdots\oplus\mathrm{Ker}f_s(\mathscr A)$ .

至少在形式上为使 $\mathrm{Ker}f(\mathscr A)=V$ ，就需要 $f(\mathscr A)=0$ .

由此引申出概念:

**定义**: 若非零多项式 $f(x)\in F[x]$ , 且 $f(\mathscr A)=0$ , 则称 $f(x)$ 为 $\mathscr{A}$ 的**零化多项式** .

而线性变换的零化多项式是很多的，旨在“最简”，就需要找到最简单的零化多项式: 

**定义**: $\mathscr A$ 的所有零化多项式中次数最小, 且最高次项系数为 $1$ 的多项式称为 $\mathscr A$ 的**最小多项式** .

为了找到这样一个最小多项式，需要先研究零化多项式，这似乎毫无头绪，但下面的定理指出任意线性变换存在一个特殊的零化多项式: 

**Hamilton-Cayley定理**: 线性变换 $\mathscr A$ 的特征多项式 $\varphi (\lambda)$ 为 $\mathscr A$ 的一个零化多项式 .

$\varphi(\lambda)$ 虽为 $\mathscr A$ 的零化多项式，但不一定为 $\mathscr A$ 的最小多项式，但究其特殊性，却存在着与最小多项式间的关联，事实上最小多项式也与所有零化多项式有着关联: 

**定理**: $\mathscr A$ 的最小多项式 $d(\lambda)$ 整除 $\mathscr A$ 的任意零化多项式 . 

特别地，$d(\lambda)|\varphi(\lambda)$ , 这说明 $d(\lambda)$ 的根均为 $\varphi(\lambda)$ 的根, 也就是说最小多项式 $d(\lambda)$ 的根, 无非在 $\mathscr A$ 的全部特征值 $\lambda_1,\lambda_2,...,\lambda_s$ 中, 那么是否有 $d(\lambda)$ 的根就确实为 $\lambda_1,\lambda_2,...,\lambda_s$ 呢？

**定理**: $\mathscr A$ 的最小多项式 $d(\lambda)$ 与特征多项式 $\varphi(\lambda)$ 有相同的根 .

至此已大致可以确定最小多项式的模样:
特征多项式 $\varphi(\lambda)=(\lambda-\lambda_1)^{l_1}(\lambda-\lambda_2)^{l_2}\cdots(\lambda-\lambda_s)^{l_s}$  , 则最小多项式形如 $d(\lambda)=(\lambda-\lambda_1)^{m_1}(\lambda-\lambda_2)^{m_2}\cdots(\lambda-\lambda_s)^{m_s}\:(1\leq m_k\leq l_k)$. 

至此，基本概念已提出完毕，对于接下来的部分，有着不一样的路径。

### 路径一：空间分解

无论如何已经有了 $V$ 的一种直和分解式 $V=\mathrm{Ker}f_1(\mathscr A)\oplus\mathrm{Ker}f_2(\mathscr A)\oplus\cdots\oplus\mathrm{Ker}f_s(\mathscr A)$ 这个分解式可以是由 $\mathscr A$ 的零化多项式得到的，由先前的结论知道，$\mathscr A$ 的零化多项式无非形如 $f(\lambda)=(\lambda-\lambda_1)^{\alpha_1}(\lambda-\lambda_2)^{\alpha_2}\cdots(\lambda-\lambda_s)^{\alpha_s}\:(m_k\leq\alpha_k)$ ，这里 $m_k$ 为最小多项式中对应因式的次数。
那么这些因式当然是两两互素的，于是可以这样分解：$$V=\mathrm{Ker}(\mathscr A-\lambda_1\mathscr I)^{\alpha_1}\oplus\mathrm{Ker}(\mathscr A-\lambda_2\mathscr I)^{\alpha_2}\oplus\cdots\oplus\mathrm{Ker}(\mathscr A-\lambda_s\mathscr I)^{\alpha_s}$$易知这是一个非平凡不变子空间分解，
接下来为了研究整体，先研究部分。

#### 幂零变换与Jordan块

考虑这样一个变换: $\mathscr A=k\mathscr I+\mathscr B$ ，这里 $\mathscr I$ 为恒等变换，$\mathscr B$ 为幂零指数为 $l$ 的幂零变换。
那么 $(\mathscr A-k\mathscr I)^l=\mathscr B^l=0$ ，故可知 $\mathscr A$ 有零化多项式同时也也易证是最小多项式的 $d(\lambda)=(\lambda-k)^l$ 。
继续研究这个变换，可以得到如下结论：

**定理**: 域 $\mathbf F$ 上的 $l$ 维线性空间 $W$ 上的线性变换 $\mathscr A=k\mathscr I+\mathscr B$ , $\mathscr B$ 为幂零指数为 $l$ 的幂零变换, 则 $W$ 中存在一个基 $\alpha_1,\alpha_2,...,\alpha_l$ 使得 $\mathscr A$ 在该基下的矩阵 $A$ 为
$$A=\begin{bmatrix}k&1&0&\cdots&0&0&0\\0&k&1&\cdots&0&0&0\\0&0&k&\cdots&0&0&0\\\vdots&\vdots&\vdots&\ddots&\vdots&\vdots&\vdots\\0&0&0&\cdots&k&1&0\\0&0&0&\cdots&0&k&1\\0&0&0&\cdots&0&0&k\end{bmatrix}$$
这里称 $A$ 为一个 $l$ 级 Jordan 块, 记作 $J_l(k)$ , $k$ 为主对角线上的元素, $J_l(k)$ 的最小多项式为 $(\lambda-k)^l$ .

为何要研究这个变换呢，这是因为先前已经有了 $V$ 的非平凡不变子空间直和分解：$$V=\mathrm{Ker}(\mathscr A-\lambda_1\mathscr I)^{\alpha_1}\oplus\mathrm{Ker}(\mathscr A-\lambda_2\mathscr I)^{\alpha_2}\oplus\cdots\oplus\mathrm{Ker}(\mathscr A-\lambda_s\mathscr I)^{\alpha_s}$$
若特别地当 $\alpha_k=m_k$ 时，则 $(\mathscr A-\lambda_k\mathscr I)$ 为 $\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^{m_k}$ 上幂零指数为 $m_k$ 的幂零变换（这里也暗道出为什么要用最小多项式而不是特征多项式或其他零化多项式，因为要保证次数为幂零指数）。

#### 根子空间与根向量

先对 $\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^{\alpha_k}$ 进一步的研究，我们知道，当 $\alpha_k=1$ 时，$$\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)=V_{\lambda_k}\qquad(特征子空间)$$ 若记 $W_{\lambda_k}^{(m)}=\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^m$ ，则不难得到一个无穷空间序列：$$V_{\lambda_k}=W_{\lambda_k}^{(1)}\subseteq W_{\lambda_k}^{(2)}\subseteq \cdots\subseteq W_{\lambda_k}^{(m)}\subseteq\cdots\subseteq V$$
由[[抽屉原理]]可知存在正整数 $N$ 使得 $W_{\lambda_k}^{(1)}\subseteq W_{\lambda_k}^{(2)}\subseteq \cdots\subseteq W_{\lambda_k}^{(N-1)}\subseteq W_{\lambda_k}^{(N)}=W_{\lambda_k}^{(N+1)}=\cdots$ 。
因此就有 $$W_{\lambda_k}^{(N)}=\bigcup_{m=1}^{\infty}W_{\lambda_k}^{(m)}\triangleq W_{\lambda_k}$$
**定义**: $W_{\lambda_k}=\bigcup_{m=1}^{\infty}\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^{(m)}$ 称作 $\mathscr A$ 的属于特征值 $\lambda_k$ 的**根子空间**, 根子空间 $W_k$ 中的非零向量称作属于特征值 $\lambda_k$ 的**根向量** .

可以证明，根子空间可以由特征多项式得到：

**定理**: 若 $\mathscr A$ 的特征多项式 $\varphi(\lambda)=(\lambda-\lambda_1)^{l_1}(\lambda-\lambda_2)^{l_2}\cdots(\lambda-\lambda_s)^{l_s}$ 为 $\mathbf F[\lambda]$ 上的标准分解式, 则属于特征值 $\lambda_k$ 的根子空间为 $\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^{l_k}$ .

$V$ 的全部不同的根子空间构成了 $V$ ：

**空间第一分解定理**: 设 $\lambda_1,\lambda_2,...,\lambda_s$ 为线性变换 $\mathscr A:V\rightarrow V$ 的全部不同特征值, 它们的代数重数分别为 $l_1,l_2,...,l_s\:(l_1,l_2,...,l_s\geq1,l_1+l_2+\cdots+l_s=n=\mathrm{dim}V)$ , 即 $\mathscr A$ 的特征多项式 $\varphi(\lambda)=(\lambda-\lambda_1)^{l_1}(\lambda-\lambda_2)^{l_2}\cdots(\lambda-\lambda_s)^{l_s}$ , 则: $$V=W_{\lambda_1}\oplus W_{\lambda_2}\oplus\cdots\oplus W_{\lambda_s}$$这里 $W_{\lambda_k}$ 为特征值 $\lambda_k$ 的根子空间 . 并且 $\mathscr A|_{W_{\lambda_k}}$ 在 $W_{\lambda_k}$ 上的特征多项式为 $\varphi_k(\lambda)=(\lambda-\lambda_k)^{l_k}$ .

至此，在线性变换 $\mathscr A$ 下，$V$ 的结构已较清晰。

**定理**: 若 $\mathscr A$ 为域 $\mathbf F$ 上线性空间 $V$ 上的线性变换, 若 $V$ 可分解为一些非平凡不变子空间的直和: $$V=W_1\oplus W_2\oplus\cdots\oplus W_s$$
且 $\mathscr A|_{W_k}$ 在 $W_k$ 上的最小多项式为 $d_k(\lambda)\:(k=1,...,s)$ , 则 $\mathscr A$ 的最小多项式为: $$d(\lambda)=[d_1(\lambda),d_2(\lambda),...,d_s(\lambda)]\qquad(最小公倍式)$$

_**整理一下：
线性变换 $\mathscr A$
$\Rightarrow$ 特征多项式  $\varphi(\lambda)$
$\Rightarrow$ 特征多项式标准分解 $(\lambda-\lambda_1)^{l_1}(\lambda-\lambda_2)^{l_2}\cdots(\lambda-\lambda_s)^{l_2}$
$\Rightarrow$ 根子空间分解 $V=W_{\lambda_1}\oplus W_{\lambda_2}\oplus\cdots\oplus W_{\lambda_s}=\mathrm{Ker}(\mathscr A-\lambda_1\mathscr I)^{l_1}\oplus\mathrm{Ker}(\mathscr A-\lambda_2\mathscr I)^{l_2}\oplus\cdots\oplus\mathrm{Ker}(\mathscr A-\lambda_s\mathscr I)^{l_s}$
$\Rightarrow$ 考虑 $W_{\lambda_k}$ 中的幂零变换 $(\mathscr A|_{W_{\lambda_k}}-\lambda_k\mathscr I)$ 的最小多项式 $d_k(\lambda)$
$\Rightarrow$ $\mathscr A$ 的最小多项式为 $d(\lambda)=[d_1(\lambda),d_2(\lambda),...,d_s(\lambda)]$**_

由于 $W_{\lambda_k}$ 的定义，可以知道 $(\mathscr A|_{W_{\lambda_k}}-\lambda_k\mathscr I)$ 的幂零指数 $r_k\leq l_k$ ，
当 $r_k=l_k$ 时，当然就有： $W_k$ 中存在基 $\alpha_{k1},...,\alpha_{kt_k}$ 使得 $\mathscr A|_{W_{\lambda_k}}$ 在该组基下的矩阵为 $J_{l_k}(\lambda_k)$ 。
故由此可知 $\mathscr A$ 在基 $\alpha_{11},...,\alpha_{1t_1},\alpha_{21},...,\alpha_{2t_2},...,\alpha_{s1},...,\alpha_{st_s}$ 下的矩阵为Jordan形矩阵 $A=\mathrm{diag}\{J_{l_1}(\lambda_1),J_{l_2}(\lambda_2),...,J_{l_s}(\lambda_s)\}$ 。

如果 $r_k < l_k$ 呢，需要进一步讨论
下面先着重研究幂零变换的最简基表示（哪怕幂零指数小于空间维数）

#### 幂零变换的Jordan标准形

设 $\mathscr B$ 为 $r$ 维线性空间 $W$ 上幂零指数为 $l\:(l\leq r)$ 的幂零变换，任取非零的 $\eta\in W$ 都有一个最小的正整数 $t=t(\eta)$ 使得 $\mathscr B^t\eta=0$ 但 $\mathscr B^{t-1}\eta\neq0\:(t\leq r)$ ，容易可以证明 $\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta$ 为线性无关组。
那么可以有如下定义：

**定义**: 设 $\mathscr B$ 为 $r$ 维线性空间 $W$ 上幂零指数为 $l\:(l\leq r)$ 的幂零变换，非零向量 $\eta\in W$ 存在最小的正整数 $t=t(\eta)$ 使得 $\mathscr B^t\eta=0$ 但 $\mathscr B^{t-1}\eta\neq0\:(t\leq r)$ ，将 $\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle$ 称作由 $\eta$ 生成的 **$\mathscr B-$强循环子空间** .

显然有 $\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle\subseteq W$ ，那么有  $W=\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle\oplus(W-\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle)$
直观而言，在同一个线性变换 $\mathscr B$ 下，$W$ 与 $(W-\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle)$ 的结构是一样的，那么后者或许也能类似做同样的分解：$$(W-\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle)=\langle\mathscr B^{t^{'}-1}\gamma,...,\mathscr B\gamma,\gamma\rangle\oplus(W-\langle\mathscr B^{t-1}\eta,...,\mathscr B\eta,\eta\rangle-\langle\mathscr B^{t^{'}-1}\gamma,...,\mathscr B\gamma,\gamma\rangle)$$
依次下去，或许 $W$ 可以分解为若干个 $\mathscr B-$强循环子空间的直和，事实上有定理：

**定理**: 设 $\mathscr B$ 为 $r$ 维线性空间 $W$ 上幂零指数为 $l\:(l\leq r)$ 的幂零变换, 则 $W$ 可分解为 $\mathrm{dim}W_0$ 个 $\mathscr B-$强循环子空间的直和, 这里 $W_0$ 为幂零变换 $\mathscr B$ 属于特征值 $0$ 的特征子空间 (幂零变换的特征值只有 $0$ ) .

这样，幂零变换的结构就完全清晰，这是因为：

若 $W=W_1\oplus W_2\oplus\cdots\oplus W_{d}\:(d=\mathrm{dim}W_0)$ ，其中 $W_{k}=\langle\mathscr B^{t_k-1}\eta_k,...,\mathscr B\eta_k,\eta_k\rangle$ ，且不难知道 $\mathscr B|_{W_k}$ 在 $W_k$ 的该组基下的矩阵为 $J_{t_k}(0)$ ，而由先前的结论就知道，将每个子空间的基合起来：$$\mathscr B^{t_1-1}\eta_1,...,\mathscr B\eta_1,\eta_1,\mathscr B^{t_2-1}\eta_2,...,\mathscr B\eta_2,\eta_2,...,\mathscr B^{t_d-1}\eta_{d},...,\mathscr B\eta_{d},\eta_{d}$$ 则其为 $W$ 的一组基，且 $\mathscr A$ 在该基下的矩阵为Jordan形矩阵 $\mathrm{diag}\{J_{t_1}(0),J_{t_2}(0),...,J_{t_d}(0)\}$ 。

**定理(幂零变换的Jordan标准形): 设 $\mathscr B$ 为 $r$ 维线性空间 $W$ 上幂零指数为 $l\:(l\leq r)$ 的幂零变换, 则 $W$ 中存在一个基, 使得 $\mathscr B$ 在该基下的矩阵 $\mathbf B$ 为一个Jordan形矩阵, 其中每个Jordan块的级数都不超过 $l$ 且主对角元都是 $0$ , Jordan块的总数为 $\mathrm{dim}W_0=\mathrm{dim}(\mathrm{Ker}\,\mathscr B)=r-\mathrm{rank}(\mathscr B)$ , $t$ 级Jordan块的个数为 $N(t)=\mathrm{rank}(\mathscr B^{t+1})+\mathrm{rank}(\mathscr B^{t-1})-2\mathrm{rank}(\mathscr B^t)$ , 将 $\mathbf B$ 称为 $\mathscr B$ 的 $\mathbf{Jordan}\bf{标准形}$ , 除去Jordan块的次序外, $\mathscr B$ 的Jordan标准形唯一 .**

这里 $N(t)$ 的计算方法源于 $$\mathrm{rank}\,\mathbf{J}_t(0)^m=\begin{cases}t-m,\qquad m<t\\0,\qquad \qquad m\geq t\end{cases}$$ 然后以此构造等量关系得到的，此处不赘述，定理的证明中会详细说明。

#### 线性变换的Jordan标准形

研究完幂零变换，一般的变换就可顺势得出，这是因为 $V=\mathrm{Ker}(\mathscr A-\lambda_1\mathscr I)^{l_1}\oplus\mathrm{Ker}(\mathscr A-\lambda_2\mathscr I)^{l_2}\oplus\cdots\oplus\mathrm{Ker}(\mathscr A-\lambda_s\mathscr I)^{l_s}$ , 这里 $(\mathscr A|_{W_k}-\lambda_k\mathscr I)$ 为 $\mathrm{Ker}(\mathscr A-\lambda_k\mathscr I)^{l_k}$ 上幂零指数不超过 $l_k$ 的幂零变换。若记 $W_k$ 上的线性变换 $\mathscr B_k=\mathscr A|_{W_k}-\lambda_k\mathscr I$ ，则 $W_k$ 中存在一组基使得 $\mathscr B_k$ 在该基下的矩阵 $B_k$ 为主对角元全为零的Jordan形矩阵，记 $\mathscr A|_{W_k}$ 在该基下的矩阵为 $A_k$ ，$\mathscr I$ 在该基下的矩阵自然为 $I$ ，则 $A_k=\lambda_k I+B_k$ ，显然 $A_k$ 为主对角元全为 $\lambda_k$ ，各级Jordan块数以及Jordan块总数和 $B_k$ 完全相同的Jordan形矩阵。
也即：

**定理(线性变换的Jordan标准形): 设 $\mathscr A$ 为域 $\mathbf F$ 上的 $n$ 维线性空间 $V$ 上的线性变换, 若 $\mathscr A$ 的最小多项式 $d(\lambda)$ 在 $\mathbf F[\lambda]$ 上的标准分解式为 $$d(\lambda)=(\lambda-\lambda_1)^{l_1}(\lambda-\lambda_2)^{l_2}\cdots(\lambda-\lambda_s)^{l_s}$$
则 $V$ 中存在一个基, 使得 $\mathscr A$ 在此基下的矩阵 $A$ 为Jordan形矩阵, 及全部对角元为 $\mathscr A$ 的全部特征值, 特征值 $\lambda_k$ 在主对角线上出现的次数为 $\lambda_k$ 的代数重数, 主对角元为 $\lambda_k$ 的Jordan块的总数 $N_k$ 为 $$N_k=n-\mathrm{rank}(\mathscr A-\lambda_k\mathscr I)$$
其中 $t$ 级Jordan块 $J_t(\lambda_k)$ 的个数 $N_k(t)$ 为 $$N_k(t)=\mathrm{rank}(\mathscr A-\lambda_k\mathscr I)^{t+1}+\mathrm{rank}(\mathscr A-\lambda_k\mathscr I)^{t-1}-2\mathrm{rank}(\mathscr A-\lambda_k\mathscr I)^{t}\quad(1\leq t\leq l_k)(k=1,2,...,s)$$
这个Jordan形矩阵 $A$ 称为 $\mathscr A$ 的 $\mathrm{Jordan}\rm{标准形}$ , 除去Jordan块的次序外, $\mathscr A$ 的Jordan标准形唯一 .**

### 路径二：$\lambda-$矩阵

为了找寻矩阵的相似标准形（即Jordan形），就要找到相似关系下的全系不变量，前人经过探索发现了 $A,B$ 间的相似关系与 $\lambda I-A,\lambda I-B$ 间的相抵关系有着密切的关系。

#### 多项式矩阵

**定义**: 形如 $$A(\lambda)=\begin{bmatrix}a_{11}(\lambda)&a_{12}(\lambda)&\cdots&a_{1n}(\lambda)\\a_{21}(\lambda)&a_{22}(\lambda)&\cdots&a_{2n}(\lambda)\\\vdots&\vdots&\ddots&\vdots\\a_{m1}(\lambda)&a_{m2}(\lambda)&\cdots&a_{mn}(\lambda)\end{bmatrix}$$

的矩阵称作 **多项式矩阵 或 $\lambda-$矩阵** , 这里 $a_{ij}(\lambda)$ 都是域 $\mathbf F$ 上关于未定元 $\lambda$ 的多项式 .

不难验证关于多项式矩阵的 **加法、矩阵乘法、数乘** 与常量矩阵并无不同
下面定义 $\lambda-$矩阵 的初等变换和初等矩阵。

**定义**: 对 $\lambda-$ 矩阵 经行如下三种变换称作 $\lambda-$矩阵 的**初等行(列)变换**: $$\begin{align}&1^{\circ}将矩阵的第i行(列)乘以f(\lambda)后加到第j行(列)\\&2^{\circ}将矩阵的第i行(列)和第j行(列)交换\\&3^{\circ}将矩阵的第i行(列)乘以非零常数 c\qquad(注意这里必须是常数不能是多项式)\end{align}$$
**定义**: 将单位矩阵分别经过单次初等变换得到的矩阵称为**初等矩阵**: $$\begin{align}&1^{\circ}P(j,i(f(\lambda)))是单位阵将第i行(第j列)乘以f(\lambda)后加到第j行(第i列)后得到的矩阵\\&2^{\circ}P(i,j)是将矩阵的第i行(列)和第j行(列)交换得到的矩阵\\&3^{\circ}P(i(c))是将矩阵的第i行(列)乘以非零常数c后得到的矩阵\end{align}$$
类似地，左（右）乘初等矩阵等价于做相应初等行（列）变换。

**定义**: 若 $A(\lambda),B(\lambda)$ 均为 $n$ 阶 $\lambda-$矩阵 且有: $$A(\lambda)B(\lambda)=B(\lambda)A(\lambda)=I_n$$
则称 $B(\lambda)$ 为 $A(\lambda)$ 的**逆 $\lambda-$矩阵** , 此时称 $A(\lambda)$ 为**可逆 $\lambda-$矩阵**, 不引起混淆时也称为**可逆阵** .

（注：常量矩阵的一些结论不能直接应用，如对于 $\lambda-$矩阵 而言：$|A(\lambda)|\neq0\nLeftrightarrow A(\lambda)可逆$ .）

不难知道，一个 $M_{m\times n}(\mathbf F[\lambda])$ 中的矩阵，可以与 $M_{m\times n}(\mathbf F)[\lambda]$ 中的多项式等同起来，即：$$M(\lambda)=M_t\lambda^t+M_{t-1}\lambda^{t-1}+\cdots+M_0\qquad(M_k\in M_{m\times n}[\mathbf F],k=0,1,...,t)$$
同样的对矩阵多项式可以做带余除法

**引理**: 设 $M(\lambda),N(\lambda)$ 为两个 $n$ 阶 $\lambda-$矩阵 且都不等于零 , 又设 $B$ 为 $n$ 阶常量矩阵, 则必然存在 $\lambda-$矩阵 $Q(\lambda),S(\lambda)$ 及常量矩阵 $R,T$ , 使得: $$\begin{align}&M(\lambda)=(\lambda I-B)Q(\lambda)+R\\&N(\lambda)=S(\lambda)(\lambda I-B)+T\end{align}$$

有了这个结论后便可以证明：

**定理**: 设 $A,B\in M_{m\times n}(\mathbf F)$ , 则 **$A$ 与 $B$ 相似** 的充要条件为 **$\lambda-$矩阵 $\lambda I-A$ 与 $\lambda I-B$ 相抵**

那么常量矩阵的相似现在归结为了 $\lambda-$矩阵 的相抵，于是试求 $\lambda-$矩阵 的相抵标准形。

**定理**: 若 $A(\lambda)=(a_{ij}(\lambda))_{m\times n}$ 为一非零 $\lambda-$矩阵, 则 $A(\lambda)$ 必相抵于如此的一个 $\lambda-$矩阵 $B(\lambda)$ , 这里这个 $B(\lambda)$ 满足 $b_{11}(\lambda)\neq0$ 且 $b_{11}(\lambda)$ 可整除 $B(\lambda)$ 中的任一元素 .

对上述结论进行归纳推广可得到：

**定理**: 设 $A(\lambda)$ 为一个 $n$ 阶 $\lambda-$矩阵 , 则 $A(\lambda)$ 相抵于对角阵 $\mathrm{diag}\{d_1(\lambda),d_2(\lambda),\cdots,d_r(\lambda),0,\cdots,0\}\qquad(r\leq n)$ , 这里 $d_k(\lambda)$ 为非零首一多项式且有 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,2,...,r-1)$ .

上述结论即 $$P(\lambda)A(\lambda)Q(\lambda)=
\begin{bmatrix}d_1(\lambda) & \ & \ & \ & \ & \ & \\
& d_2(\lambda) & \ & \ & \ & \ & \\
& \ & \ \ddots & \ & \ & \ & \\
& \ & \ & \ d_r(\lambda) & \ & \ & \\
& \ & \ & \ & 0 & \ & \\& \ & \ & \ & \ & \ \ddots &  \\
& \ & \ & \ & \ & \ & \ 0\end{bmatrix}$$

**定义**: 上面的对角矩阵称为 $\lambda-$矩阵 $A(\lambda)$ 的**法式**或**相抵标准形** .

**推论**: 任意 $n$ 阶可逆 $\lambda-$矩阵都可表示为有限个初等 $\lambda-$矩阵 之积 .

由于 可逆对角 $\lambda-$矩阵 $\implies$ 主对角元均为非零常数（不难证明）
因此 $A(\lambda)$ 可逆且 $P(\lambda),Q(\lambda)$ 为若干初等阵乘积 $\implies$ 左式可逆 $\implies$ 右式可逆 $\implies$ $r=n$ 且 $d_1(\lambda)=d_2(\lambda)=\cdots=d_n(\lambda)=1$ （因为 $d_k(\lambda)$ 均为首一多项式，且应为常数）

故 $P(\lambda)A(\lambda)Q(\lambda)=I_n$ ，进而有 $A(\lambda)=P(\lambda)^{-1}Q(\lambda)^{-1}$ 

**推论**: $A\in M_n[\mathbf F]$ ，则 $A$ 的特征矩阵 $\lambda I_n-A$ 必相抵于 $$\mathrm{diag}\{1,\cdots,1,d_1(\lambda),\cdots,d_m(\lambda)\}$$ 这里 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,2,...,m-1)$

#### 不变因子

上一部分指明了多项式矩阵的法式相同必然相抵，但相抵是否能推出法式相同仍然有待讨论
如若确实，则找到了一个 $\lambda-$矩阵 相抵的全系（完全）不变量：
即多项式序列 $$d_1(\lambda),d_2(\lambda),...,d_r(\lambda)$$
这里 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,...,r-1)$ 
于是，我们试证实上式在相抵关系下具有不变性。

**定义**: 设 $A(\lambda)$ 为 $n$ 阶 $\lambda-$矩阵 , $k$ 为小于等于 $n$ 的正整数 . 若 $A(\lambda)$ 有一个不为零的 $k$ 阶子式, 则定义 $A(\lambda)$ 的 $k$ 阶行列式因子 $D_k(\lambda)$ 为 $A(\lambda)$ 的所有 $k$ 阶子式的首一最大公因式 . 若 $A(\lambda)$ 的所有 $k$ 阶子式都为零 ,则定义 $A(\lambda)$ 的 $k$ 阶行列式 $D_k(\lambda)$ 为零 .

那么对于对角阵 $A(\lambda)=\mathrm{diag}\{d_1(\lambda),d_2(\lambda),\cdots,d_r(\lambda),0,\cdots,0\}\qquad(r\leq n)$ , 这里 $d_k(\lambda)$ 为非零首一多项式且有 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,2,...,r-1)$ .
$A(\lambda)$ 各阶行列式因子便为 $D_1(\lambda)=d_1(\lambda)\,,\,D_2(\lambda)=d_1(\lambda)d_2(\lambda)\,,...,\,D_r(\lambda)=d_1(\lambda)d_2(\lambda)\cdots d_r(\lambda)$ 。

另一方面，也有：

**引理**: 若 $D_1(\lambda),D_2(\lambda),...,D_r(\lambda)$ 为 $A(\lambda)$ 的非零行列式因子, 则 $D_k(\lambda)|D_{k+1}(\lambda)\:(k=1,2,...r-1)$ .

这是因为 $D_{k+1}(\lambda)$ 可以展开为 $k+1$ 个 $D_{k+1}(\lambda)$ 的 $k$ 阶子式 （同时也是 $A(\lambda)$ 的 $k$ 阶子式）的线性组合，而任何 $A(\lambda)$ 的 $k$ 阶子式又必然被 $D_k(\lambda)$ 整除（因为定义如此）。

由此，可以合理的定义：

**定义**: 若 $D_1(\lambda),D_2(\lambda),...,D_r(\lambda)$ 为 $\lambda-$矩阵 $A(\lambda)$ 的非零行列式因子, 则可定义 $g_1(\lambda)=D_(\lambda),g_2(\lambda)=D_2(\lambda)/D_1(\lambda),...,g_r(\lambda)=D_r(\lambda)/D_{r-1}(\lambda)$ , 它们称为 $A(\lambda)$ 的不变因子 .

**定理**: 相抵的矩阵有相同的行列式因子, 进而有相同的不变因子 .

该定理只需分别证明在三种初等变换下，行列式因子不改变即可，笔记的证明部分会详细说明

**推论**: 若 $n$ 阶 $\lambda-$矩阵 $A(\lambda)$ 的法式为 $$\Lambda=\mathrm{diag}\{d_1(\lambda),d_2(\lambda),...,d_r(\lambda),0,...,0\}$$这里 $d_k(\lambda)$ 为非零首一多项式且 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,2,...,r-1)$ , 则 $A(\lambda)$ 的不变因子为 $d_1(\lambda),d_2(\lambda),...,d_r(\lambda)$ , 事实上有法式和不变因子相互唯一确定 .

**推论**: 若 $A(\lambda),B(\lambda)$ 为 $n$ 阶 $\lambda-$矩阵 , 则 $A(\lambda)$ 与 $B(\lambda)$ 相抵当且仅当它们的法式相同 .

**推论**: $n$ 阶 $\lambda-$矩阵 $A(\lambda)$ 的法式与初等变换的选取无关

**定理**: 若 $A,B\in M_n[\mathbf F]$ , 则 **$A$ 与 $B$ 相似** 当且仅当 **它们的特征多项式 $\lambda I-A$ 与 $\lambda I-B$ 具有相同的行列式因子或不变因子** .

之后特征矩阵 $\lambda I-A$ 的行列式因子和不变因子简称为 $A$ 的行列式因子和不变因子

**推论**: 设域 $\mathbf F\subseteq\mathbf K$ , $A,B$ 为 $\mathbf F$ 上的两个矩阵, 则 $A$ 和 $B$ 在 $\mathbf F$ 上相似 当且仅当 $A$ 和 $B$ 在 $K$ 上相似 .

这说明域扩张不改变矩阵的相似关系。

#### 有理标准形

旨在构造一个更简单的矩阵，使得它与给定的矩阵有相同的不变因子
前面已经知道 $A$ 的特征矩阵 $\lambda I_n-A$ 必相抵于 $$\mathrm{diag}\{1,\cdots,1,d_1(\lambda),\cdots,d_m(\lambda)\}$$ 这里 $d_k(\lambda)|d_{k+1}(\lambda)\:(k=1,2,...,m-1)$ ，故 $\lambda I_n-A$ 的不变因子为：$$1,...,1,d_1(\lambda),...,d_k(\lambda)$$

**引理**: 设 $r$ 阶矩阵 $$F=\begin{bmatrix}0&1&0&\cdots&0\\0&0&1&\cdots&0\\\vdots&\vdots&\vdots&\ddots&\vdots\\0&0&0&\cdots&1\\-a_r&-a_{r-1}&-a_{r-2}&\cdots&-a_1\end{bmatrix}$$
则: 
$(1)$ $\mathbf F$ 的行列式因子和不变因子都为 $$1,...,1,f(\lambda)$$
这里前面有 $r-1$ 个 $1$ , $f(\lambda)=\lambda^r+a_1\lambda^{r-1}+\cdots+a_r$ .
$(2)$ $\mathbf F$ 的最小多项式为 $f(\lambda)$ .

**引理**: 若 $\lambda-$矩阵 $A(\lambda)$ 与对角 $\lambda-$矩阵 $\mathrm{diag}\{d_1(\lambda),d_2(\lambda),...,d_n(\lambda)\}$ ,  $\lambda-$矩阵 $B(\lambda)$ 与对角 $\lambda-$矩阵 $\mathrm{diag}\{d_1^{'}(\lambda),d_2^{'}(\lambda),...,d_n^{'}(\lambda)\}$ , 这里 $d_1^{'}(\lambda),d_2^{'}(\lambda),...,d_n^{'}(\lambda)$ 为 $d_1(\lambda),d_2(\lambda),...,d_n(\lambda)$ 的一个置换, 则 $A(\lambda)$ 相抵于 $B(\lambda)$ .

**定理**: 设 $A$ 为 $\mathbf F$ 上的 $n$ 阶方阵, $A$ 的不变因子组为 $$1,...,1,d_1(\lambda),...,d_k(\lambda)$$
这里 $\mathrm{deg}\,d_k(\lambda)=m_k\geq 1$ , 则 $A$ 相似于下面的分块对角矩阵: $$F=\begin{bmatrix}F_1& & & \\& F_2& &\\& & \ddots&\\& & & F_k\end{bmatrix}$$
这里 $F_k$ 为 $m_k$ 阶方阵, 且 $F_k$ 是形如 $$\begin{bmatrix}0&1&0&\cdots&0\\0&0&1&\cdots&0\\\vdots&\vdots&\vdots&\ddots&\vdots\\0&0&0&\cdots&1\\-a_r&-a_{r-1}&-a_{r-2}&\cdots&-a_1\end{bmatrix}$$
的矩阵, $F_j$ 的最后一行为 $d_j(\lambda)$ 的除首项系数外的负系数 .

**定义**: 上面定理中的分块对角矩阵称为矩阵 $A$ 的**有理标准形**或**Frobenius标准形**, 每个 $F_j$ 称为**Frobenius块** .

**算例**: 矩阵 $A$ 的不变因子为 $1,1,1,\lambda-1,(\lambda-1)^2,(\lambda-1)^2(\lambda+1)$ ; 则这里 $F_1(\lambda)=\lambda-1,F_2(\lambda)=(\lambda-1)^2=\lambda^2-2\lambda+1,F_3(\lambda)=\lambda^3-\lambda^2-\lambda+1$ , 那么 $A$ 的有理标准形为 $$F=\begin{bmatrix}1&&&&&\\&0&1&&&\\&-1&2&&&\\&&&0&1&0\\&&&0&0&1\\&&&-1&1&1\end{bmatrix}$$

**定理**: $\mathbf F$ 上的矩阵 $A$ 的不变因子为 $$1,...,1,d_1(\lambda),...,d_k(\lambda)$$
这里 $d_j(\lambda)|d_{j+1}(\lambda)\:(j=1,...,k-1)$ , 则 $A$ 的最小多项式 $m(\lambda)=d_k(\lambda)$ . 

#### 初等因子

已经把矩阵 $A$ 的形式按照不变因子简化为了各块，但这样的结果比较粗糙，如果把不变因子进一步分解，可以得到更加精细的结果。

**定义**: 若 $\mathbf F$ 上的矩阵 $A$ 有非常数不变因子 $d_1(\lambda),d_2(\lambda),...,d_k(\lambda)$ , 在 $\mathbf F$ 上将它们分解为不可约因式之积: $d_j(\lambda)=p_1(\lambda)^{e_{j1}}p_2(\lambda)^{e_{j2}}\cdots p_t(\lambda)^{e_{jt}}\:(j=1,2,...,k)$ , 这里 $e_{ij}\geq0$ , 而 $d_j(\lambda)|d_{j+1}(\lambda)$ , 因此 $$e_{1j}\leq e_{2j}\leq\cdots\leq e_{kj}\qquad(j=1,2,...,t)$$
称 $p_j(\lambda)^{e_{ij}}$ 为 $A$ 的一个初等因子, 将 $A$ 的全体初等因子称为 $A$ 的初等因子组 .
$A$ 的初等因子组被其不变因子唯一确定, 同样的, 在适当添补 $1$ 之后 (即表示为 $p_j(\lambda)^{e_{ij}}\:(e_{ij}=0)$ ), 可将这组初等因子按不可约因式降幂排列: $$\begin{align}
&p_1(\lambda)^{e_{k1}},p_1(\lambda)^{e_{k-1,1}},...,p_1(\lambda)^{e_{11}}\\
&p_2(\lambda)^{e_{k2}},p_2(\lambda)^{e_{k-1,2}},...,p_2(\lambda)^{e_{12}}\\
&\qquad\qquad\quad\cdots\cdots\\
&p_t(\lambda)^{e_{kt}},p_t(\lambda)^{e_{k-1,t}},...,p_t(\lambda)^{e_{1t}}
\end{align}$$

**定理**: 域 $\mathbf F$ 上的矩阵 $A,B$ 相似的充分条件为它们有相同的初等因子组

即初等因子组为矩阵相似关系的全系不变量。
