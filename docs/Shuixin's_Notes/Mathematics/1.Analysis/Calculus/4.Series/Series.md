_#历史上开始时微积分尚不严谨时，级数相关的研究甚至早于数列，极限等严格化定义_
# 数项级数

## 基本内容

数项级数形式上是可数无穷个数之和，本质上是极限过程，这样的结果并不在四则运算的范畴内，也即如一定要算出个结果来，就需要再填人为定义，当然，必须是合理的。

下面是一种最常见的定义数项级数结果的方法：

 **定义**: 无穷级数 $$\sum_{n=1}^{\infty}a_n=a_1+a_2+\cdots+a_n+\cdots$$的前 $n$ 项和$$S_n=a_1+a_2+\cdots+a_n$$称为这个技术的第 $n$ 个**部分和** . 若部分和数列 $\{S_n\}$ 有有限的极限 $S$ , 则称该级数**收敛**, 其**和**为 $S$ .
记作: $$\sum_{n=1}^{\infty}a_n=S$$ 若 $\{S_n\}$ 无有限的极限, 则称该级数**发散** .

两类可以用基本方法求出结果的级数：
	$(1)$ 等比(几何)级数：$$\sum_{n=0}^{\infty}q^{n}=\frac{1}{1-q},\:(|q|<1)$$ 当 $|q|\geq1$ 时, 级数发散
	$(2)$ 裂项：$$\sum_{n=1}^{\infty}\frac{1}{(sn-p)(sn+q)}=\frac{1}{s(s-p)},(s=p+q)$$

**定理**: 级数 $$\sum_{n=1}^{\infty}a_n$$ 收敛的必要条件为 $$\lim_{n\to\infty}a_n=0$$

**定理**: 若级数 $\sum_{k=1}^{\infty}a_k$ 和 $\sum_{k=1}^{\infty}b_k$ 都收敛, 则级数 $$\sum_{k=1}^{\infty}(\alpha a_k+\beta b_k)$$ 也收敛, 且 $\sum_{k=1}^{\infty}(\alpha a_k+\beta b_k)=\alpha\sum_{k=1}^{\infty}a_k+\beta\sum_{k=1}^{\infty}b_k$ , 这里 $\alpha$ 和 $\beta$ 为任意实数 .

_便是数列极限的运算法则_

**定理**: 收敛级数 $\sum_{n=0}^{\infty}a_n$ , 将级数的项任意结合但不改变其先后次序, 得到的新级数$$(a_1+\cdots+a_{k_1})+(a_{k_1+1}+\cdots+a_{k_2})+\cdots+(a_{k_{n-1}+1}+\cdots+a_{k_n})+\cdots$$ 即$$\sum_{n=1}^{\infty}(\sum_{m=k_{n-1}+1}^{k_n}a_m)$$ 收敛, 这里 $0=k_0<k_1<k_2<\cdots$ , 且新级数与原级数有相同的和 .

_数列收敛，任意子列收敛于相同值_

上述命题的逆命题自然也是不成立的，但若再加一定条件：

**定理**: 若$$\sum_{n=1}^{\infty}(\sum_{m=k_{n-1}+1}^{k_n}a_m)=(a_1+\cdots+a_{k_1})+(a_{k_1+1}+\cdots+a_{k_2})+\cdots+(a_{k_{n-1}+1}+\cdots+a_{k_n})+\cdots$$ 中每个括号内的项都分别有相同的符号, 则从该级数收敛可推出 $\sum_{n=1}^{\infty}a_n$ 收敛, 且与该级数和相同 .

**定理**: 在级数中去掉或改变有限项不会影响级数的敛散性 .



## 正项级数

若对 $\forall n=1,2,...$ ，都有 $a_n\geq0$ ，则称级数 $\sum_{n=1}^{\infty}a_n$ 为**正项级数** 

**定理**: 正项级数 $\sum_{n=1}^{\infty}a_n$ 收敛的充要条件为其部分和数列 $\{S_n\}$ 有界 .

_单调有界原理_

**比较判别法**: 设有正项级数 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ , 若 $\exists N\in N^*$ , 使得 $n\geq N$ 时有$$a_n\leq b_n$$ 那么: 
	$(1)$ $\sum_{n=1}^{\infty}b_n$ 收敛, 则 $\sum_{n=1}^{\infty}a_n$ 收敛
	$(2)$ $\sum_{n=1}^{\infty}a_n$ 发散, 则 $\sum_{n=1}^{\infty}b_n$ 发散

**比较判别法的极限形式**: 设有正项级数 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ , 若 $$\lim_{n\to\infty}\frac{a_n}{b_n}=l$$ 那么: 
	$(1)$ 若 $0<l<+\infty$ , 则 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ 同敛散
	$(2)$ 若 $l=0$ , 则当 $\sum_{n=1}^{\infty}b_n$ 收敛时, $\sum_{n=1}^{\infty}a_n$ 也收敛
	$(3)$ 若 $l=+\infty$ , 则当 $\sum_{n=1}^{\infty}b_n$ 发散时, $\sum_{n_1}^{\infty}a_n$ 也发散

比较判别法是核心的判别法，理由是其余很多判别法都源于此

**Cauchy积分判别法**: 设当 $x\geq1$ 时, $f(x)$ 非负且递减, 则无穷级数 $\sum_{n=1}^{\infty}f(n)$ 和 $\int_1^{\infty}f(x)\mathrm{dx}$ 同敛散 .

_可以由面积原理得到_

由积分判别法可以得到一类常用参照级数的敛散性判别：

**p-级数**: 级数 $\sum_{n=1}^{\infty}\frac{1}{n^p}$ 收敛当且仅当 $p\geq1$ .
**广义-p级数**: 
	$(i)$级数 $$\sum_{n=2}^{\infty}\frac{1}{n^p(\ln n)^{q}}\begin{cases}\,收敛\quad&,p>1\\\,发散\quad&,p<1\\\,收敛\quad&,p=1且q>1\\\,发散\quad&,p=1且q\leq1\end{cases}$$ $(ii)$级数$$\sum_{n=3}^{\infty}\frac{1}{n^p(\ln n)^q(\ln\ln n)^r}\begin{cases}\,收敛\quad&,p>1\\\,发散\quad&,p<1\\\,收敛\quad&,p=1且q>1\\\,发散\quad&,p=1且q<1\\\,收敛\quad&,p=1且q=1且r>1\\\,发散\quad&,p=1且q=1且r\leq1\end{cases}$$ $\cdots\cdots$


