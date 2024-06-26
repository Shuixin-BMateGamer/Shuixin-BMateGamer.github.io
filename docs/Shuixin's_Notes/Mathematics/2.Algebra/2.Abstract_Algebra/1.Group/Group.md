
# 基本内容

**笛卡尔积: 设集合 $S,M$ , 称 $S\times M\triangleq\{(s,m)|s\in S,m\in M\}$ 为 $S$ 与 $M$ 的笛卡尔积 .
集合划分: 若集合 $S$ 为其一些两两不交的非空子集 $S_k\:(k=1,2,...,m)$ 的并集, 则称集合 $\{S_1,S_2,...,S_m\}$ 为 $S$ 的一个划分 .
二元关系: 设非空集合 $S$ , 将 $S\times S$ 的一个子集 $W$ 称为 $S$ 上的一个二元关系, 若 $(a,b)\in W$ , 则称 $a$ 与 $b$ 有 $W$ 关系, 记作 $aWb$ 或 $a\sim a$ , 若 $(a,b)\notin W$ , 则称 $a$ 与 $b$ 没有 $W$ 关系 .
等价关系: 集合 $S$ 上的一个二元关系 $\sim$ , 若满足: 
	     $(1)\:a\sim a$ , $\forall \,a \in S$ (反身性)
	     $(2)$ 若 $a\sim b$ 则 $b\sim a$ (对称性)
	     $(3)$ 若 $a\sim b$ 且 $b\sim c$ , 则 $a\sim c$ (传递性)
	    则称 $\sim$ 为 $S$ 上的等价关系 .
等价类: 设 $\sim$ 为集合 $S$ 上的一个等价关系 . 任给 $a\in S$ , 令 $$\bar a\triangleq\{x\in S|x\sim a\}$$
		 则称 $S$ 的这个子集 $\bar a$ 为 $a$ 的等价类 . 将 $a$ 称为等价类 $\bar a$ 的一个代表(元) .
等价关系划分集合: 集合 $S$ 上有一个等价关系 $\sim$ , 则所有的等价类组成的集合是 $S$ 的一个划分 .
商集: 集合 $S$ 上有一个等价关系 $\sim$ , 则所有等价类组成的集合称为 $S$ 对于 $\sim$ 的商集, 记作 $S/\sim$ .
左分配律: $a*(b+c)=a*b+a*c$   右分配率 : $(b+c)*a=b*a+c*a$  (集合有两种二元运算 $*,+$)
交换律:      $ab=ba$      $\forall \,a,b\in S$ 
左幺元:       $\exists\,e\in S$     $\forall \,a \in S$   $s.t.\, ea=a$  称 $e$ 为左幺元
右幺元:       $\exists \,e\in S$     $\forall \,a \in S$   $s.t.\, ae=a$  称 $e$ 为右幺元
幺元: 既为左幺元, 又为右幺元 .**
	_# 幺元也称单位元_
**左(右)消去律: 若 $\forall\,a,b,c\in S$ , 由 $ab=ac\:(ba=ca)$ 可以推出 $b=c$ , 则称 $S$ 满足消去律 .**
# 半群

**定义**: 若非空集合 $S$ 上有一个满足交换律的二元运算 $*$ , 则称 $(S,*)$ 为一个**半群** .

**定义**: 若半群上存在幺元, 则称为**幺半群** .

**定义**: 若幺半群上的运算满足交换律, 则称为**交换幺半群** .

_半群中可能有左（右）幺元但没有右（左）幺元_
_既有左幺元又有右幺元的半群必然为幺半群_

**定义**: 幺半群 $S$ 有幺元 $e$ , 对于 $a\in S$ , 若 $\exists\,b\in S$ 使得 $ba=e\,(ab=e)$ 则称 $b$ 为 $a$ 的**左(右)幺逆元**

_幺半群的幺元唯一_

**定义**: 若 $\exists \,b\in S$ 即为 $a$ 的左逆元, 又为 $a$ 的右逆元, 则称其为 $a$ 的**逆元**, 并称 $a$ 为**可逆元** 

_幺半群中的元素可能存在左（右）逆元但不存在右（左）逆元_
_既有左逆元又有右逆元的元素为可逆元_
_**幺半群中任何可逆元的逆元唯一**_
由唯一性，可以记 $a$ 的逆元为  $a^{-1}$ 
# 群

群是一种由代数运算及其公理在集合上嵌入的基本结构

**定义: 设非空集合 $G$ , 上面定义了一个代数运算, 通常称为乘法 (或加法) , 若满足: 
$(1)$ $(ab)c=a(bc)$    $\forall \,a,b,c\in G$
$(2)\:G$ 中有元素 $e$ , 使得: $ea=ae=a$    $\forall \,a\in G$     称 $e$ 为 $G$ 的单位元
$(3)$ 对于 $G$ 中每个元素 $a$ , 存在 $b\in G$ , 使得: $ba=ab=e$ 
 称a可逆,把b称为a的逆元,记作 $a^{-1}$ , 那么称G为一个群 .
可以证明, 群的单位元唯一, $G$ 中每个元素 $a$ 的逆元唯一, 且 $$(a^{-1})^{-1}=a$$
若群 $G$ 的乘法还满足交换律, 则称 $G$ 为交换群或 $\mathrm{Abel}$ 群 .
可以证明, $\mathbb Z^*_m$ 为一个群, 将其称为 $\mathbb Z_m$ 的单位群. **

**定理**: 若 $G$ 为一个半群, 则 $G$ 为一个群当且仅当 $G$ 满足: 
	$(1)$ $G$ 中存在左(右)幺元, 即 $\exists\,e\in G$ 使得 $\forall\,a\in G$ , 有 $ea=a\:(ae=a)$
	$(2)$ $G$ 中任意元素都有左(右)逆元, 即 $\forall\,a\in G$ , $\exists\,b\in G$ , 使得 $ba=e\:(ab=e)$

