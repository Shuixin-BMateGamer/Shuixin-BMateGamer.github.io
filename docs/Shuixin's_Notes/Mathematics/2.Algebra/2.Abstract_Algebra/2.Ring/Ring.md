
# 环

相对于群，环是具有两种运算法则的代数体系，再结合律基础上以分配律建立了两种运算间的关系

**定义**: 设 $R$ 为一个非空集合, 如果在 $R$ 中有两种二元运算, 且满足: 
	$(1)$ $R$ 对于其中一种运算(记为加法 $'+'$ )成为交换群, 即 $(R,+)$ 为交换群
	$(2)$ $R$ 对于另外一种运算(记为乘法 $'\cdot'$ )称为半群, 即 $(R,\cdot)$ 为半群
	$(3)$ 两种运算间满足分配律$$a\cdot(b+c)=a\cdot b+a\cdot c\qquad\qquad(a+b)\cdot c=a\cdot c+b\cdot c\qquad\qquad\forall\,a,b,c\in R$$则称 $R$ 为一个**环** , 可记作 $(R\,;+,\cdot)$ 或 $\{R\,;+,\cdot\}$
	如若 $(R,\cdot)$ 有幺元, 则称 $R$ 为**幺环**; 如若 $(R,\cdot)$ 满足交换律, 则称 $R$ 为**交换环** .

**之后乘法 $a\cdot b$ 均简记为 $ab$**

**性质**:
	$(1)$ $(m+n)a=ma+na$ , $m(-a)=-(ma)$ , $(mn)a=m(na)$ , $m(a+b)=ma+mb$
	$(2)$ $a^ma^n=a^{m+n}$ , $(a^m)^n=a^{mn}$
	$(3)$ $(\sum_{i=1}^na_i)(\sum_{j=1}^mb_j)=\sum_{i=1}^n\sum_{j=1}^ma_ib_j$ 
	$(4)$ $\forall a,b\in R$ , 有 $a0=0a=0$ , $0$ 为 $(R,+)$ 中的零元; $(-a)b=a(-b)=-(ab),(-a)(-b)=ab$

**定义**:
	$(1)$ 设 $R$ 为一个环, $a,b\in R$ , 且 $a\neq0,b\neq0$ , 若 $ab=0$ , 则称 $a$ 为 $R$ 中的一个**左零因子**, $b$ 为 $R$ 中的**右零因子**, 都简称为**零因子** .
	$(2)$ 设 $R$ 为一个环, 若由 $ax=ay,a\neq0$ 可以推出 $x=y$ , 则称 $R$ 满足**左消去律**; 若由 $xa=ya,a\neq0$ 可以推出 $x=y$ , 则称 $R$ 满足**右消去律** .

**命题**: 环 $R$ 没有零因子的充要条件为其满足左右消去律 .

**定义**: 若环 $R$ 不是零环, 且其没有零因子, 则称 $R$ 为**无零因子环** .

**命题**: 设无零因子环 $R$ , 记 $R^*=R-\{0\}$ , 则 $R^*$ 中的元素对于 $R$ 的加法具有相同的阶, 且当这共同的阶有限时, 该阶必为素数 .

**定义**: 设无零因子环 $R$ , 若 $R$ 中所有的非零元都是无穷阶的, 则称 $R$ 的**特征**为 $0$ ; 若 $R$ 中所有的非零元都是 $p$ 阶的 ( $p$ 必为素数) , 则称 $R$ 的**特征**为 $p$ . 记环 $R$ 的特征记为 $\mathrm{char}\,R$ .

**命题**: 设 $R$ 是无零因子的交换环, $\mathrm{char}\,R=p$, $p$ 为素数, 则对任意的 $a,b\in R$ , 有
	$(1)$$$(a+b)^p=a^p+b^p\qquad\qquad(a-b)^p=a^p-b^p$$
	$(2)$$$(a+b)^{p^n}=a^{p^n}+b^{p^n}\qquad\qquad(a-b)^{p^n}=a^{p^n}-b^{p^n}$$$\forall n\in N$

# 理想，商环

类似于研究子空间和商空间，子群和商群，同样可以用子环和商环的子体系和商体系研究环的结构

**定义**: 设 $R_1$ 为环 $R$ 的非空子集, 若 $R$ 中的运算对于 $R_1$ 仍成环, 则称 $R_1$ 为 $R$ 的子环 .

_例如：
	（1）$m\mathbb Z$ 为 $\mathbb Z$ 的子环（还可以证明 $\mathbb Z$ 的非零子环必然形如 $m\mathbb Z$）_
    _（2）$\mathbb Z^{n\times n}$ 为 $\mathbb F^{n\times n}$ 的子环，这里 $\mathbb F$ 为数域_
    _（3）$C^{\infty}(\mathbb R^n)$ 为 $C(\mathbb R^n)$ 的子环_

**命题**: 若 $R$ 为环, $R_1$ 为 $R$ 的非空子集, 则 $R_1$ 为 $R$ 的子环的充要条件为: $\forall a,b\in R_1$ 有 $a-b\in R_1,ab\in R_1$ .
