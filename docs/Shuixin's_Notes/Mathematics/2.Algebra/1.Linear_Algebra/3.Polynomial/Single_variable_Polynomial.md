
# 一元多项式环

**定义**: 域 $\mathbf F$ 上的一元多项式形如$$f(x)=a_nx^n+a_{n-1}x^{n-1}+\cdots+a_1x+a_0$$这里 $a_k\in\mathbf F$ , 称为**系数**, 而 $x$ 只是代表一个符号, 不在 $\mathbf F$ 中, 称为**不定元**, 将 $f(x)$ 称作一个域上的**多项式**(或**多项式形式**), $n$ 为非负整数, 若 $a_n\neq0$ , 则将 $n$ 称为多项式 $f(x)$ 的次数, 记为 $\deg f(x)$ , $a_nx^n$ 称作**首项**, $a_0$ 为**常数项**, $a_ix^i$ 为一项 .
$\forall\,a\in\mathbf F^*$ , 将 $a$ 看作 $\mathbf F$ 上的 $0$ 次多项式 .  $0\in\mathbf F$ 视为 $\mathbf F$ 上的多项式, 称为**零多项式**, 次数规定为 $-\infty$ .

_两个多项式 $f(x)=\sum_{k=0}^na_kx^k,g(x)=\sum_{k=0}^mb_kx^k$ 相等当且仅当 $m=n$ 且 $a_k=b_k\,(\forall\,k)$_ 

将域 $\mathbf F$ 上的所有关于不定元 $x$ 的多项式的集合记为 $\mathbf F[x]$ , 在 $\mathbf F[x]$ 上可定义加法和乘法： $$\begin{align}\sum_{k=0}^na_kx^k+\sum_{k=0}^mb_kx^k&:=\sum_{k=0}^{n}(a_k+b_k)x^k\qquad (n\geq m)\\(\sum_{k=0}^na_kx^k)\cdot(\sum_{k=0}^mb_kx^k):=&\sum_{k=0}^{m+n}(\sum_{i+j=k}a_ib_j)x^k\end{align}$$( $k>n$ 时, $a_k=0$ ; $k>m$ 时, $b_k=0$ ) 
之后 $f(x)\cdot g(x)$ 简记为 $f(x)g(x)$

**关于多项式次数的性质**: 若 $f(x),g(x)\in\mathbf F[x]$ , 则$$\begin{align}\deg(f(x)\pm g(x))&\leq\max\{\deg f(x),\deg g(x)\}\\\deg(f(x)g(x))&=\deg f(x)+\deg g(x)\end{align}$$

可以证明， $(\mathbf F[x],+)$ 为交换群，零元为 $0$ ， $(\mathbf F[x],\cdot)$ 为交换群，幺元为 $1$ ，于是 $(\mathbf F[x];+,\cdot)$ 为域 $\mathbf F$ 上的交换环，且无平凡零因子，于是 $\mathbf F[x]$ 为含幺无零因子环，即**整环** .