**引理**: 群满足左消去律和右消去律

**定理**: 若 $G$ 为一个半群, 则 $G$ 为一个群当且仅当 $G$ 满足 $\forall\,a,b\in G$ , 关于 $x$ 的方程 $ax=b$ 和 $xa=b$ 均有解

**定理**: 若有限半群 $G$ 满足左右消去律, 则 $G$ 为群

_该结论对无限半群不成立_

**定理**: 幺半群 $S$ 中的可逆元的全体记为 $U(S)$ , 则 $U(S)$ 为群

_这也就说明了由于 $(\mathbb Z_m,\cdot)$ 为幺半群，从而 $(\mathbb Z_m^*,\cdot)$ 为一个群_
# 循环群

设 $G$ 为一个群，对于 $a,b\in G$
先完备一些基本的运算：
**\[写成乘法\]**
$(1)\:(ab)^{-1}=b^{-1}a^{-1}\:;(a_1a_2\cdots a_n)^{-1}=a_n^{-1}\cdots a_2^{-1}a_1^{-1}$ 
$(2)\:a^n\triangleq aa\cdots a$ 
$(3)\:a^0\triangleq e$
$(4)\:a^{-n}\triangleq(-a)^n$
$(5)\:a^ma^n=a^{m+n}$
$(6)\:(a^n)^m=a^{mn}$
**\[写成加法\]**
$(1)\:0a\triangleq0$
$(2)\:na\triangleq a+a+\cdots+a\:(n个)$
$(3)\:(-n)a\triangleq n(-a)$

**定义**: 若群 $G$ 有无限个元素, 称 $G$ 为**无限群**; 若群 $G$ 有有限个元素, 称 $G$ 为**有限群**, 对于有限群 $G$ ,称 $G$ 的元素个数为 $G$ 的**阶**, 记作 $|G|$ .

_研究个例：
(I)整数集 $\mathbb Z$ 对于加法称为群，记作 $(\mathbb Z,+)$ ，它的零元为 $0$ 。
(II)模 $m$ 剩余类环 $\mathbb Z_m$ 对于加法成为一个群，记作 $(\mathbb Z_m,+)$ ，它的零元为 $\bar0$ 。
(II)有数论中的结论：**在  $(\mathbb Z_m,\cdot)$ 中，$\bar a$ 为可逆元当且仅当 $a$ 与 $m$ 互素**
而无论如何都有 $(\mathbb Z_m,\cdot)$ 为半群，那么 $(\mathbb Z_m^*,\cdot)$ 为由 $m$ 的缩系内元素做代表元的集合，这个集合关于乘法构成群
_

**定义**: 不妨设群 $G$ 的运算为乘法, 若 $G$ 中的每一个元素都是 $G$ 中某个元素 $a$ 的整数次幂, 则称 $G$ 为**循环群** , 将 $a$ 叫做 $G$ 的一个**生成元**, 将 $G$ 记作 $\langle a\rangle$ .

**定义**: 对于 $G=\langle a\rangle$ , 运算记作乘法, 单位元 $e$ , 若 $\forall\,n\in N^*$ , 都有 $a^n\neq e$ , 则称 $\langle a\rangle$ 为**无限循环群** .

对于循环群 $\langle a\rangle$ , 若 $i\neq j$ , 则必有 $a^i\neq a^j$ 
故 $\langle a\rangle=\{\cdots,a^{-n},\cdots,a^{-1},e,a,a^2,\cdots,a^n,\cdots\}$ 

**定义**: 对于 $G=\langle a\rangle$ , 运算记作乘法, 单位元 $e$ , 若 $\exists\,n\in N^*$ , 使得 $a^n=e$ , 则这个循环群的元素个数有限, 可以定义群的**阶**为 $n$ , 这里 $n=\mathrm{min}\{m\in N^*|a^m=e\}$ , 记作 $n=|a|$ .

_循环群必然为Abel群，但Abel群不一定为循环群_

出于循环群相关定义，可以拓宽到一般的群：

**定义**: 对于群 $G$ 中的元素 $a$ , 若 $\exists\,n\in N^*$ , 使得 $a^n=e$ , 则把使该式成立的最小正整数 $n$ 称为元素 $a$ 的阶, 记作 $|a|$ , 即 $|a|=n=\mathrm{min}\{m\in N^*|a^m=e\}$ ; 若 $\forall n\in N^*$ 有 $a^n\neq e$ , 则称 $a$ 为**无限阶元素** .

**命题**: 有限群 $G$ 是循环群当且仅当有一个元素的阶等于群的阶 .

_注意区分：**群的阶**，**元素的阶**，**循环群的阶**_ 

**命题**: 群 $G$ 的运算为乘法, 若群 $G$ 中元素 $a$ 的阶为 $n$ , 则对于正整数 $m$ , 有 $$a^m=e\iff n|m$$

**命题**: 群 $G$ 的运算为乘法, 设 $G$ 中元素 $a$ 的阶为 $n$ , 则 $\forall\,k\in N^*$ , 有: $$|a^k|=\frac{n}{(n,k)}$$

**命题**: 群 $G$ 中, 若 $ab=ba$ , $a,b$ 的阶分别为 $n,m$ ,且 $(n,m)=1$ , 则 $ab$ 的阶为 $nm$ .

从一个个例探究，考虑Abel群 $\mathbb Z_9^*=\{\bar1,\bar2,\bar4,\bar5,\bar7,\bar8\}$ ，经过计算可得：$$|\bar1|=1,|\bar2|=6,|\bar4|=3,|\bar5|=6,|\bar7|=3,|\bar8|=2$$
这里 $2$ 的阶数 $|\bar2|$ 是其它元素的倍数，猜测出如下结论：

