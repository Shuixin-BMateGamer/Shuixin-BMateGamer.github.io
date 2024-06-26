
矩阵分解主要旨在简化矩阵，简化运算，同时剖析线性空间的结构，探求各类线性映射的本质，
Jordan标准形理论已将空间结构叙述的较为清晰，完全解决了复方阵的**相似标准形**问题
见笔记 [[Jordan标准型]]
下面是一些常见的另类分解
可能基于不同**研究目的**，基于不同的**数域**，基于不同的矩阵间的**等价关系**或是不同的**特殊矩阵**，也自然基于不同的**研究方法**
$(\mathrm{I})$ 讨论空间：
	$(1)$ 实内积空间
	$(2)$ 酉空间
$(\mathrm{II})$ 矩阵间常见的关系：
	$(1)$ 相抵
	$(2)$ 相似
	$(3)$ 合同
	$(4)$ 酉相似
	$(5)$ 酉等价
$(\mathrm{III})$ 常见矩阵的特点：
	$(0)$ 方阵/非方阵
	$(1)$ 满秩阵
	$(2)$ 可逆阵 （非奇异阵）
	$(3)$ 对称矩阵/斜对称矩阵
	$(4)$ Hermite阵/斜Hermite阵/本性Hermite阵
	$(5)$ 正交矩阵/酉矩阵
	$(6)$ 正规矩阵
	$(7)$ 对角阵/分块对角阵
	$(8)$ 上（下）三角阵/分块上（下）三角阵
$\rm Q$ :
	$1^\circ$ 解决什么问题时需要分解矩阵
	$2^\circ$ 分解什么样的矩阵，分解成什么样的矩阵，猜想结论
	$3^\circ$ 是否有可如此分解的例子，如果有，是否是普遍的
		如果是普遍的，探究一般表达式，寻找分解的共性
		如果不是普遍的，探究反例，寻找可分解条件
	$4^\circ$ 涉及到哪部分矩阵基本理论的内容，可能涉及到的手法与数学工具
	$5^\circ$ 寻找结论的等价命题，哪怕是必要命题或是在更强的条件下考虑
	$6^\circ$ 从低阶/维度的情况入手，如果能证明，试抽象出证明手法
	$7^\circ$ 从多个方面考虑，如果能找到几何直观上的解释最好不过

# 满秩分解
# QR分解

复制自[[有度量的线性空间]]，即

**定理·QR分解**: 设 $A$ 为 $n$ 阶实(复)矩阵, 则 $A$ 可分解为 $$A=QR$$其中 $Q$ 为正交(酉)矩阵, $R$ 为一个主对角线上的元素均大于等于零的上三角阵, 如果 $A$ 是非奇异阵, 则该分解方式唯一

# Cholesky分解
# Schur三角型

复制自[[有度量的线性空间]]，即

**Schur定理**: 设 $V$ 为 $n$ 维酉空间, $\varphi$ 是 $V$ 上的线性算子, 则存在 $V$ 的一组标准正交基, 使 $\varphi$ 在该组基下的矩阵为上三角阵, 即**复矩阵必然可正交相似上三角化**
**[证明]**
	对 $V$ 的维数归纳, $n=1$ 时显然成立
	假设对 $n-1$ 维的酉空间结论成立, 那么对于 $n$ 维酉空间, $\varphi^{*}$ 总有特征值和特征向量, 设 $$\varphi^{*}(e)=\lambda e$$记 $W=\langle e\rangle^{\perp}$ , 则 $V=\langle e\rangle\oplus W$ , $W$ 为 $(\varphi^{*})^{*}=\varphi$ 的不变子空间, 由归纳假设, $\varphi|_{W}$ 在 $n-1$ 维空间 $W$ 上存在一组标准正交基 $e_{1},...e_{n-1}$ 使得 $\varphi|_{W}$ 在该组基下的矩阵为 $n-1$ 阶的上三角矩阵, 在记 $e_{n}=\frac{e}{||e||}$ , 则 $\varphi$ 在基 $e_{1},e_{2},...,e_{n}$ 下的矩阵为上三角矩阵
	即证

# LU分解
# 特征分解(ED)&谱分解(SD)
## 基本内容