**定义**: 若 $R$ 为整环, 幺元为 $1^{'}$ , 若 $R$ 有子环 $R_1$ , 满足: 
	$1^\circ$ $1^{'}\in R_1$
	$2^\circ$ 域 $\mathbf F$ 与 $R_1$ 间有一个保持加法和乘法的双射 $\tau$
则称 $R$ 可看成 $R_1$ 的**扩环** .

**定理**: 域 $\mathbf F$ , 整环 $R$ , $R$ 可看作 $\mathbf F$ 的扩环, $\mathbf F$ 到 $R$ 的子环 $R_1$ 间保加法和乘法的双射为 $\tau$ , 若 $\forall\,t\in R$ , 定义: $$\begin{align}\sigma_t:\mathbf F[x]&\longrightarrow R\\f(x)=\sum_{i=0}^{n}a_ix^i&\longmapsto\sum_{i=0}^{n}\tau(a_i)t^i\triangleq f(t)\end{align}$$ 则 $\sigma_t$ 为一个保持加法和乘法的映射, 即若有$$f(x)+g(x)=h(x),\qquad f(x)g(x)=p(x)$$ 则$$\begin{align}h(t)=\sigma_t(h(x))=\sigma_t(f(x)+g(x))&=\sigma_t(f(x))+\sigma_t(g(x))=f(t)+g(t)\\p(t)=\sigma_t(p(x))=\sigma_t(f(x)g(x))&=\sigma_t(f(x))\sigma_t(g(x))=f(t)g(t)\end{align}$$ 由于特别地, 有 $\sigma_t(x)=t$ , 故将映射 $\sigma_t$ 称为 **$x$ 用 $t$ 代入** .

_#关于 $t$ 代入 $f(x)g(x)=p(x)$ 并不需要 $R$ 为交换环，而只需 $t$ 与 $R_1$ 中的元素可交换即可_

# 整除与带余除法

## 整除

类似于整数环，对于多项式环，可以定义二元关系：

**定义**: 设 $f(x),g(x)\in\mathbf F[x]$ , 若存在 $h(x)\in\mathbf F[x]$ , 使得 $f(x)=h(x)g(x)$ , 那么就称 $g(x)$ **整除** $f(x)$ , 记作 $g(x)|f(x)$ , 否则称 $g(x)$ 不能整除 $f(x)$ , 记作 $g(x)\nmid f(x)$ .
当 $g(x)|f(x)$ , 称 $g(x)$ 为 $f(x)$ 的一个**因式**, $f(x)$ 为 $g(x)$ 的一个**倍式 .

**性质**: 
	$1^\circ$ $0|f(x)$ $\iff$ $f(x)=0$
	$2^\circ$ $f(x)|0$  $(\forall\,f(x)\in\mathbf F[x])$ 
	$3^\circ$ $b|f(x)$  $(\forall\,b\in\mathbf F^*\,,\forall\,f(x)\in\mathbf F[x])$ 

整除关系为具有反身性和传递性的二元关系，但并不满足对称性，故不为等价关系
但却可就此定义一个等价关系：

**定义**: 在 $\mathbf F[x]$ 中, 若 $g(x)|f(x)$ 且 $f(x)|g(x)$ , 则称 $f(x)$ 与 $g(x)$ **相伴**, 记作 $f(x)\sim g(x)$ .

相伴关系为 $\mathbf F[x]$ 上的等价关系

**命题**: 在 $\mathbf F[x]$ 中, $f(x)\sim g(x)$ 当且仅当存在 $c\in\mathbf F^*$ 使得 $f(x)=cg(x)$ 

**命题**: 在 $\mathbf F[x]$ 中, 若 $g(x)|f_i(x)\:(i=1,2,...,s)$ , 则对于 $\forall\,u_i(x)\in\mathbf F[x]\:(i=1,2,...,s)$ , 有$$g(x)|(u_1(x)f_1(x)+u_2(x)f_2(x)+\cdots+u_s(x)f_s(x))$$ 
## 带余除法

**定理(带余除法)**: 设 $f(x),g(x)\in\mathbf F[x]$ , 且 $g(x)\neq0$ , 则存在**唯一**的 $h(x),r(x)\in\mathbf F[x]$ , 使得$$f(x)=h(x)g(x)+r(x)\qquad\qquad\deg\,r(x)<\deg\,g(x)$$ $f(x)$ 称作**被除式**, $g(x)$ 称作**除式**, $h(x)$ 称作**商式**, $r(x)$ 称作**余式**, 上式称为**除法算式** .

**推论**: 若 $f(x)$ 关于 $g(x)$ 作带余除法得到的式子为 $f(x)=h(x)g(x)+r(x)$ , 则$$g(x)|f(x)\iff r(x)=0$$ 
通过该推论可以证明，整除关系不随域的扩大而改变，即：若 $\mathbf K\subseteq\mathbf F$ ，则在 $\mathbf F[x]$ 中，$g(x)|f(x)$ 当且仅当在 $\mathbf K[x]$ 中，$g(x)|f(x)$ 。

_多项式的**综合除法**: 
	已知 $f(x)=\sum_{k=0}^{n}a_kx^k,g(x)=\sum_{k=0}^{m}b_kx^k\in\mathbf F[x]$ , 且 $\deg\,f(x)\geq\deg\,g(x)$ , $g(x)\neq0$ 
	试求除法算式 $f(x)=h(x)g(x)+r(x)$ 中的 $h(x),r(x)$
	做如下操作: $$\begin{align}\\\,{\color{blue}b_mx^m\:+\:b_{m-1}x^{m-1}\:+\:\cdots\:b_1x\:+\:b_0})\overline{\,a_nx^n\:+\:a_{n-1}x^{n-1}\:+\:\cdots\:a_1x\:+\:a_0}\end{align}$$ $(i)$ 取单项式 $\frac{a_n}{b_m}x^{n-m}$ 置于头部, 与除式相乘后左对齐写于次行, 右侧两行再做减法, 最高次项相消, 得到新被除式$$\begin{align}&{\color{red}\frac{a_n}{b_m}x^{n-m}}\\\,{\color{blue}b_mx^m\:+\:b_{m-1}x^{m-1}\:+\:\cdots\:b_1x\:+\:b_0})&\overline{\,a_nx^n\:+\:a_{n-1}x^{n-1}\:+\:\cdots\:a_1x\:+\:a_0}\\&{\color{purple}a_nx^n}+{\color{red}\frac{a_n}{b_m}x^{n-m}}{\color{blue}b_{m-1}x^{m-1}}+\cdots\\&\overline{0\:+\:(a_{n-1}-{\color{red}\frac{a_n{\color{blue}b_{m-1}}}{b_m}}){\color{purple}x^{n-1}}+\cdots}\end{align}$$ $(ii)$ 若新被除式 $(a_{n-1}-{\color{red}\frac{a_n{\color{blue}b_{m-1}}}{b_m}}){\color{purple}x^{n-1}}+\cdots$ 首项为 $0$ 则考虑最高次的不为零项, 下面不妨设最高次项不为零, 记 $c_m=a_n,c_{m-1}=a_{n-1}-\frac{c_mb_{m-1}}{b_m}$ , 则取单项式 $\frac{c_{m-1}}{b_m}x^{n-m-1}$ , 类似地, 置于头部, 做和之前的相同操作, 得到下一行$$\begin{align}&{\color{red}\frac{a_n}{b_m}x^{n-m}+\frac{c_{m-1}}{b_m}x^{n-m-1}}\\\,{\color{blue}b_mx^m\:+\:b_{m-1}x^{m-1}\:+\:\cdots\:b_1x\:+\:b_0})&\overline{\,a_nx^n\:+\:a_{n-1}x^{n-1}\:+\:\cdots\:a_1x\:+\:a_0}\\&{\color{purple}a_nx^n}+{\color{red}\frac{a_n}{b_m}x^{n-m}}{\color{blue}b_{m-1}x^{m-1}}+\cdots\\&\overline{0\:+\:c_{m-1}x^{n-1}+(a_{n-2}-\frac{a_nb_{m-2}}{b_m})x^{n-2}+\cdots}\\&0\:+{\color{purple}c_{m-1}x^{n-1}}+{\color{red}\frac{c_{m-1}}{b_m}x^{n-m-1}}{\color{blue}b_{m-2}x^{m-1}}+\cdots\\&\overline{0\:+\:0+(a_{n-2}-\frac{a_nb_{m-2}}{b_m}-{\color{red}\frac{c_{m-1}{\color{blue}b_{m-2}}}{b_m}}){\color{purple}x^{n-2}}+\cdots}\end{align}$$$(iii)$ 不断重复这样的操作, 直到新被除式的次数低于除式, 由于多项式的次数是有限的, 新被除式的次数是严格递减的, 故结果可以在有限步内得到
	$(iv)$ 结果式如下$$\begin{align}&{\color{red}\frac{a_n}{b_m}x^{n-m}+\frac{c_{m-1}}{b_m}x^{n-m-1}+\cdots\qquad\qquad\triangleq h(x)}\\\,{\color{blue}b_mx^m\:+\:b_{m-1}x^{m-1}\:+\:\cdots\:b_1x\:+\:b_0})&\overline{\,a_nx^n\:+\:a_{n-1}x^{n-1}\:+\:\cdots\:a_1x\:+\:a_0}\\&{\color{purple}a_nx^n}+{\color{red}\frac{a_n}{b_m}x^{n-m}}{\color{blue}b_{m-1}x^{m-1}}+\cdots\\&\overline{0\:+\:c_{m-1}x^{n-1}+(a_{n-2}-\frac{a_nb_{m-2}}{b_m})x^{n-2}+\cdots}\\&0\:+{\color{purple}c_{m-1}x^{n-1}}+{\color{red}\frac{c_{m-1}}{b_m}x^{n-m-1}}{\color{blue}b_{m-2}x^{m-1}}+\cdots\\&\overline{0\:+\:0+(a_{n-2}-\frac{a_nb_{m-2}}{b_m}-{\color{red}\frac{c_{m-1}{\color{blue}b_{m-2}}}{b_m}}){\color{purple}x^{n-2}}+\cdots}\\&\qquad\qquad\qquad\qquad\quad\cdots\cdots\\&\overline{\qquad\qquad\qquad{\color{purple}r(x)\qquad(\deg\,r(x)<\deg\,g(x))}\qquad}\end{align}$$ 则结果为 $f(x)=h(x)g(x)+r(x)$ 