**命题**: 若 $G$ 为有限 $\mathrm{Abel}$ 群, 则 $G$ 中有一个元素的阶是其它元素的阶的倍数 .

**定理**: 设 $G$ 为有限 $\mathrm{Abel}$ 群, 如果对于任给的正整数 $m$ , 方程 $x^m=e$ 在 $G$ 中的解的个数不超过 $m$ , 那么 $G$ 为循环群 .

**定理**: 有限域 $\mathbf F$ 中的所有非零元组成的集合 $\mathbf F^*$ 对于乘法成群, 且 $\mathbf F^*$ 为循环群 .

**推论**: 若 $p$ 为素数, 则 $\mathbb Z^*_p$ 为循环群 .

**定理**: 设 $m$ 为大于 $1$ 的整数, 则 $\mathbb Z^*_m$ 为循环群当且仅当 $m$ 为下列几种情形: $$2,\,4,\,p^r,\,2p^r\qquad这里p为奇素数,r\in \mathbb N^*$$

**定义**: 若群 $G$ 到群 $\widetilde{G}$ 有一个双射 $\sigma$ , 使得 $$\sigma(ab)=\sigma(a)\sigma(b),\qquad\forall\,a,b\in G$$
则称 $\sigma$ 为 $G$ 到 $\widetilde{G}$ 的一个**群同构映射** , 此时称群 $G$ 与群 $\widetilde{G}$ 是**同构的** , 记作 $G\cong\widetilde{G}$ .

**命题**: 设 $\sigma$ 为 $G$ 到 $\widetilde{G}$ 的一个群同构映射, 则: 
	$(1)$ $\sigma(e)=\widetilde{e}$ , $e$ 和 $\widetilde{e}$ 分别为 $G$ 和 $\widetilde{G}$ 的单位元
	$(2)$ $\sigma(a^{-1})=\sigma(a)^{-1},\:\forall a\in G$ 
	$(3)$ $a$ 与 $\sigma(a)$ 阶数相同(如果其中一个是无限阶元素, 那就都为无限阶元素)

可以验证，群同构关系是所有群组成的集合上的一个等价关系，满足反身性，对称性，传递性
如此，将群集合上的群同构关系的等价类称作**同构类** .

**定理**: 
	$(1)$ 任意一个无限循环群都与 $(\mathbb Z,+)$ 同构
	$(2)$ 对于 $m>1$ , 任意一个 $m$ 阶循环群都与 $(\mathbb Z_m,+)$ 同构
	$(3)$ $1$ 阶循环群都与加法群 $\{0\}$ 同构

如此，就有：
	所有无限循环群恰好组成一个同构类，代表元为 $(\mathbb Z,+)$
	所有 $1$ 阶循环群恰好组成一个同构类，代表元为 $(0,+)$ 
	所有 $m\,(m>1)$ 阶循环群恰好组成一个同构类，代表元为 $(\mathbb Z_m,+)$

**定理**: 设 $m_1,m_2$ 为大于 $1$ 的整数, 则 $(\mathbb Z_{m_1}\oplus\mathbb Z_{m_2},+)$ 为循环群当且仅当 $m_1$ 与 $m_2$ 互素 .


# 对称群

## 图形的对称群

用对称群刻画图形的对称性

**定义**: 平面上(或空间中)的一个变换 $\sigma$ 如若保持任意两点间的距离不变, 则称 $\sigma$ 为平面上(或空间中)的一个**正交点变换**(也称**保距变换**) .

**定义**: 平面上(或空间中)的一个正交性变换 $\sigma$ 如果使得图形 $\Gamma$ 的像与自身重合, 则称 $\sigma$ 为图形 $\Gamma$ 的一个**对称(性)变换** .

将图形 $\Gamma$ 的所有对称（性）变换组成的集合记作 $G$
可以证明：对称性变换的乘积（复合）满足结合律，结果仍为对称性变换，恒等变换为 $G$ 上的幺元，且每个对称性变换都可逆，于是 $(G,\circ)$ 为一个群，称为**图形 $\Gamma$ 的对称(性)群**. 

**结论**: 设正 $n$ 边形的中心为 $O$ , 用 $\sigma$ 表示绕点 $O$ 转角为 $\frac{2\pi}{n}$ 的旋转, 用 $\tau$ 表示关于正 $n$ 边形的某条对称轴的反射, 则正 $n$ 边形的对称群为 $D_n$ 为: $$D_n=\langle\sigma,\tau|\sigma^n=\tau^2=I,\tau\sigma\tau=\sigma^{-1}\rangle$$
$\sigma,\tau$ 为 $D_n$ 的两个生成元, 由 $\tau\sigma=\sigma^{-1}\tau=\sigma^{n-1}\tau\neq\sigma\tau$ , 知 $D_n$ 非 $\mathrm{Abel}$ 群, 称为**二面体群**, $|D_n|=2n$ . 

## $n$ 元对称群

最开始是由方程的根的对称性研究起：
如一元二次方程 $x^2+bx+c=0$ 的两个复根 $x_1,x_2$ 满足 $\mathrm{Viete}$ 定理：$$x_1+x_2=-b,\qquad x_1x_2=c$$
记 $\Omega=\{x_1,x_2\}$ ，令 $$\begin{align}\sigma&:\Omega\rightarrow\Omega\\&x_1\rightarrow x_2\\&x_2\rightarrow x_1\end{align}$$
经过变换 $\Omega$ 后，仍然有 $$\begin{align}\sigma(x_1)+\sigma(x_2)&=x_2+x_1=x_1+x_2=-b\\\sigma(x_1)\sigma(x_2)&=x_2x_1=x_1x_2=c\end{align}$$
一个集合的性质经过一个自身上的双射（可逆）变换保持不变，这便是对称性的体现。

