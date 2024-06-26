**酉矩阵**是一种特殊的非奇异矩阵，具有更加好的性质：$S^{-1}=S^*$ 。
## 一些定义

**定义**: 若 $A=(a_{ij})\in M_{m,n}(\mathbf F)$ , 则 $A$ 的**转置**（记为 $A^{\mathrm T}$）是 $M_{n,m}(\mathbf F)$ 中的一个矩阵, 满足 $A^{\mathbf T}(i;j)=A(j;i)$ . $A$ 的**共轭转置** $A^*$ （有时也称为**伴随**或**Hermite伴随**）, 记作 $A^*$ , 定义为 $A^*=\overline A^{\mathrm T}$ , 满足 $A^*(i;j)=\overline{A(j;i)}$ .

**对称的**: 满足 $A^{\mathrm T}=A$ .
**斜对称的**: 满足 $A^{\mathrm T}=-A$ .
**Hermite的**: 满足 $A^*=A$ .
**斜Hermite的**: 满足 $A^*=-A$ .
**本性Hermite的**: 满足 $\exists\,\theta\in\mathbf R,s.t.e^{i\theta}A$ 为**Hermite的** .
**酉的**: 满足 $A^*A=I$ .
**正规的**: 满足 $A^*A=AA^*$ .
**对称部分**: $S(A)={1\over2}(A+A^{\mathrm T})$ .
**斜对称部分**: $C(A)={1\over2}(A-A^{\mathrm T})$ .
**实部**: $\mathrm{Re}(A)={1\over2}(A+\overline A)$ .
**虚部**: $\mathrm {Im}(A)={1\over2}(A-\overline A)$ .
**Hermite部分**: $H(A)={1\over2}(A+A^*)$ .
**斜Hermite部分**: $iK(A)={1\over2}(A-A^*)$ .
**Toeplitz分解**: 做分解 $A=H(A)+iK(A)$ .
**迹**:  $A=[a_{ij}]\in M_{m,n}(\mathbf F),\,\mathrm{tr}(A)=a_{11}+a_{22}+...+a_{qq},\,q\in\mathrm{min}\{m,n\}$ .
（$\mathrm{tr}AA^*=\mathrm{tr}A^*A=\sum_{i,j}|a_{i,j}|^2$ , 故 $\mathrm{tr}AA^*=0$ 当且仅当 $A=0$ ）
**迷向的**: $x^{\mathrm T}x=0$ .

## 酉矩阵与QR分解

**定义**: 一列向量 $x_1,...,x_k$ , 若对 $\forall i\neq j;i,j\in\{1,...,k\}$ 有 $x_i^*x_j=0$ 则称它们是**正交的**. 特别地若有 $\forall i\in\{1,...,k\}$  有 $x_i^*x_i=1$ , 则称它们是**标准正交的**.

**定理**: $C^n$ 中正交的向量组线性无关

下面一些命题等价: 
	$(1)$ $U$ 为酉矩阵
	$(2)$ $U^*U=I$
	$(3)$ $U^*$ 为酉矩阵
	$(4)$ $U$ 的行向量组为标准正交的
	$(5)$ $U$ 的列向量组为标准正交的
	$(6)$ $\forall\,x\in C^n$ , $|x|=|Ux|$

前面几条性质的显然的，关注于 $(6)$ ，引出定义：

**定义**: 如果 $\forall\,x\in C^n$ , 都有 $|x|=|Tx|$ , 确切来讲是 $||x||_2=||Tx||_2$ , 此时称线性算子 $T$ 是**Euclid等距**的

由此看来，一个复矩阵为酉矩阵当且仅当它是Euclid等距的