**Cauchy判别法**: 
	设 $\sum_{n=1}^{\infty}a_n$ 为一个正项级数, 
	$(普通形式)$ 
		$(1)$ 若 $\exists\,q<1$ , 使得 $n$ 足够大时便有$$\sqrt[n]{a_n}\leq q<1$$ 则级数收敛
		$(2)$ 若存在无穷多个 $n$ 使得$$\sqrt[n]{a_n}\geq1$$ 则级数发散
	$(极限形式)$
		若 $\forall n\in N$ , $a_n\geq0$ , 且$$\limsup_{n\to{\infty}}\sqrt[n]{a_n}=q$$则:  
		$(1)$ $q<1$ 时, 级数收敛
		$(2)$ $q>1$ 时, 级数发散
		$(3)$ $q=1$ 时, 无法判断

**分式比较判别法**: 有两个正数列 $\{a_n\},\{b_n\}$ , 若 $n\geq n_0$ 时, 有 $$\frac{a_{n+1}}{a_n}\leq\frac{b_{n+1}}{b_n}$$ 则
	$(1)$ 当 $\sum_{n=1}^{\infty}b_n$ 收敛时, $\sum_{n=1}^{\infty}a_n$ 也收敛
	$(2)$ 当 $\sum_{n=1}^{\infty}a_n$ 发散时, $\sum_{n=1}^{\infty}b_n$ 也发散

在分式比较判别法中取 $b_n=q^n\,(0<q<1)$ 可得到 D'Alembert判别法