**定义**: 一个非空集合 $\Omega$ 到自身的所有双射组成的集合, 记作 $S_{\Omega}$ , $\Omega$ 到自身的任意两个双射的乘积仍然是 $\Omega$ 到自身的双射, 因此映射的乘法是 $S_{\Omega}$ 上的运算, 它满足结合律, $\Omega$ 上的恒等变换 $\mathrm{id}_{\Omega}$ 为 $S_{\Omega}$ 的单位元, $\Omega$ 到自身的任一双射 $\sigma$ 的逆映射 $\sigma^{-1}$ 仍是 $\Omega$ 到自身的双射, 于是 $S_{\Omega}$ 为一个群, 称它为集合 $\Omega$ 上的**全变换群**.
特别地, 若 $\Omega$ 为有限集合, $S_{\Omega}$ 中的任意一个元素称为 $\Omega$ 上的一个置换, 设 $\Omega$ 有 $n$ 个元素, 不妨设 $\Omega=\{1,2,...,n\}$ , 将 $\Omega$ 上的一个置换称为**n元置换**, 称 $\Omega$ 上的全变换群为**n元对称群**, 记作 $S_n$ .
通常将 $S_n$ 上的 $n$ 元置换 $\sigma:\:i\mapsto a_i\:(i=1,2,...,n)$ , 写成下面的形式: $$\sigma=\begin{pmatrix}1&2&\cdots&n\\a_1&a_2&\cdots&a_n\end{pmatrix}$$这里 $a_1,a_2,...,a_n$ 为 $1,2,...,n$ 的一个 $n$ 元排列, 那么每个 $n$ 元置换都给出了一个排列
相反也有, 任给一个 $1,2,...,n$ 的 $n$ 元排列 $a_1,a_2,...,a_n$ , 上面的式子给出了一个 $n$ 元置换
也即, 所有的 $n$ 元置换组成的集合和所有的 $n$ 元排列间有一个一一对应
由于 $n$ 元排列的总数为 $n!$ , 故 $|S_n|=n!$ .

不会引起混淆，置换还可以用这样的方式表示：
例： $(\mathrm{I})$ 置换 $\sigma=\begin{pmatrix}1&2&\cdots&n\\n&1&\cdots&n-1\end{pmatrix}$ 可以写作 $\begin{pmatrix}1&2&\cdots&n\end{pmatrix}$ 
	$(\mathrm{II})$ 置换 $\tau =\begin{pmatrix}1&2&3&4\\4&3&2&1\end{pmatrix}$ 可以写作 $\tau=\begin{pmatrix}14\end{pmatrix}\begin{pmatrix}23\end{pmatrix}$ 
	解释于下面的定义：

**定义**: 如果一个 $n$ 元置换 $\sigma$ 作用后, 将 $i_1$ 映射为 $i_2$ , $i_2$ 映射为 $i_3$ , $\cdots\cdots$ , $i_{r-1}$ 映射为 $i_r$ , $i_r$ 映射为 $i_1$ , 并且其余元素不变, 则称 $\sigma$ 为一个 **$r-$轮换** , 简称为**轮换**, 记作 $(i_1i_2i_3\cdots i_{r-1}i_r)$ , 同样也可以写作 $(i_2i_3i_4\cdots i_{r}i_{1})$ , $(i_3i_4i_5\cdots i_{1}i_2)$ , 等等, 他们都是一样的. 特别地, $2-$轮换称之为**对换** , 现在恒等映射(变换)不仅可以记作 $I$ , $\mathrm{id}$ , 还可以记作 $(1)$ .

**定义**: 当两个轮换无公共元素时, 称它们**不相交** .

_例如：$(13467)$ 和 $(2589)$ 便为两个不相交的轮换_

可以证明，两个不相交的轮换对于乘法（复合映射）是可交换的。

**定理**: $S_n$ 的任一非单位元的置换都能表示成一些两两不交的轮换的乘积, 且除序后表示法唯一 .

_从一个例子：$\sigma=(1234)$ 的逆 $\sigma^{-1}=(1432)$ 
可以归纳出结论：$(i_1i_2\cdots i_{r-1}i_r)^{-1}=(i_1i_ri_{r-1}\cdots i_2)$
从：$(1234)=(12)(13)(14)$
也可以归纳出结论：$(i_1i_2i_3\cdots i_{r-1}i_r)=(i_1i_r)(i_1i_{r-1})\cdots(i_1i_3)(i_1i_2)$         
（直观来看无非就是一个位一个位的移）

上述两个结论直接计算验证即可得到