特征分解就为矩阵的相似对角化
对于可对角化的矩阵 $A$ , 我们已知其有 $n$ 个线性无关的特征向量 $\eta_k$ , $(A\eta_k=\lambda_k\eta_k)$ 
即存在一组特征向量基 $\eta_1,\eta_2,...,\eta_n$
那么该矩阵满足 $$A(\eta_1,\eta_2,\cdots,\eta_n)=(\lambda_1\eta_1,\lambda_2\eta_2,\cdots,\lambda_n\eta_n)=\underbrace{(\eta_1,\eta_2,\cdots,\eta_n)}_{P}\underbrace{\begin{bmatrix}\lambda_1&0&\cdots&0\\0&\lambda_2&\cdots&0\\\vdots&\vdots&\ddots&\vdots\\0&0&\cdots&\lambda_n\end{bmatrix}}_{\Lambda}$$即有$$A=P\Lambda P^{-1}$$这就称为矩阵的**特征分解**

## 特殊矩阵的谱分解

### 正规矩阵

**正规矩阵谱分解: 
	对于正规矩阵 $A\in M_n$ , 做分解 $A=U\Lambda U^*$ , 这里 $U$ 为酉矩阵, $\Lambda$ 为对角矩阵, 该表示法称为 $A$ 的谱分解**

在此之前，先给出所需的基本概念

**定义**: 矩阵 $A\in M_n$ , 若 $AA^*=A^*A$ , 则将 $A$ 称为**正规矩阵**

为了接下来的讨论，下面是几个将会用到的性质
**性质**:
	$(1)$ 

**引理**: 设 $A\in M_n$, $A=\begin{bmatrix}A_{11}&A_{12}\\0&A_{22}\end{bmatrix}$ , $A_{11}$ 和 $A_{22}$ 都为方阵, 则$$A为正规矩阵\iff A_{11},A_{22}为正规矩阵,且A_{12}=O$$更一般的, 若 $A$ 为分块上三角矩阵, 则 $$A为正规矩阵\iff A的对角线上的分块矩阵都为正规矩阵,且对角线之外的矩阵都为零矩阵$$
**推论**: 分块上三角矩阵为正规矩阵当且仅当它为分块对角矩阵

**定理**: 设 $A=(a_{ij})\in M_n$ , 特征值为 $\lambda_1,\lambda_2,...,\lambda_n$ , 则下面的命题等价: 
	$(a)$ $A$ 为正规阵
	$(b)$ $A$ 可以酉对角化
	$(c)$ $\sum_{i=1}^n\sum_{j=1}^n|a_{ij}|^2=\sum_{k=1}^n|\lambda_k|^2$
	$(d)$ $A$ 有 $n$ 个标准正交的特征向量

### 对称矩阵



# 奇异值分解(SVD)

## 实数域下

复制自[[有度量的线性空间]]，即

**定义**: 设 $A$ 为 $m\times n$ 实矩阵, 如果存在非负实数 $\sigma$ 及 $n$ 维非零实列向量 $\alpha$ , $m$ 维非零实列向量 $\beta$ , 使得 $$A\alpha=\sigma\beta,\qquad A^{\mathrm T}\beta=\sigma\alpha$$将 $\sigma$ 称为 $A$ 的**奇异值**, $\alpha$ , $\beta$ 分别称为 $A$ 关于 $\sigma$ 的**右奇异值向量**和**左奇异值向量**, 

**定义**: 设 $V,U$ 分别为 $n$  维, $m$ 维Euclid空间, $\varphi$ 是 $V\to U$ 的线性映射, 若有 $U\to V$ 的线性映射 $\varphi^*$ , 使对任意的 $v\in V,u\in U$ , 都有$$(\varphi(v),u)=(v,\varphi^*(u))$$成立, 则称 $\varphi^*$ 是 $\varphi$ 的**伴随**

**定理**: 设 $V,U$ 分别是 $n$ 维, $m$ 维Euclid空间, $\varphi$ 是 $V\to U$ 的线性映射, 则 $\varphi$ 的伴随 $\varphi^*$ 存在且唯一

若取定 $V$ 的基 $v_1,v_2,...,v_n$ , $U$ 的基 $u_1,u_2,...,u_m$ , 设 $\varphi$ 在这两组基下的矩阵为 $A=(\alpha_1,\alpha_2,\cdots,\alpha_n)$ , 则可证明 $\varphi^*$ 在这两组基下的矩阵为 $A^{\mathrm T}$