_

# 最大公因式

完全类似于整数的数论中相关内容，有了整除，带余除法等基本工具后，在多项式环中，同样可以研究最大公因式，最小公倍式等概念像探究整数环结构一样，进而进一步探究多项式环的结构。

**定义**: 在 $\mathbf F[x]$ 中, 若 $c(x)|f(x)$ 且 $c(x)|g(x)$ , 则称 $c(x)$ 为 $f(x)$ 与 $g(x)$ 的一个**公因式** .

**定义**: 若 $\mathbf F[x]$ 中的多项式 $f(x)$ 和 $g(x)$ 有一个公因式 $d(x)$ 对于 $f(x)$ 与 $g(x)$ 的任一公因式 $c(x)$ , 都有 $c(x)|d(x)$ , 则称 $d(x)$ 是一个 $f(x)$ 与 $g(x)$ 的**最大公因式** .
不难知道, $f(x)$ 与 $g(x)$ 的最大公因式不唯一, 且任意两个它们的最大公因式是相伴的, 那么可写为 $\lambda d(x)$ 的形式 $(\lambda\neq0)$ , 特别地, 将**首项系数为 $1$** 的最大公因式称作 $f(x)$ 与 $g(x)$ 的**首一最大公因式**, 通常记作 $(f(x),g(x))$ 或 $\gcd(f(x),g(x))$ .