**给出一种书写计算方法的格式：
$$\begin{align}
&比如如果要计算:
(i_{m1}i_{m2}\cdots i_{mr})(i_{(m-1)1}i_{(m-1)2}\cdots i_{(m-1)r})\cdots(i_{11}i_{12}\cdots i_{1r})\\
&这里\,i_{k1},i_{k2},\cdots,i_{kr} 为\,1,2,...,r\, 的一个排列\\
&可以做一个与原像\,12\cdots r相关联的式子\\
&即\qquad
\\&\qquad\qquad(i_{m1}i_{m2}\cdots i_{mr})(i_{(m-1)1}i_{(m-1)2}\cdots i_{(m-1)r})\cdots(i_{11}i_{12}\cdots i_{1r})|12\cdots r\rangle\\
&然后从右至左依次计算(右边关联的部分经最近的轮换作用)\\
&\qquad\qquad(i_{m1}i_{m2}\cdots i_{mr})(i_{(m-1)1}i_{(m-1)2}\cdots i_{(m-1)r})\cdots{\color{red}(i_{11}i_{12}\cdots i_{1r})|12\cdots r}\rangle\\
&得到(这里右边关联的部分改为上一步得到的像,然后作这一步的原像)\\
&\qquad\qquad(i_{m1}i_{m2}\cdots i_{mr})(i_{(m-1)1}i_{(m-1)2}\cdots i_{(m-1)r})\cdots(i_{21}i_{22}\cdots i_{2r})|{\color{red}i_{11}i_{12}\cdots i_{1r}}\rangle\\
&进一步计算\\
&\qquad\qquad(i_{m1}i_{m2}\cdots i_{mr})(i_{(m-1)1}i_{(m-1)2}\cdots i_{(m-1)r})\cdots{\color{blue}(i_{21}i_{22}\cdots i_{2r})|i_{11}i_{12}\cdots i_{1r}}\rangle\\
&一直这样逐个计算\\
& \qquad\qquad\qquad\qquad\qquad\qquad\qquad\qquad\cdots\cdots\\
&一直到\\
&\qquad\qquad\qquad\qquad\qquad\qquad(i_{m1}i_{m2}\cdots i_{mr})|{\color{purple}I^{'}_1I^{'}_2\cdots I^{'}_r}\rangle\\
&这里I^{'}_1I^{'}_2\cdots I^{'}_r为前m-1步计算的结果\\
&最后得到结果\\
& \qquad\qquad\qquad\qquad\qquad\qquad\qquad\quad{\color{purple}(I_1I_2\cdots I_r)}
\end{align}
$$**

**推论**: $S_n$ 中每一个置换都可以表示为一些对换的乘积 . (表示法并不唯一)

**命题**: $S_n$ 中的一个置换表示为对换的乘积, 其中对换的个数的奇偶性由这个置换本身决定, 与本身无关 .

**定义**: 若置换 $\sigma$ 可以表示为偶数个对换的乘积, 则称其为**偶置换**; 若可以表示为奇数个对换的乘积, 则称其为**奇置换** .

_对换都是奇置换，$S_n$ 的单位元 $(1)$ 是偶置换_

由于两个偶置换的乘积显然还为偶置换，于是如若将 $S_n$ 中所有的偶置换组成的集合记作 $A_n$ ，可以验证其满足：$(i)$ 存在幺元 $(1)$ ； $(ii)$ 运算为映射乘法满足结合律 ； $(iii)$ 每个元素均在 $A_n$ 中可逆
那么 $(A_n,\circ)$ 成群：

**定义**:  $S_n$ 中所有的偶置换组成的集合 $A_n$ , $(A_n,\circ)$ 称为**n元交错群** .

$S_n$ 的任意一个奇置换乘以 $(12)$ 为一个偶置换，任意一个偶置换乘以 $(12)$ 为一个奇置换，如此可知存在一个奇置换集与偶置换集间的双射，那么由于为有限集，故有： $|A_n|=\frac{|S_n|}{2}=\frac{n!}{2}$ .

**定义**: 设 $S$ 为群 $G$ 的一个非空子集, 若 $G$ 中每个元素都可以表示成 $S$ 中有限多个元素的整数次幂的乘积, 则称 $S$ 为**群 $G$ 的生成元集** , 或是说 **$S$ 的所有元素生成 $G$** .
如果群 $G$ 的一个生成元集为有限集, 则称 $G$ 为**有限生成的群**, 若这个生成元集为 $\{a_1,a_2,...,a_t\}$ , 则记作: $G=\langle a_1,a_2,...,a_t\rangle$ .

_有限群一定是有限生成的，但无限群则不然，如 $(\mathbb Z,+)$ 就是由 $1$ 生成的，但显然它是无限群_



# 子群

由对称群相关讨论可以看到，$A_n$ 作为对称群 $S_n$ 的一个子集，若将 $S_n$ 中的运算放到 $A_n$ 中， $A_n$ 关于这个运算仍成群，由此引出定义：

**定义**: 若群 $G$ 的非空子集 $H$ 对于 $G$ 的运算也成为一个群, 那么称 $H$ 为 $G$ 的一个**子群**, 记作 $H<G$ .

_$n$ 元对称群 $S_n$ 的任一子群称为 **$n$ 元置换群**_
_非空集合 $\Omega$ 上的全变换群 $S_{\Omega}$ 的任一子群称为 $\Omega$ 上的**变换群**_
_群 $G$ 中，仅由单位元素 $e$ 组成的子集 $\{e\}$ 为 $G$ 上的一个子群，$G$ 本身也是 $G$ 的一个子群，$\{e\}$ 和 $G$ 称为 $G$ 的**平凡子群**_

**命题**: 若群 $G$ 有非空子集 $H$ , 则 $H$ 为子群当且仅当 $\forall a,b\in H,\:ab^{-1}\in H$ .

类似于**线性空间**和**子空间**
可以利用群的子群研究群的结构

利用子群，可以对 $G$ 进行划分，在此之前需要建立 $G$ 上的等价关系

_类比几何空间中的等价关系建立法，当时利用 $R^3$ 的子空间（过原点的直线或平面 $\pi$ ），对于 $\forall\:\vec{a},\vec{b}\in R^3$ ，建立等价关系：$\vec a\sim \vec b:\iff \vec a-\vec b\in\pi$

于是受到启发，可建立群 $G$ 上的等价关系：
已知 $H$ 为 $G$ 的一个子群，
规定群 $G$ 上的二元关系：$$a\sim b:\iff ab^{-1}\in H$$
不难验证 $\sim$ 为 $G$ 上的等价关系

**定义**: 
	$(\mathrm I)$ 定义群 $G$ 上的等价关系 $\sim\,:\:a\sim b\iff ab^{-1}\in H$ , 这里 $H$ 为 $G$ 的一个子群. 任取 $a\in G$ , 可以给出等价类 $\widetilde{a}=\{x\in G|\,x\sim a\}=\{x\in G|\,xa^{-1}\in H\}=\{x\in G|\,xa^{-1}=h,h\in G\}=\{x\in G|\,x=ha,h\in H\}\triangleq Ha$ 称 $Ha$ 为 $H$ 的一个**右陪集**, $a$ 称为**陪集代表**, 那么 $H$ 的所有右陪集就组成了 $G$ 的一个划分, 将该划分称为 $G$ 的**右商集**, 记为 $(G/H)_r$ .
	$(\mathrm {II})$ 定义群 $G$ 上的等价关系 $\sim\,:\:a\sim b\iff b^{-1}a\in H$ , 这里 $H$ 为 $G$ 的一个子群. 任取 $a\in G$ , 可以给出等价类 $\widetilde{a}=\{x\in G|\,x\sim a\}=\{x\in G|\,a^{-1}x\in H\}=\{x\in G|\,a^{-1}x=h,h\in G\}=\{x\in G|\,x=ah,h\in H\}\triangleq aH$ 称 $aH$ 为 $H$ 的一个**左陪集**, $a$ 称为**陪集代表**, 那么 $H$ 的所有左陪集就组成了 $G$ 的一个划分, 将该划分称为 $G$ 的**左商集**, 记为 $(G/H)_l$ .

可以建立对应关系：$$\begin{align}\sigma:(G/H)_l&\to(G/H)_r\\aH&\mapsto Ha^{-1}\end{align}$$
可以证明，同一陪集选取不同代表元不会影响结果，故为映射
可以证明，映射为单射
可以证明，映射为满射
总之，该映射为建立在 $(G/H)_l$ 与 $(G/H)_r$ 间的双射
故有 $|(G/H)_l|=|(G/H)|_r$ （这里表示集合的基数）

**定义**: 设 $H$ 是群 $G$ 的一个子群, 把 $(G/H)_l$ 或 $(G/H)_r$ 的基数称为 $H$ 在 $G$ 中的**指数**, 记作 $[G:H]$ .
	若群 $G$ 的子群 $H$ 在 $G$ 中的指数为 $[G:H]=r$ , 则$$G=H\cup a_1H\cup a_2H\cup\cdots\cup a_{r-1}H$$	这里 $H,a_1H,a_2H,...,a_{r-1}H$ 两两不交.
	将上式关于 $G$ 的集合分解称为群 $G$ 关于子群 $H$ 的**左陪集分解式**, 将 $\{e,a_1,a_2,...,a_{r-1}\}$ 称为 $H$ 在 $G$ 中的**左陪集代表系** . (类似可以定义右陪集相关概念)

可以建立对应关系：$$\begin{align}\tau:H&\to aH\\h&\mapsto ah\end{align}$$
不难知道，$\tau$ 为一个映射，为单射，满射，如此，$\tau$ 为一个 $H$ 与 $aH$ 间的双射，故 $H$ 与 $aH$ 间的基数也是相同的 。

现在可以证明：

**Lagrange定理: 设 $G$ 为有限群, $H$ 为 $G$ 的任意子群, 则 $$|G|=[G:H]|H|$$
故 $G$ 的任意子群 $H$ 的阶为 $G$ 的阶的因数 .**

**定义**: 设 $G$ 为一个有限群, $a\in G$ , 设 $a$ 的阶为 $s$ , 记 $$H=\{e,a,a^2,...,a^{s-1}\}$$
由于对于 $\forall i,j\in\{0,1,...,s-1\}$ (不妨 $i\leq j$ ) , 有: $$a^ia^{-j}=a^{i-j}=a^{-(j-i)}=ea^{j-i}=a^{s-(j-i)}\in H$$
(因为 $s-(j-i)\in\{0,1,...,s-1\}$) , 故 $H$ 为 $G$ 的子群, 将它称为是**由 $a$ 生成的子群, 记作 $\langle a\rangle$ 

显然的有：$|\langle a\rangle|=|a|$ 。

**推论**: 设 $G$ 为有限群, 则 $G$ 的任意有限元素 $a$ 的阶均为 $G$ 的阶数的因数, 也就有 $a^{|G|}=e$ .

**推论**: 素数阶群必然为循环群 .

作为应用，利用上面的结论，可以做出数论中的欧拉定理和费马小定理的简短证明：

**\*Euler定理**: 设 $m$ 为大于 $1$ 的整数, 若整数 $a$ 与 $m$ 互素, 则 $$a^{\varphi(m)}=1\quad(\mathrm{mod}\:m)$$

**\*Fermat小定理**: 设 $p$ 为素数, 则对于任意整数 $a$ , 有 $$a^p\equiv a\quad(\mathrm{mod}\:m)$$

现在研究有限循环群的所有子群，

**定理**: 设 $G=\langle a\rangle$ 为 $n$ 阶循环群, 则有: 
	$(1)$ $G$ 的每一个子群都为循环群 .
	$(2)$ 对于 $G$ 的阶 $n$ 的每一个正因数 $s$ , 都存在一个唯一的一个 $s$ 阶子群, 它们为 $G$ 的全部子群 .

## \*四阶群的同构类

考察任一四阶群 $G=\{e,g_1,g_2,g_3\}$ ，考察非单位元元素的阶，若 $g\in G$ , 则 $|g|$ 为 $|G|=4$ 的非幺因子，也即 $|g|=2$ 或 $|g|=4$ .
分类讨论：
	_情形一：若 $G$ 有四阶元 $a$ ，则直接得到 $G=\langle a\rangle$ ，故 $G\cong (\mathbb Z_4,+)$。
	情形二：若 $G$ 无四阶元，则 $|g_1|=|g_2|=|g_3|=2$ ，由此可以得到：$$g_1g_2\neq e\qquad g_1g_2\neq g_1\qquad g_1g_2\neq g_2$$
	因此有 $g_1g_2=g_3$ ，同理有 $g_2g_1=g_3$ ，类似还可得到其他结论
	总之有：$$\begin{align}&g_1g_2=g_3=g_2g_1\\&g_2g_3=g_1=g_3g_2\\&g_3g_1=g_2=g_1g_3\end{align}$$可知 $G$ 为 $\mathrm{Abel}$ 群。
	定义：$$\begin{align}\sigma:G&\to(\mathbb Z_2\oplus\mathbb Z_2,+)\\e&\mapsto(\bar0,\bar0)\\g_1&\mapsto(\bar0,\bar1)\\g_2&\mapsto(\bar1,\bar0)\\g_3&\mapsto(\bar1,\bar1)\end{align}$$
	易证 $\sigma$ 为双射，并可以进一步验证其满足 $$\begin{align}&\sigma(ab)=\sigma(a)+\sigma(b),\quad\forall\,a,b\in G\end{align}$$
	于是 $\sigma$ 为一个 $G$ 到 $(\mathbb Z_2\oplus\mathbb Z_2,+)$ 的同构映射，即有 $G\cong(\mathbb Z_2\oplus\mathbb Z_2,+)$ 。

_# 上面的群 $(\mathbb Z_2\oplus\mathbb Z_2,+)$ 称为**Klein**群，或是**四群**，通常记作 $V$_

# 群的直积（直和）

经过上面有关Klein群的讨论，注意到它的形式 $(\mathbb Z_2\oplus\mathbb Z_2,+)$ ，抛开上面定义运算不谈，他本身是一个集合，由 $\mathbb Z_2\oplus\mathbb Z_2$ 得到，再补充上运算 $'+'$ 。
经启发引出定义：

**定义**: 
	$(\mathrm I)$ 设 $G,\widetilde{G}$ 为两个群, 它们的运算均为乘法, 在 $G\times\widetilde{G}$ 上定义乘法运算: $$(g_1,\tilde{g_1})(g_2,\tilde{g_2})\triangleq(g_1g_2,\tilde{g_1}\tilde{g_2})$$
	该运算是 $G\times\widetilde{G}$ 到自身的映射, 并满足结合律, 且可以验证 $(e,\tilde{e})$ 为 $G\times\widetilde{G}$ 的单位元( $e$ 和 $\tilde{e}$ 分别为它们的幺元), 且 $(g,\tilde{g})$ 总有逆元 $(g^{-1},\tilde{g}^{-1})$ , 总之可知 $G\times\widetilde{G}$ 为一个群, 称之为 群 $G$ 与 群 $\widetilde{G}$ 的**直积**, 仍然记作 $G\times\widetilde{G}$ .
	$(\mathrm{II})$ 设 $G,\widetilde{G}$ 为两个群, 它们的运算均为加法, 在 $G\times\widetilde{G}$ 上定义加法运算: $$(g_1,\tilde{g_1})+(g_2,\tilde{g_2})\triangleq(g_1+g_2,\tilde{g_1}+\tilde{g_2})$$
	该运算是 $G\times\widetilde{G}$ 到自身的映射, 并满足结合律, 且可以验证 $(0,\tilde{0})$ 为 $G\times\widetilde{G}$ 的单位元( $0$ 和 $\tilde{0}$ 分别为它们的零元), 且 $(g,\tilde{g})$ 总有负元 $(-g,-\tilde{g})$, 总之可知 $G\times\widetilde{G}$ 为一个群, 称之为 群 $G$ 与 群 $\widetilde{G}$ 的**直和**, 记作 $G\oplus\widetilde{G}$ .

考虑一个映射 $$\begin{align}\sigma:G\times \widetilde{G}&\to\widetilde{G}\times G\\ (g,\tilde{g})&\mapsto(\tilde{g},g)\end{align}$$
显然 $\sigma$ 为双射，且有 $\sigma((g_1,\tilde{g_1})(g_2,\tilde{g_2}))=\sigma((g_1g_2,\tilde{g_1}\tilde{g_2}))=(\tilde{g_1}\tilde{g_2},g_1g_2)=(\tilde{g_1},g_1)(\tilde{g_2},g_2)=\sigma(g_1)\sigma(g_2)$ 
如此，$\sigma$ 为群同构映射，$G\times\widetilde{G}$ 与 $\widetilde{G}\times G$ 同构。

$G\times\widetilde{G}$ 的子集 $\{(g,\tilde{e})|g\in G\}$ 为一个 $G\times\widetilde{G}$ 的子群，也即 $G\times\{\tilde{e}\}<G\times\widetilde{G}$ ，同理有 $\{e\}\times\widetilde{G}<G\times\widetilde{G}$ ，也不难知道有 $G\times\{\tilde{e}\}\cong G\times\widetilde{G}\cong\{e\}\times\widetilde{G}$ 。

更一般的有：

**定义** 有群 $G_1,G_2,...,G_s$ , 运算均为乘法, 在 $G_1\times G_2\times\cdots\times G_s$ 上定义运算: $$(x_1,x_2,...,x_s)(y_1,y_2,...,y_s)\triangleq(x_1y_1,x_2y_2,...,x_sy_s)$$
可以证明, $G_1\times G_2\times\cdots\times G_s$ 关于该运算成群, 将这个群称之为 $G_1\times G_2\times\cdots\times G_s$ 的**直积**, 仍记作 $G_1\times G_2\times\cdots\times G_s$ .
类似可以定义**直和**, 记作 $G_1\oplus G_2\oplus\cdots\oplus G_s$ .

通过群的子群的直和或直积可以研究群的结构

**定理**: 已知 $H,K$ 为群 $G$ 的两个子群,
	则 $H\times K\cong{G}$ , 且有 $H\times K$ 到 $G$ 的同构映射 $\sigma:(h,k)\mapsto{hk}$ 当且仅当: $$\begin{align}&(\mathrm1)\,G=HK\\&(\mathrm2)\,H\cap K=\{e\}\\&(3)\,H中每个元素与K中每个元素可交换\end{align}$$
**定义**: 设 $H,K$ 为群 $G$ 的两个子群, 如果 $H\times K\cong G$ , 其同构映射为 $(h,k)\mapsto hk$ , 那么称 $G$ 是他的子群 $H$ 与 $K$ 的**内直积**, 一般可记作 $G=H\times K$ . $G$ 中的每个元素 $g$ 能唯一地表示为 $g=hk$ , $h\in H$ , $k\in K$ .

更一般的：

**定理**: 已知 $H_1,H_2,...,H_s$ 为群 $G$ 的子群, 
	$G$ 的运算为加法, 则 $H_1\oplus H_2\oplus\cdots\oplus H_s\cong G$ , 且其同构映射为 $(h_1,...,h_s)\mapsto h_1+...+h_s$ 当且仅当: $$\begin{align}&(1)\,G=H_1+H_2+\cdots+H_s\\&(2)\,H_i\cap(\sum_{j\neq i}H_j)=\{e\},\,i=1,2,...,s\\&(3)\,H_i的每个元素与H_j的每个元素可交换,\,i\neq j,1\leq i,j\leq s\end{align}$$
**定义**: 设 $H_1,H_2,...,H_s$ 均为群 $G$ 的 (运算为加法) 子群, 如果 $H_1\oplus H_2\oplus\cdots\oplus H_s\cong G$ , 其同构映射为 $(h_1,h_2,...,h_s)\mapsto h_1+h_2+\cdots+h_s$ 
那么称 $G$ 是它的子群 $H_1,H_2,...,H_s$ 的**内直和**, 一般记作$$G=H_1\oplus H_2\oplus\cdots\oplus H_s$$

# 群的同态

令$$\begin{align}\sigma:(\mathbb Z,+)&\to(\mathbb Z_m,+)\\k&\mapsto\bar k\end{align}$$
则 $\sigma$ 为 $(\mathbb Z,+)$ 到 $(\mathbb Z_m,+)$ 的一个映射, 并且 $\forall\,k,l\in\mathbb Z$ , 有$$\sigma(k+l)=\overline{k+l}=\bar k+\bar l=\sigma(k)+\sigma(l)$$
由该例可引出概念：

**定义**: 若群 $G$ 到群 $\tilde{G}$ 有一个映射 $\sigma$ ,使得$$\sigma(ab)=\sigma(a)\sigma(b)\qquad\forall\,a,b\in G$$
则称 $\sigma$ 为群 $G$ 到 $\tilde{G}$ 的一个**同态映射**, 简称为**同态** .
若 $\sigma$ 为单射, 则称 $\sigma$ 为**单同态**; 若 $\sigma$ 为满射, 则称 $\sigma$ 为**满同态** .

**性质**: 
	$(1)$ $\sigma(e)=\tilde{e}$ , 这里 $e,\tilde{e}$ 分别为 $G,\widetilde{G}$ 的单位元
	$(2)$ $\sigma(a^{-1})=\sigma(a)^{-1}$ , $\forall a\in G$
	$(3)$ $G$ 的子群 $H$ 在 $\sigma$ 下的像 $\sigma(H)$ 是 $\widetilde{G}$ 的子群; 特别地, $\sigma(G)$ 是 $\widetilde{G}$ 的子群, $\sigma(G)$ 记作 $\mathrm{Im}G$ .
	$(4)$ 若 $a\in G$ 且 $a^n=e$ , 则 $\sigma(a)^n=\tilde{e}$ ,也即若 $a$ 为 $G$ 的 $n$ 阶元, 则 $\sigma(a)$ 的阶是 $n$ 的一个因数 .

在$$\begin{align}\sigma:(\mathbb Z,+)&\to(\mathbb Z_m,+)\\k&\mapsto\bar k\end{align}$$
中，$\mathbb Z_m$ 的零元 $\bar0$ 的原像集 $\sigma^{-1}(\bar0)=\{lm|\,l\in\mathbb Z\}=m\mathbb Z$ 

由此引出定义：

**定义**: 设 $\sigma$ 是群 $G$ 到 $\widetilde{G}$ 的一个同态, 则 $\widetilde{G}$ 的单位元 $\tilde{e}$ 在 $\sigma$ 下的原像集称为称为 $\sigma$ 的**核**, 记作 $\mathrm{Ker}\sigma$, 即$$\mathrm{Ker}\sigma\triangleq\{a\in G|\,\sigma(a)=\tilde{e}\}$$
**命题**: $\sigma$ 为群 $G$ 到 $\widetilde{G}$ 的一个同态, 则 $\mathrm{Ker}\sigma$ 是 $G$ 的一个子群 .

**命题**: $\sigma$ 为群 $G$ 到 $\widetilde{G}$ 的一个同态, 则 $\sigma$ 是单射当且仅当$$\mathrm{Ker}\sigma=\{e\}$$
**命题**: $\sigma$ 是群 $G$ 到 $\widetilde{G}$ 的一个同态, 则 $\forall\,a\in G$ , 有 $$a(\mathrm{Ker\sigma})=(\mathrm{Ker}\sigma)a$$ 
**定义**: 如果群 $G$ 的子群 $H$ 满足: $\forall a\in G$ , 有 $$aH=Ha$$ 
则称 $H$ 为 $G$ 的**正规子群**, 记作 $H\lhd G$ . 特别地, $\{e\},G$ 为 $G$ 的正规子群, 称为**平凡正规子群** .

**命题**: 设 $\sigma$ 是群 $G$ 到 $\widetilde{G}$ 的一个同态, 则 $\mathrm{Ker}\sigma$ 是 $G$ 的一个正规子群 .

**命题**: 群 $G$ 的子群 $H$ 是 $G$ 的正规子群当且仅当$$aHa^{-1}=H$$

**证明/定义**: 若 $H$ 为群 $G$ 的一个子群, 任取 $a\in G$ , 则 $aHa^{-1}$ 也是 $G$ 的一个子群, 称它为 $H$ 的一个**共轭子群** .