于是奇异值和奇异向量也可以带有几何意义的如下定义$$\varphi(v)=\sigma u,\quad\varphi^*(u)=\sigma v$$这里 $\sigma\geq0$ , $v\in V$ , $u\in U$ 均为非零向量, 

## 复数域下

**奇异值分解**: 给定 $A\in M_{n\times m}$ , 令 $q=\min\{m,n\}$ , 设 $r=\mathrm{rank}\,A$ , 则: 
	$(a)$ 存在酉矩阵 $V\in M_n$ , $W\in M_m$ , 以及对角阵 $$\Sigma_q=\begin{bmatrix}\sigma_1& \ &0\\ \ & \ddots & \ \\0& \ &\sigma_q\end{bmatrix}$$使得 $\sigma_1\geq\sigma_2\geq\cdots\geq\sigma_r>0=\sigma_{r+1}=\cdots=\sigma_q$ 以及 $A=V\Sigma W^*$ , 其中这里 $\Sigma$ 为: $$\Sigma=\begin{cases}\Sigma_q\qquad\qquad& m=n\\\\\begin{bmatrix}\Sigma_q&0\end{bmatrix}\in M_{n\times m}\qquad\qquad&m>n\\\\\begin{bmatrix}\Sigma_q\\0\end{bmatrix}\in M_{n\times m}\qquad\qquad&m<n\end{cases}$$
	$(b)$ 其中的参数 $\sigma_1,...,\sigma_q$ 为 $AA^*$ 或是 $A^*A$ 的非零特征值的正平方根的递减排列
上面方阵 $\Sigma_q$ 的对角元素 $\sigma_1,...,\sigma_q$ 称为 $A$ 的**奇异值**, $A$ 的奇异值 $\sigma$ 的重数是 $\sigma^2$ 作为 $AA^*$ 的特征值的重数. 如果 $\sigma^2$ 是 $AA^*$ 的一个单重特征值, 则将 $A$ 的奇异值 $\sigma$ 称为是**单重的**, 显然有 **$A$ 的秩等于其非零奇异值的个数**, 而 $A$ 的秩不小于 $A$ 的非零特征值的个数, 除奇异值排序外, 对角因子 $\Sigma$ 唯一
**[证明]**
	$(\mathrm{I})$ 当 $m=n$ 时, Hermite矩阵 $AA^*\in M_n$ 与 $A^*A\in M_n$ 有同样的特征值, 从而它们酉相似, 故存在酉矩阵 $U$ , 使得 $A^*A=U(AA^*)U^*$ , 那么 $$(UA)^*(UA)=A^*U^*UA=A^*A=U(AA^*)U^*=(UA)(UA)^*$$因此 $UA$ 为正规矩阵, 设 $\lambda_k=|\lambda_k|e^{i\theta_k}$ $(k=1,2,...,n)$ 为 $UA$ 的特征值, 且 $|\lambda_1|\geq\cdots\geq|\lambda_n|$ ,设 $r=\mathrm{rank}\,A=\mathrm{rank}\,UA$ , 那么 $r$ 为 $UA$ 的非零特征值的个数
	那么   $\lambda_j>0\,(j\leq r)$   ,   $\lambda_j=0\,(r+1\leq j\leq n)$ ,
	记 $\Lambda=\mathrm{diag}\{\lambda_1,\cdots,\lambda_n\}$ , 令 $D=\mathrm{diag}\{e^{i\theta_1},\cdots,e^{i\theta_n}\}$ , $\Sigma_q=\mathrm{diag}\{|\lambda_1|,\cdots,|\lambda_n|\}$ , 那么 $\Lambda=\Sigma_qD$
	设酉矩阵 $X$ , 使得 $UA=X\Lambda X^*$ , 即得到 $$A=U^*X\Lambda X^*=U^*X\Sigma_qDX^*=(U^*X)\Sigma_q(DX^*)$$这里记 $V=U^*X$ , $W=XD^*$ , 即得 $A=V\Sigma_qW^*$ ,
	$V^*V=X^*UU^*X=X^*X=I$ , $W^*W=DX^*XD^*=DD^*=I$ , 因此 $V$ 和 $W$ 都为酉矩阵
	$(\mathrm{II})$ 当 $m>n$ 时, 由于有 $r\leq n$ , 故


# CS分解
# 极分解