_将 $\gcd$ 看做一个函数，如此，它关于两个变元 $f(x),g(x)$ 对称，即 $\gcd(f(x),g(x))=\gcd(g(x),f(x))$_

有了最大公因式的定义，但是需要探究如何求任给的两个多项式的最大公因式
在此之前更是不清楚是否任何时候都存在最大公因式

**引理**: 设 $f(x),g(x)\in\mathbf F[x]$ , 若在 $\mathbf F[x]$ 中有等式 $f(x)=h(x)g(x)+r(x)$ 成立, 则$$c(x)|f(x)\,且\,c(x)|g(x)\iff c(x)|g(x)\,且\,c(x)|r(x)$$ 进而有$$d(x)\sim(f(x),g(x))\iff d(x)\sim(g(x),r(x))$$ 
这个结论非常显然，但是却可以推出下面这个至关重要的定理：

**定理**: 对于 $\mathbf F[x]$ 中任意两个多项式 $f(x),g(x)$ , 存在它们的一个最大公因式 $d(x)$ , 并且存在 $u(x),v(x)\in\mathbf F[x]$  , 使得$$u(x)f(x)+v(x)g(x)=d(x)$$ 
这和整数中的 $\mathrm{B\acute{e}zout}$ 定理毫无二致，这再次道出了整数环与多项式环间有许许多多的相同之处。

这个定理的证明过程是一个经典且重要的算法，可以通过该方法求出最大公因式

**辗转相除法**: 已知多项式 $f(x),g(x)$
	$(i)$ 若其中一个(不妨为 $g(x)$) 为 $0$ , 则 $(f(x),g(x))=f(x)$ 
	$(ii)$ 均不为 $0$ , 做带余除法, $f(x)=h_1(x)g(x)+r_1(x)$  $(\deg\,r_1(x)<\deg\,g(x))$ 
	$(iii)$ 对于 $g(x),r_1(x)$ 做带余除法, 即 $g(x)=h_1(x)r_1(x)+r_2(x)$  $(\deg\,r_2(x)<r_1(x))$ 
	$\cdots\cdots$
	(\*) 对于 $r_n(x),r_{n+1}(x)$ 做带余除法, 若此时除尽, 即 $r_n(x)=h_{n+1}(x)r_{n+1}(x)$ , 即得到 $(f(x),g(x))=r_{n+1}(x)$ , 这是因为$$(f(x),g(x))=(g(x),r_1(x))=(r_1(x),r_2(x))=\cdots=(r_n(x),r_{n+1}(x))=(r_{n+1}(x),0)$$ 由于多项式的次数是有限的, 故上述步骤将在有限步内结束

**性质**: 
	$(1)$ 设 $f(x),g(x)\in\mathbf F[x]$ , $a,b\in\mathbf F^*$ , 则 $d(x)$ 为 $f(x)$ 与 $g(x)$ 的一个最大公因式当且仅当 $d(x)$ 为 $af(x)$ 与 $bg(x)$ 的一个最大公因式
	$(2)$ $\mathbf F[x]$ 中, 若 $d(x)$ 为 $f(x)$ 与 $g(x)$ 的一个最大公因式, 则对 $\forall\,a\in\mathbf F$ , $ad(x)$ 为 $f(x)$ 与 $g(x)$ 的一个最大公因式
	$(3)$ 若 $f(x),g(x)\in\mathbf F[x]$ , $\mathbf F\subseteq\mathbf K$ , 则 $f(x),g(x)$ 在 $\mathbf F$ 和 $\mathbf K$ 中的首一最大公因式是一样的, 即数域的扩大不改变首一最大公因式