**D'Alembert判别法**: 设 $a_n>0$
	$(普通形式)$
		$(1)$ 若存在正数 $q<1$ , 使得 $n$ 足够大时有$$\frac{a_{n+1}}{a_n}\leq q$$ 则级数 $\sum_{n=1}^{\infty}a_n$ 收敛
		$(2)$ 若 $n$ 足够大时有$$\frac{a_{n+1}}{a_n}\geq1$$ 则级数 $\sum_{n=1}^{\infty}a_n$ 发散
	$(极限形式)$
		$(1)$ 若 $\limsup_{n\to{\infty}}\frac{a_{n+1}}{a_n}=q<1$ , 则 $\sum_{n=1}^{\infty}a_n<+\infty$
		$(2)$ 若 $\liminf_{n\to\infty}\frac{a_{n+1}}{a_n}=q^{'}>1$ , 则 $\sum_{n=1}^{\infty}a_n=+\infty$
		$(3)$ 若 $q=1$ 或 $q^{'}=1$ , 则结果无法判断

_对于任意的正数列 $\{a_n\}$ , 都有 $$\liminf_{n\to\infty}\frac{a_{n+1}}{a_n}\leq\liminf_{n\to\infty}\sqrt[n]{a_n}\leq\limsup_{n\to\infty}\sqrt[n]{a_n}\leq\limsup_{n\to\infty}\frac{a_{n+1}}{a_n}$$ 这可以说明理论上而言Cauchy判别法要比D'Alembert判别法的应用范围更宽泛_

上面的判别法都是应用了比较判别法，以几何级数为参照得到的

下面以 $p-$级数 乃至 广义 $p-$级数 为参照 还可以得到更多更为精确的判别法

**Raabe判别法**: 设 $a_n>0$
	$(普通形式)$
		$(1)$ 若存在正数 $r>1$ , 使得 $n$ 足够大时有 $$n(\frac{a_n}{a_{n+1}}-1)\geq r$$ 则该级数收敛
		$(2)$ 若 $n$ 足够大时有 $$n(\frac{a_n}{a_{n+1}}-1)\leq1$$ 则该级数发散
	$(极限形式)$ 
		若 $$\lim_{n\to\infty}n(\frac{a_n}{a_{n+1}}-1)=l$$ 即 $$\frac{a_n}{a_{n+1}}=1+\frac{l}{n}+o(\frac{1}{n})\qquad(n\to\infty)$$ 则 $l>1$ 时, 级数收敛; $l<1$ 时, 级数发散

**Gauss判别法**: 设正数列 $\{a_n\}$ 满足条件$$\frac{a_n}{a_{n+1}}=1+\frac{1}{n}+\frac{\beta}{n\ln n}+o(\frac{1}{n\ln n})\qquad(n\to\infty)$$ 那么当 $\beta>1$ 时, 级数 $\sum_{n=1}^{\infty}a_n$ 收敛, $\beta<1$ 时, 级数 $\sum_{n=1}^{\infty}a_n$ 发散, $\beta=1$ 时, 无法判断

诸如Rabbe判别法和Gauss判别法的同类型判别法称作**Bertrand**判别法

可以看到**基于比较判别法**时可以通过类似的方法构造出无数种判别法，而总可以构造出新的判别法的同时，其实另一方面也道出也总需要新的判别方法，就是说不存在一个万能的**作比较的收敛级数**一定可以判别出级数收敛与否，下面的两个定理明确了这一点：

**Du Bois-Reymond定理**: 对于一个给定的收敛正项级数 $\sum_{n=1}^{\infty}a_n$ , 一定存在一个收敛的正项级数 $\sum_{n=1}^{\infty}b_n$ , 使得 $\lim_{n\to\infty}\frac{a_n}{b_n}=0$ 

**Abel定理**: 对于一个给定的发散正项级数 $\sum_{n=1}^{\infty}a_n$ , 一定存在一个发散正项级数 $\sum_{n=1}^{\infty}b_n$ , 使得 $\lim_{n\to\infty}\frac{b_n}{a_n}=0$

下面给出几个另类的判别法：

**Cauchy凝聚判别法**: 设 $\{a_n\}$ 为单调递减的正数列, 则 $\sum_{n=1}^{\infty}a_n$ 收敛的充要条件为: 凝聚项级数$$\sum_{n=0}^{\infty}2^na_{2^n}=a_1+2a_2+4a_4+\cdots+2^na_{2^n}+\cdots$$ 收敛

_# 经常能看见用该方法证明调和级数发散_

**Sapagof判别法**: 设正数数列 $\{a_n\}$ 单调递减, 则 $\lim_{n\to\infty}a_n=0$ 的充要条件为 $\sum_{n=1}^{\infty}(1-\frac{a_{n+1}}{a_n})$ 发散
等价形式: 
	$(1)$ 设 $\{a_n\}$ 为单调递增的正数列, 则该数列与 $\sum_{n=1}^{\infty}(1-\frac{a_n}{a_{n+1}})$ 同敛散
	$(2)$ 若正项级数 $\sum_{n=1}^{\infty}a_n$ 的部分和为 $\{S_n\}$ , 则 $\sum_{n=1}^{\infty}a_n$ 与 $\sum_{n=1}^{\infty}\frac{a_n}{S_n}$ 同敛散

**Kummer判别法**: 
	$(1)$ 正项级数 $\sum_{n=1}^{\infty}a_n$ 收敛的充要条件为存在正数数列 $\{b_n\}$ 和正数 $\delta$ , 使得 $n$ 足够大时有 $$b_n\cdot\frac{a_n}{a_{n+1}}-b_{n+1}\geq\delta>0$$ $(2)$ 正项级数 $\sum_{n=1}^{\infty}a_n$ 发散的充要条件为存在发散的正项级数 $\sum_{n=1}^{\infty}\frac{1}{b_n}$ 使得 $n$ 充足大时$$b_n\cdot\frac{a_n}{a_{n+1}}-b_{n+1}\leq0$$ 

_# Kummer判别法与比较判别法没有直接联系，而是源于部分和数列有上界的充要条件_

## 任意项级数

对于任意项级数 $\sum_{n=1}^{\infty}a_n$ ，即不再要求 $a_n\geq0$ ，$a_n$ 的符号可以任意，可正可负

这时直接对级数的部分和应用Cauchy收敛原理：

**Cauchy收敛原理**: 级数 $\sum_{n=1}^{\infty}a_n$ 收敛的充要条件为 $\forall\,\varepsilon>0$ , $\exists\,N\in N^*$ , 使得 $\forall\,n>N,\forall\,p\in N^*$ , 有 $$|a_{n+1}+\cdots+a_{n+p}|<\varepsilon$$ 
讨论一种特别地任意项级数，**交错级数**，形如 $\sum_{n=1}^{\infty}(-1)^{n-1}a_n$ ，这里 $a_n>0$

**Leibniz判别法**: 如果 $\{a_n\}$ 递减趋于 $0$ , 则交错级数 $\sum_{n=1}^{\infty}(-1)^{n-1}a_n$ 收敛

通过[[Abel恒等式]]可以得到[[Abel不等式]]进而有下面两个判别法：

**Dirichlet判别法**: 设 $\{a_k\},\{b_k\}$ 是两个数列, $S_k=\sum_{i=1}^{k}a_i$ , 若它们满足: 
	$(a)$ $\{b_k\}$ 单减趋于零
	$(b)$ $\{S_k\}$ 有界
则级数 $\sum_{k=1}^{\infty}a_kb_k$ 收敛

**Abel判别法**: 设 $\{a_k\}$ , $\{b_k\}$ 满足下面的条件: 
	$(a)$ $\{b_k\}$ 单调有界
	$(b)$ $\sum_{k=1}^{\infty}a_k$ 收敛
则级数 $\sum_{k=1}^{\infty}a_kb_k$ 收敛

_# 上面一般合称为 **A-D判别法**，出乎意料的是，这两个判别法均是级数收敛的充要条件
即：
若级数 $\sum_{n=1}^{\infty}u_n$ 收敛，
则存在适当的分解 $u_n=a_nb_n$ 使得：
	$(1)$ $\lim_{n\to\infty}b_n=0$ 且 $\sum_{k=1}^na_k$ 有界
也存在适当的分解 $u_n=a_n^{'}b_n^{'}$ 使得：
	$(2)$ $\{b_n\}$ 单调有界 且 $\sum_{n=1}^{\infty}a_n$ 收敛
_

尽管已经给出了一些任意项级数的判别法，但有些时候使用起来并不方便，有些笨重，但反而可以通过更简单的方法判断，如：
_判断：$\sum_{n=1}^{\infty}\frac{\sin nx}{2^n}$ 收敛与否
该级数并不单调，不适合Leibniz判别法，而Dirichlet判别法或是直接使用Cauchy收敛原理可以通过一些技巧性的恒等变形解决，Abel判别法理论上可以解决但并不容易
然而：由于 $|\frac{\sin nx}{2^n}|\\<\frac{1}{2^n}$ ，经过简易放缩再使用Cauchy收敛原理，由于右式对应级数收敛，原结果收敛就是显然的了_

下面引入内容

**定理**: 如果 $\sum_{n=1}^{\infty}|a_n|$ 收敛, 则 $\sum_{n=1}^{\infty}a_n$ 也收敛

**定义**: 
	$(1)$ 若 $\sum_{n=1}^{\infty}|a_n|$ 收敛, 则称 $\sum_{n=1}^{\infty}a_n$ **绝对收敛** (绝对收敛必收敛)
	$(2)$ 若 $\sum_{n=1}^{\infty}a_n$ 收敛, 但 $\sum_{n=1}^{\infty}|a_n|$ 发散, 则称 $\sum_{n=1}^{\infty}a_n$ **条件收敛**

为方便起见，常常有这么两种流行的记法：
记 $a_n^+=\frac{|a_n|+a_n}{2}$ , $a_n^-=\frac{|a_n|-a_n}{2}$ ，它们分别表示级数中正项和负项的绝对大小和 $0$ 组成的数列，相当于把一个数列纵向拆分成了两个数列，但并不分别向前补位，事实上有 $a_n=a_n^+-a_n^-$ 

交换律，结合律对于无限项的情况并不一定成立，但**级数收敛后，结合律便成立**，然而交换律，或是说交换级数内无限项的求和次序却并不一定与原结果相同
当**级数绝对收敛时，交换律再次成立**：

**定理**: 交换绝对收敛级数中无穷多项的次序, 所得的新级数仍然绝对收敛, 其和也不变

另一方面，若级数条件收敛，结论不再成立，但会得到很有趣的结论

**Riemann重排定理**: 若级数 $\sum_{n=1}^{\infty}a_n$ 条件收敛, 则适当交换各项的次序, 可使结果收敛到任一事先指定的实数 $S$ , 或发散至 $\infty$


## 级数乘法

两个有限和相乘 $(\sum_{i=1}^ma_i)(\sum_{j=1}^nb_j)$ 遵循有限运算法则即可
事实上结果为下面矩阵中元素之和：$$\begin{bmatrix}a_1b_1&a_1b_2&\cdots&a_1b_n\\a_2b_1&a_2b_2&\cdots&a_2b_n\\\vdots&\vdots&\ddots&\vdots\\a_mb_1&a_mb_2&\cdots&a_mb_n\end{bmatrix}$$
当相乘的对象变为两个作为无限和的级数时，$(\sum_{i=1}^{\infty}a_i)(\sum_{j=1}^{\infty}b_j)$
旨在它们都收敛时能找到一个简化的积级数 $\sum_{k=1}^{\infty}c_k$ 结果恰为这两个级数结果的乘积
类比成无穷规格矩阵 $$\begin{bmatrix}a_1b_1&a_1b_2&\cdots &a_1b_j&\cdots\\a_2b_1&a_2b_2&\cdots&a_2b_j&\cdots\\\vdots&\vdots&\ddots&\vdots&\cdots\\a_ib_1&a_ib_2&\cdots&a_ib_j&\cdots\\\vdots&\vdots&\ddots&\vdots&\ddots\end{bmatrix}$$ 对于无穷规格的矩阵而言，求和方法不再唯一，涉及到求和顺序的问题，有先前的结论，我们已经知道不同求和顺序会产生不同的结果，在众多求和方法中有两种方法最为常用：
	$(\mathrm I)$ ‘’按方块相加‘’, 即 $$S=\sum_{k=1}^{\infty}(\sum_{\max\{i,j\}=k}a_ib_j)=a_1b_1+(a_1b_2+a_2b_2+a_2b_1)+(a_1b_3+a_2b_3+a_3b_3+a_3b_2+a_3b_1)+\cdots$$
	$(\mathrm{II})$ “按对角线相加”, 即 $$S=\sum_{k=2}^{\infty}(\sum_{i+j=k}a_ib_j)=a_1b_1+(a_1b_2+a_2b_1)+(a_1b_3+a_2b_2+a_3b_1)+\cdots$$
第二种求和方法作为我们讨论的核心，称为**Cauchy乘积**，即 $\sum_{n=1}^{\infty}c_n$ ，这里 $c_n=\sum_{i+j=n+1}^{\infty}a_ib_j$ 
理想情况下，当然希望有 $\sum_{n=1}^{\infty}a_n=A$ , $\sum_{n=1}^{b_n}=B$ , 则 $\sum_{n=1}c_n=AB$ 
但这并不一定成立，例如：级数 $\sum_{n=1}^{\infty}(-1)^{n-1}\frac{1}{\sqrt n}$ 收敛，但它与自身的Cauchy乘积却发散

**定理**: 若级数 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ 都绝对收敛, 其和分别为 $A$ , $B$ , 则将 $a_ib_j$ 按照任意方式遍历 $i,j\in N^*$ 求和得到的结果都是收敛的, 且等于 $AB$

**Mertens定理**: 设级数 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ 都收敛, 其和分别为 $A$ , $B$ , 若其中至少有一个级数绝对收敛, 则它们的Cauchy乘积收敛于 $AB$

**Abel定理**: 设级数 $\sum_{n=1}^{\infty}a_n$ 和 $\sum_{n=1}^{\infty}b_n$ 都收敛, 其和分别为 $A$ , $B$ , 若它们的Cauchy乘积收敛, 则必收敛于 $AB$


# 函数项级数

## 基本内容

**定义**: 在 $[a,b]$ 定义的一列函数 $u_1(x),u_2(x),...,u_n(x),...$ , 称为 $[a,b]$ 上的一个**函数列**, 若取定 $x_0\in[a,b]$ , 得到的数列 $\{u_n(x_0)\}$ 为一个数列, 若其收敛, 则称函数列**在 $x_0$ 处收敛**, 否则称**在 $x_0$ 处发散**, 若 $\{u_n(x)\}$ 在 $[a,b]$ 上任一点处收敛, 则称其在 $[a,b]$ 上**收敛**, 更精确来说称为**逐点收敛**, 函数列在定义域内收敛的点组成的集合称为**收敛点集**, 发散的点组成的集合称为**发散点集**
当函数列 $\{u_n(x)\}$ 在 $E\subset[a,b]$ 上收敛时, 对于 $\forall\,x\in E$ , 记 $u(x)=\lim_{n\to\infty}u_n(x)$ , 则 $u(x)$ 为一个函数, 称为函数列 $\{u_n(x)\}$ 的**极限函数**, 记作 $n\to\infty$ 时, 在 $E$ 上 $u_n\to u$

**定义**: 在 $[a,b]$ 上的一列函数 $u_1(x),u_2(x),...,u_n(x),...$ ,称 $\sum_{n=1}^{\infty}u_n(x)$ 为 $[a,b]$ 上的一个**函数项级数**,
若取定 $x_0\in[a,b]$ , 得到的 $\sum_{n=1}^{\infty}u_n(x_0)$ 为一个数项级数, 若其收敛, 则称函数项级数**在 $x_0$ 处收敛**, 否则称**在 $x_0$ 处发散**, 若 $\sum_{n=1}^{\infty}u_n(x)$ 在 $[a,b]$ 上任一点处收敛, 则称其在 $[a,b]$ 上**收敛**, 更精确来说称为**逐点收敛**, 函数项级数在定义域内收敛的点组成的集合称为**收敛点集**, 发散的点组成的集合称为**发散点集**
当 $\sum_{n=1}^{\infty}u_n(x)$ 在 $E\subset[a,b]$ 上收敛时, 对于 $\forall\,x\in E$ , 记 $S(x)=\sum_{n=1}^{\infty}u_n(x)$ , 则 $S(x)$ 为一个函数, 称为函数项级数的**和函数**

接下来首先要研究的**核心问题**有三：
	$(a)$ 收敛时, 若 $u_n(x)$ $(\forall\,n)$ 连续, 是否有 $u(x)$ 连续?
	$(b)$ 收敛时, 若 $u_n(x)$ $(\forall\,n)$ 可导, 是否有 $u(x)$ 可导? 若可导, 是否相等?
	$(c)$ 收敛时, 若 $u_n(x)$ $(\forall\,n)$ 可积, 是否有 $u(x)$ 可积? 若可积, 是否相等? $(\mathrm{Riemann}可积)$ 

在函数项级数仅仅收敛时，上述**三个问题均有反例**
_经典反例：
	$({\color{red} a})({\color{red} b})$ 取 $u_n(x)=x^n$ , $x\in[0,1]$ , 极限函数为 $$u(x)=\begin{cases}0\quad,x\in[0,1)\\1\quad,x=1\end{cases}$$ $u(x)$ 在 $1$ 处不连续, 进而不可导
	$({\color{red} b})$ 取 $u_n(x)=\frac{\sin nx}{\sqrt n}$ , $x\in[0,1]$ , 显然极限函数为 $u(x)=0$ , 那么 $u^{'}(x)=0$ , 但 $u^{'}_n(x)=\sqrt n\cos nx\nrightarrow0\quad(n\to\infty)$ , 即均可导但结果不相等
	$({\color{red}c})$ 取 $u_n(x)$ , $x\in[0,1]$ , $u_n(x)$ 定义如下: 已知有理数可列, 那么记 $\{Q_n\}$ 逐一列出了 $[0,1]$ 中所有有理数唯一一次, 考虑 $E_n=\{Q_k:k\leq n\}$, 令 $u_n(x)=\chi_{(x\in E_n)}$ , $x\in[0,1]$ 
	则可知 $\int_0^1u_n(x)\mathrm{dx}=0$ , 但 $\lim_{n\to\infty}u_n(x)=D(x)\notin R[0,1]$ , 即极限函数不一定可积	
		\[具体一点: 其实可以写出 $u_n(x)=\lim_{m\to\infty}(\cos n!\pi x)^{2m}$\]
	$({\color{red}c})$ 取 $u_n(x)=-2nxe^{-nx^2}$ , $x\in[0,1]$ , 则极限函数 $u(x)=0$ , 那么 $\int_0^1u(x)\mathrm{dx}=0$ , 但 $\int_0^1u_n(x)\mathrm{dx}=(e^{-nx^2})|_0^1=e^{-n}-1\nrightarrow0\quad(n\to\infty)$ , 即均可积但结果不相等 
_

_# 极限运算对连续函数类，可导函数类，可积函数类均不封闭_


## 一致收敛

### 函数族
函数列更一般的讲，可以说是一个二元函数，或是一个含参变量的函数
关于 $x\in X$ 的函数列通项 $f_n(x)$ 实际上可以看成一个定义在 $X\times N$ 上的二元函数
下面不专门研究以正整数为参变量的函数列，不妨先讨论一下更为一般的以任意集合为参变量取值的函数族的性质

**定义**: 如果两个变量 $x,t$ 的函数 $(x,t)\mapsto F(x,t)$ 定义于集合 $X\times T$ , 并且可以将变量 $t\in T$ 分离出来并成为**参数**或**参变量**, 则上述函数称为**依赖于参数 $t$ 的函数族**, 这时, 集合 $T$ 称为**参数集**或**参数域**, 函数族本身常记作 $f_t(x)$ 或 $\{f_t,t\in T\}$ 的形式

**定义**: 设 $\{f_t:X\to\mathbb R,t\in T\}$ 是依赖于参数 $t$ 的函数族, $\mathfrak B$ 是参数集 $T$ 中的基. 如果 $\lim_{\mathfrak B}f_t(x)$ 对于固定值 $x$ 存在, 我们就说该函数族**在点 $x$ 收敛**, 全部收敛点的集合称为该函数族在**给定基 $\mathfrak B$ 上的收敛集**. 若函数族在集合 $E\subset X$ 的每一点 $x$ 在基 $\mathfrak B$ 上收敛, 就说该函数族**在集合 $E$ 和基 $\mathfrak B$ 上收敛**, 将定义在 $E$ 上的函数 $f(x):=\lim_{\mathfrak B}f_t(x)$ 称为函数族 $f_t$ **在集合 $E$ 和基 $\mathfrak B$ 上的极限函数**或**极限**

**定义**: 函数 $f_t:X\to\mathbb R$ 构成函数族 $\{f_t,t\in T\}$ , $\mathfrak B$ 为 $T$ 中的基, 若 $\lim_{\mathfrak B}f_t(x)=f(c)$ $(\forall\,x\in E\subset X)$ , 则称该函数族在集合 $E$ 和 基 $\mathfrak B$ 上**逐点收敛到 $f:E\to\mathbb R$ $**, 常记为在 $E$ 上 $$f_t\to_{\mathfrak B}f$$ 
**定义**: 函数 $f_t:X\to\mathbb R$ 构成函数族 $\{f_t,t\in T\}$ , $\mathfrak B$ 为 $T$ 中的基, 若 $\forall\,\varepsilon>0$ , $\exists\,B\in\mathfrak B$ , $s.t.$ $\forall\,t\in B$ , $x\in E$ , 有 $|f(x)-f_t(x)|<\varepsilon$ , 就称函数族在集合 $E$ 和基 $\mathfrak B$ 上**一致收敛到函数 $f:E\to\mathbb R$** , 常记为在 $E$ 上$$f_t\rightrightarrows_{\mathfrak B}f$$ 
用 $\Delta_t(x)=|f(x)-f_t(x)|$ 用于度量 $f_t$ 与 $f$ 间的偏差, 用 $\Delta_t=\sup_{x\in E}\Delta_t(x)$ 记在 $E$ 内两者的最大偏差(如果存在的话), 那么有 $\Delta_t(x)\leq\Delta_t$ $(\forall\,x\in E)$ $$\begin{align}在\,E上\,f_t\to_{\mathfrak B}f&\iff在 \mathfrak B上\Delta_t(x)\to0\\在\,E上\,f_t\rightrightarrows_{\mathfrak B}f&\iff在\mathfrak B上\Delta_t\to0\end{align}$$ 
 **Cauchy收敛准则**: 设函数族 $\{f_t:X\to\mathbb R,t\in T\}$ , $T$ 有一个基 $\mathfrak B$ , 则该函数族在集合 $E\subset X$ 和基 $\mathfrak B$ 上一致收敛的充要条件为: $\forall\,\varepsilon>0$ , $\exists\,B\in\mathfrak B$ , $s.t.$ $\forall\,t_1,t_2\in B$ , $x\in E$ , 有 $|f_{t_1}(x)-f_{t_2}(x)|<\varepsilon$ 

_# 上面的定义都是基于实值函数，在任意度量空间中有着完全类似地定义，将 $X\to\mathbb R$ 换为 $X\to Y$ 这里 $Y$ 为度量空间，那么将 $|f_{t_1}(x)-f_{t_2}(x)|$ 改为 $d_Y(f_{t_1}(x),f_{t_2}(x))$ 即可，这里 $d_Y$ 为 $Y$ 中的度量
同样，Cauchy收敛原理也是成立的，只要 $Y$ 是完备的度量空间_

### 函数项级数

**定义**: 设 $\{a_{n}:X\to \mathbb{C},n\in \mathbb{N}\}$ 为复值函数序列, 如果序列(**部分和**) $S_{m}(x)=\{\sum_{n=1}^ma_{n}(x),m\in \mathbb{N}\}$ 在集合 $E \subset X$ 上收敛或是一致收敛, 则称级数 $\sum_{n=1}^\infty a_{n}(x)$ 在集合 $E$ 上**收敛**或是**一致收敛**

显然的，函数项级数收敛问题本质上也是函数列收敛的问题
那么类似的有

 **Cauchy收敛准则**: 函数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ 在集合 $E\subset X$ 和基 $\mathfrak B$ 上一致收敛的充要条件为: $\forall\,\varepsilon>0$ , $\exists\,N\in\mathbb N$ , $s.t.$ $\forall\,m\geq n>N$ , $x\in E$ , 有 $|a_n(x)+\cdots+a_m(x)|<\varepsilon$

**定理**: 函数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ 在 $E$ 上一致收敛的必要条件是在 $E$ 上 $a_n(x)\rightrightarrows0$ 

**定义**: 若对 $\forall\,x\in E$ , 数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ 绝对收敛, 则称函数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ 在 $E$ 上**绝对收敛**

**命题**: 若有级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ , $\sum\limits_{n=1}^{\infty}b_n(x)$ , 只要 $n$ 足够大时在 $E$ 上有 $|a_n(x)|\leq b_n(x)$ , 则 $$\sum\limits_{n=1}^{\infty}b_n(x)一致收敛\implies\sum\limits_{n=1}^{\infty}a_n(x)绝对收敛且一致收敛$$ 
**Weierstrass强函数检验法**: 对于级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ , 若存在收敛数项级数 $\sum\limits_{n=1}^{\infty}M_n$ , 使得 $n$ 足够大时$$\sup_{x\in E}|a_n(x)|\leq M_n$$成立, 则级数 $\sum\limits_{n=1}^{\infty}a_n(x)$ 在 $E$ 上绝对收敛且一致收敛, 这里 $\sum\limits_{n=1}^{\infty}M_n$ 称为一个 $\sum\limits_{n=1}^{\infty}$ 的**优级数**

作为应用，讨论一下有关幂级数的内容

**定义**: 形如$$\sum\limits_{n=0}^{\infty}a_n(x-x_0)^n=a_0+a_1(x-x_0)+\cdots+a_n(x-x_0)^n+\cdots$$的函数项级数称为**幂级数**

**命题**: 若幂级数 $\sum\limits_{n=0}^{\infty}c_n(z-z_0)^n$ 在点 $\zeta\neq z_0$ 处收敛, 则它在任何一个圆 $K_q=\{z\in\mathbb{C}||z-z_0|<q|\zeta-z_0|\}\,(0<q<1)$ 内绝对收敛且一致收敛
**[证明]**:
	由于 $|c_n(z-z_0)^n|=|c_n|\frac{|(z-z_0)^n|}{|(z_0-\zeta)^{n}|}|(z_0-\zeta)^{n}|<|c_n||q|^n|z_0-\zeta|^n<q^n\,(因为c_n(\zeta-z_0)^n\to0,故n充分大时|c_n(\zeta-z_0)^n|<1)$由于级数 $\sum\limits_{n=1}^{\infty}q^n$ 收敛, 故原级数绝对收敛且一致收敛

利用**Weierstrass判别法**只能判别即 $\sum\limits_{n=1}^{\infty}a_n(x)$ 绝对收敛又有 $\sum\limits_{n=1}^{\infty}|a_n(x)|$ 一致收敛的级数，但实际上存在一致收敛但不绝对收敛的级数；或是绝对收敛且一致收敛但 $\sum\limits_{n=1}^{\infty}|a_n(x)|$ 并不一致收敛的级数
于是需要更强的判别法

数项级数中的**A-D判别法**在函数项级数中有完全类似的命题，在此之前我们需要定义：

**定义**: 若 $E$ 上的函数列 $\{f_n(x)\}$ 满足 $\forall\,x\in E$ , $\exists\,M(x)>0$ , $s.t.\,|f_n(x)|\leq M(x)$ 对 $\forall\,n\in\mathbb{N}$ 成立, 则称 $\{f_n(x)\}$ 在 $E$ 上**逐点有界**; 若 $\exists\,M>0$ , $s.t.\forall\,n\in\mathbb{N}$ 都有 $|f_{n}(x)|\leq M$ 成立则称 $\{f_n(x)\}$ 在 $E$ 上**一致有界**

_例：
	$f_n(x)=x^n$ 在 $(0,1)$ 上一致有界, $f_n(x)=nx^n$ 在 $(0,1)$ 上逐点有界但不一致有界
_

**Dirichlet判别法**: $E$ 上的函数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)b_n(x)$ , 记 $S_n(x)=\sum\limits_{k=1}^na_k(x)$ 若满足: 
	$(a)$ $b_n(x)\rightrightarrows0$ , $n\to\infty$ , 且对于固定的 $x\in E$ , $\{b_n(x)\}$ 是单调的
	$(b)$ $S_n(x)$ 在 $E$ 上一致有界
则原级数在 $E$ 上一致收敛

**Abel判别法**: $E$ 上的函数项级数 $\sum\limits_{n=1}^{\infty}a_n(x)b_n(x)$ , 若满足: 
	$(a)$ $\{b_n(x)\}$ 对于固定的 $x\in E$ 单调, 且其一致有界
	$(b)$ $\sum\limits_{n=1}^{\infty}a_n(x)$ 一致收敛
则原级数在 $E$ 上一致收敛

_关于 **A-D判别法**，它们本质上是对同一表达式两部分通过不同的方式分别控制得到的，意思是：
$$\begin{align}\bigg|\sum\limits_{n=N}^{N+p}a_n(x)b_n(x)\bigg|&=\bigg|b_{N+p}(x)\sum\limits_{n=N}^{N+p}a_n(x)-\sum\limits_{n=N}^{N+p-1}\bigg(\sum\limits_{k=N}^{n}a_k(x)\bigg)(b_n(x)-b_{n+1}(x))\bigg|\\&\leq\bigg|b_{N+p}(x)\sum\limits_{n=N}^{N+p}a_n(x)\bigg|+\sum\limits_{n=N}^{N+p-1}\bigg|\sum\limits_{k=N}^{n}a_k(x)\bigg||b_n(x)-b_{n+1}(x)|\\&=\begin{cases}\underbrace{\color{red}|b_{N+p}(x)|}_{\color{red}无穷小量}\underbrace{\color{blue}|\sum\limits_{n=N}^{N+p}a_n(x)|}_{\color{blue}有界量}+\underbrace{\color{red}\sum\limits_{n=N}^{N+p-1}|b_n(x)-b_{n+1}(x)|}_{\color{red}无穷小量}\underbrace{\color{blue}\bigg|\sum\limits_{k=N}^{n}a_k(x)\bigg|}_{\color{blue}有界量},\qquad(\mathrm{Dirichlet判别})\\\\\\\underbrace{\color{red}|b_{N+p}(x)|}_{\color{red}有界量}\underbrace{\color{blue}|\sum\limits_{n=N}^{N+p}a_n(x)|}_{\color{blue}无穷小量}+\underbrace{\color{blue}\sum\limits_{n=N}^{N+p-1}\bigg|\sum\limits_{k=N}^{n}a_k(x)\bigg|}_{\color{blue}无穷小量}\underbrace{\color{red}|b_n(x)-b_{n+1}(x)|}_{\color{red}有界量},\qquad(\mathrm{Abel判别})\end{cases}\end{align}$$
_

还有一些与判断函数项级数一致收敛与否的常见结论

$1^\circ$ 数项级数控制上下界
**命题**: 区间 $[a,b]$ 上的单调函数 $u_n(x)$ , $(\forall\,n)$ , 如果级数 $\sum\limits_{n=1}^{\infty}u_n(a)$ 和 $\sum\limits_{n=1}^{\infty}u_n(b)$ 都绝对收敛, 则: 
级数 $\sum\limits_{n=1}^{\infty}u_n(x)$ 在 $[a,b]$ 上绝对且一致收敛
**[证明]**:
	$u_{n}(x)$ 在 $[a,b]$ 上单调, 即一定有 $|u_{n}(x)|\leq\max\{|u_{n}(a)|,|u_{n}(b)|\}$ , 故由比较审敛法, 可知无论如何都有 $\sum\limits_{n=1}^{\infty}u_{n}(x)$ 绝对收敛

$2^\circ$ 连续函数受开边界性质影响
**命题**: $\{u_n(x)\}$ 为 $[a,b]$ 上的连续函数列, 若 $\sum\limits_{n=1}^{\infty}u_n(x)$ 在 $[a,b)$ 内的每一点收敛, 但 $\sum\limits_{n=1}^{\infty}u_n(b)$ 发散, 则 $\sum\limits_{n=1}^{\infty}u_n(x)$ 在 $[a,b)$ 上不一致收敛
**[证明]**:
	若 $\sum\limits_{n=1}^{\infty}u_{n}(x)$ 在 $[a,b)$ 上一致收敛, 则 $\forall\,\varepsilon>0$ , $\exists\,N\in\mathbb{N}^{*}$ , 使得 $n>N$ , $\forall\,p\in\mathbb{N}$ , $\forall\,x\in[a,b)$ 时, 有 $$\bigg|\sum\limits_{m=n+1}^{n+p}u_{m}(x)\bigg|<\varepsilon$$由于 

$3^\circ$ 点态推一致，局部推整体（有限覆盖）
**命题**: 设 $[a,b]$ 为有限闭区间, 若 $\forall\,x\in[a,b]$ , 存在包含 $x$ 的开区间 $I_x$ , 使得 $\{f_n\}$ 在 $I_x$ 上一致收敛于 $f$ , 则 $\{f_n\}$ 在 $[a,b]$ 上一致收敛于 $f$

$4^\circ$ 受导函数控制
**命题(Bendixon判别法)**: 设 $\sum\limits_{n=1}^{\infty}u_n(x)$ 为 $[a,b]$ 上的可微函数项级数, 且 $\sum\limits_{n=1}^{\infty}u_n^{'}(x)$ 的部分和数列一致有界, 若 $\sum\limits_{n=1}^{\infty}u_n(x)$ 在 $[a,b]$ 上收敛, 则 $\sum\limits_{n=1}^{\infty}u_n(x)$ 在 $[a,b]$ 上一致收敛

可以通过**A-D判别法**证明一个关于幂级数的结论

**Abel第二定理**: 若幂级数 $\sum\limits_{n=0}^{\infty}c_n(z-z_0)^n$ 在某点 $\zeta\in\mathbb{C}$ 收敛, 则它在以 $z_0,\zeta$ 为端点的闭区间上一致收敛
**[证明]**:
	在以 $z_0,\zeta$ 为端点的闭区间上的点 $z$ 可以表示为 $z=z_0+(\zeta-z_0)t$ , $t\in[0,1]$
	因此 $\sum\limits_{n=0}^{\infty}c_n(z-z_0)^n=\sum\limits_{n=0}^{\infty}c_n(\zeta-z_0)^nt^n$ 由于: 
	$\sum\limits_{n=0}^{\infty}c_n(\zeta-z_0)^n$ (一致)收敛, 且有 $t^n$ 在 $t\in[0,1]$ 上一致有界且关于每个 $t$ 都单调递减
	由 $\rm{Abel}$ 判别法即知原级数在区间上一致收敛

## 极限交换

为了研究函数项级数的连续，可微，可积性，由于它们本质上都是极限过程，直觉上讲交换求和与极限次序结果是一样的，但这里的求和是无限和，故交换求和与极限就成为了交换极限与极限的问题，故我们研究更宽泛的极限交换的问题，即这些问题的通性

### 两个极限运算可交换的条件

**定理**: 设 $\{F_{t},t\in T\}$ 为依赖于参数 $t$ 的函数 $F_t:X\to\mathbb{C}$ 构成的函数族, $\mathfrak B_X$ 为 $X$ 中的基, $\mathfrak B_T$ 为 $T$ 中的基, 如果函数族在 $X$ 和基 $\mathfrak B_T$ 上一致收敛到函数 $F:X\to\mathbb{C}$ , 而极限 $\lim_\limits{\mathfrak B_{X}}F_t(x)=A_t$ 对于所有的 $t\in T$ 都存在, 则一定有累次极限 $\lim_\limits{\mathfrak B_X}(\lim_\limits{\mathfrak B_T}F_t(x))$ 和 $\lim_\limits{\mathfrak B_T}(\lim_\limits{\mathfrak B_X}F_t(x))$ 都存在, 且 $$\lim_\limits{\mathfrak B_X}(\lim_\limits{\mathfrak B_T}F_t(x))=\lim_\limits{\mathfrak B_T}(\lim_\limits{\mathfrak B_X}F_t(x))$$该结果可以用下面的图表示: $$\begin{align}&{\color{red}F_t(x)\:\overrightarrow{\underset{\mathfrak B_T}{\longrightarrow}}}\:F(x)\\&{\color{red}\small{\mathfrak B_X}\bigg\downarrow}\qquad\quad{\color{blue}\exists\bigg\downarrow{\small{\mathfrak B_X}}}\\&\quad A_t\:\:\:{\color{blue}\xrightarrow[\mathfrak B_T]{\exists}\:\:\: A}\end{align}$$左上红色是定理条件, 右下蓝色是可得到的结论

该定理的证明用到了分析手法中十分常见的**三分法**
**[证明]**: 
	已知 $F_t(x)\underset{\mathfrak B_T}{\rightrightarrows} F(x)$ ,
		故 $\forall\,\varepsilon>0$ , $\exists\,B_T\in\mathfrak B_T$ , $s.t.$ $\forall\,t_{1},t_{2}\in B_T$ , 有 $|F_{t_1}(x)-F_{t_2}(x)|<\frac{\varepsilon}{3}$
	已知 $\forall\,t\in T,F_t(x)\underset{\mathfrak B_X}{\to}A_t$ , 
		故 $\forall\,\varepsilon>0$ , $\exists\,B_X(t)\in\mathfrak B_X$ , $s.t.\,\forall\,x\in B_X(t)$ , 有 $|F_t(x)-A_t|<\frac{\varepsilon}{3}$ 
	综合上面的条件
	因此 $\forall\,t_1,t_2\in B_T$ , $\exists\,B_X(t_1),B_X(t_2)\in\mathfrak B_X$ , 使得: 
	$|F_{t_1}(x)-A_{t_1}|<\frac{\varepsilon}{3}$ , $|F_{t_2}(x)-A_{t_2}|<\frac{\varepsilon}{3}$ 对 $\forall\,x\in B_X(t_1)\cap B_X(t_2)\triangleq B_X(t)\in\mathfrak B_X$ 成立
	那么 $$|A_{t_1}-A_{t_2}|\leq|F_{t_1}(x)-A_{t_1}|+|F_{t_1}(x)-F_{t_2}(x)|+|F_{t_2}-A_{t_2}|<\frac{\varepsilon}{3}+\frac{\varepsilon}{3}+\frac{\varepsilon}{3}=\varepsilon$$故可知关于 $t$ 的函数 $A_t$ 在 $\mathfrak B_T$ 上收敛, 不妨设收敛于 $A$
	下证 $F(x)\underset{\mathfrak B_X}{\to}A$ , 
	取定 $t_2$ 不变, 则 $\exists B_X\in \mathfrak B_X$ , $s.t.$ $\forall\,x\in B_X$ , 有 $|F_{t_2}(x)-A_{t_2}|<\frac{\varepsilon}{3}$ 成立, 
	另一方面, 在式 $|F_{t_1}(x)-F_{t_2}(x)|<\varepsilon$ 及式 $|A_{t_1}-A_{t_{2}}|\leq\varepsilon$ 中, 令 $t_1$ 在 $B_T$ 上取极限, 则得到 $|F(x)-F_{t_2}(x)|<\frac{\varepsilon}{3}$ , $|A-A_{t_2}|\leq\varepsilon$
	因此 $$|F(x)-A|\leq|F(x)-F_{t_2}(x)|+|F_{t_2}(x)-A_{t_2}|+|A_{t_2}-A|<\frac{5\varepsilon}{3}$$由此可说明 $\lim_\limits{\mathfrak B_X}F(x)=A$

**推论**: 若 $\{f_{t},t\in T\}$ 为依赖于参数 $t$ 的函数 $f_t:X\to\mathbb{C}$ 构成的函数族, $\mathfrak B$ 为 $T$ 中的基, 如果在 $X$ 和基 $\mathfrak B$ 上有 $f_t\rightrightarrows f$ , 且 $f_t$ 在 $x_0$ 处连续, 则函数 $f:X\to\mathbb{C}$ 上连续也在该点连续
**[证明]**:
	证明就是上面定理的直接推论, 
	$f_t$ 在 $x_0$ 处连续满足了向下的箭头, $f_t$ 在 $\mathfrak B$ 上 $f_t\rightrightarrows f$ 满足了向右的箭头, 故有 $$\lim_\limits{x\to x_0}\lim_\limits{\mathfrak B}f_t(x)=\lim_\limits{\mathfrak B}\lim_\limits{x\to x_0}f_t(x)$$这就证明极限函数在 $x_0$ 处连续, 且值就是交换极限的结果

**推论**: 如果一个集合上的连续函数序列在该集合上一致收敛, 则极限函数也在该集合上连续

**推论**: 如果一个集合上由连续函数组成的级数在该集合上一致收敛, 则和函数也在该集合上连续

之前我们证明过一个有关幂级数的结论，Abel第二定理
现在可以知道 $\sum\limits_{n=0}^{\infty}c_n(z-z_0)^n$ 在 $\zeta$ 处收敛，则在 $[z_0,\zeta]$ 上和函数存在且连续
特别地，取 $z_0=0$ ，$\zeta=1$ ，由此可以得到如果 $\sum\limits_{n=0}^{\infty}c_n$ 收敛，则 $\sum\limits_{n=0}^{\infty}c_nz^n$ 在 $1$ 处右连续

总之上面我们看到了，一致极限运算可以充分保持收敛函数列的连续性，但是否也是必要的呢？
某些情形下，如果连续函数列收敛到连续函数，反过来也可以推出该收敛过程为一致收敛

**Dini定理**: 如果紧集上的连续函数序列在该紧集上单调收敛于连续函数, 则该序列一致收敛
**[证明]**:
	设紧集 $E$ 上的连续函数列 $\{f_n:n\in\mathbb{N}\}$ 收敛于 $E$ 上的连续函数 $f$
	且对于 $\forall\,x\in E$ , 数列 $\{f_n(x)\}$ 单调, 不妨设为单调递减
	由于 $f_n-f$ **递减收敛于 $0$**  , 故 $\forall\,y\in E$ , $\forall\,\varepsilon>0$ , $\exists\,N(y,\varepsilon)\in\mathbb{N}$ , 使得 $n>N(\varepsilon,y)$ 时, 有 $0<f_n(y)-f(y)<f_{N(y,\varepsilon)}(y)-f(y)<\frac{\varepsilon}{3}$
	另一方面, 由于$f$ **连续**, 故 $\exists\,\delta(\varepsilon)>0$ , $s.t.$ $|x-y|<\delta(\varepsilon)$ , 就有 $|f(x)-f(y)|<\frac{\varepsilon}{3}$ , 
	然后, 由于 $f_n$ **连续**, 故 $\exists\,\delta(\varepsilon,n)>0$ , $s.t.$ $|x-y|<\delta(\varepsilon,n)$ , 就有 $|f_n(x)-f_n(y)|<\frac{\varepsilon}{3}$ ,
	于是, 只要 $n>N(y,\varepsilon)$ , $\forall\,x$ , 只要满足 $|x-y|<\min\{\delta(\varepsilon),\delta(\varepsilon,n)\}$ , 即 $x\in B(y,\delta(y)):=B(y,\min\{\delta(\varepsilon),\delta(\varepsilon,n)\})$ 时, 就有 $$|f_n(x)-f(x)|\leq|f_n(x)-f_n(y)|+|f_n(y)-f(y)|+|f(y)-f(x)|<\varepsilon$$