**定义**: 设 $f(x),g(x)\in\mathbf F[x]$ , 若 $(f(x),g(x))=1$ , 则称 $f(x)$ 与 $g(x)$ **互素**

**定理**: $f(x),g(x)$ 在 $\mathbf F[x]$ 中互素当且仅当存在 $u(x),v(x)\in\mathbf F[x]$ 使得 $u(x)f(x)+v(x)g(x)=1$ 

**性质**: 
	$(1)$ 在 $\mathbf F[x]$ 中, 若 $f(x)|g(x)h(x)$ 且 $(f(x),g(x))=1$ 则 $f(x)|h(x)$
	$(2)$ 在 $\mathbf F[x]$ 中, 若 $f(x)|h(x)$ , $g(x)|h(x)$ 且有 $(f(x),g(x))=1$ 则 $f(x)g(x)|h(x))$
	$(3)$ 在 $\mathbf F[x]$ 中, 若 $(f(x),h(x))=1$ , $(g(x),h(x))=1$ , 则 $(f(x)g(x),h(x))=1$ 
	$(3-*)$ 在 $\mathbf F[x]$ 中, 若 $(f_i(x),h(x))=1$ , $(i=1,2,...,s)$ , 则 $(f_1(x)f_2(x)\cdots f_s(x),h(x))=1$ 

对于多个多项式的情况, 有类似的讨论

**定义**: $\mathbf F[x]$ 中, 若 $f_1(x),f_2(x),...,f_s(x)$ 的公因式 $d(x)$ 整除于 $f_1(x),f_2(x),...,f_s(x)$ 的任一公因式, 则称 $d(x)$ 为 $f_1(x),f_2(x),...,f_s(x)$ 的一个**最大公因式**, 且它们的所有最大公因式相伴, 其中首项系数为 $1$ 的最大公因式称为**首一最大公因式**, 记作 $(f_1(x),f_2(x),...,f_s(x))$ 或 $\gcd(f_1(x),f_2(x),...,f_s(x))$ 

可以证明 $(f_1(x),f_2(x),...,f_s(x))=((f_1(x),f_2(x),...,f_{s-1}(x)),f_s(x))$ , 进而可以归纳得到：

**定理**: 在 $\mathbf F[x]$ 中, 有多项式 $f_i(x)$, 则存在多项式 $u_i(x)$ , $(i=1,2,...,s)$
使得 $u_1(x)f_1(x)+u_2(x)f_2(x)+\cdots+u_s(x)f_s(x)=(f_1(x),f_2(x),...,f_s(x))$ 

**定义**: 在 $\mathbf F[x]$ 中, 若 $f_1(x),f_2(x),...,f_s(x)$ 满足 $(f_1(x),f_2(x),...,f_s(x))=1$ , 则称它们**互素**

**定理**: 多项式 $f_i(x)$ 在 $\mathbf F[x]$ 中互素当且仅当存在 $u_i(x)\in\mathbf F[x]$ , $(i=1,2,...,s)$ 使得$$u_1(x)f_1(x)+u_2(x)f_2(x)+\cdots+u_s(x)f_s(x)=1$$ 

# 唯一因式分解定理

类似于整数的唯一素数分解，任意整数都是由素数'构'成的，多项式环中的元素也可以分解为其中一些最基本的元素

**定义**: 设 $\mathbf F[x]$ 中次数大于 $0$ 的多项式 $f(x)$ , 若 $f(x)$ 在 $\mathbf F[x]$ 中的因式只有零次多项式和 $f(x)$ 的相伴元, 那么称 $f(x)$ 为域 $\mathbf F$ 上的一个**不可约多项式**, 否则称 $f(x)$ 在 $\mathbf F$ 上是**可约的**

**定理**: 设 $p(x)$ 是 $\mathbf F[x]$ 中一个次数大于 $0$ 的多项式, 则下面的命题等价: 
	$(1)$ $p(x)$ 是不可约多项式
	$(2)$ $\forall\,f(x)\in\mathbf F[x]$ , 有 $p(x)|f(x)$ 或 $(p(x),f(x))=1$
	$(3)$ 在 $\mathbf F[x]$ 中, 从 $p(x)|f(x)g(x)$ 可推出$$p(x)|f(x)\quad或\quad p(x)|g(x)$$$(4)$ 在 $\mathbf F[x]$ 中, $p(x)$ 不能分解成两个次数较低的多项式的乘积

