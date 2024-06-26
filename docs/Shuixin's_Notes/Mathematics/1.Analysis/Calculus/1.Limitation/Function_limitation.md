
**定义**: 函数 $f:E\to \mathbb{R}$ , 若 $\forall\,\varepsilon>0$ , $\exists\,\delta>0$, $s.t.\forall\,x\in E$ , 且 $0<|x-a|<\delta$ , 有 $|f(x)-A|<\varepsilon$ , 则称 $x$ 趋于 $a$ 时, $f$ 趋于 $A$ , 或是说 $A$ 为 $f$ 在 $x$ 趋于 $a$ 时的极限, 记作 $$\lim_{x\to a,x\in E}f(x)=A,\qquad或是\qquad\lim_{E\ni x\to a}f(x)=A$$ 
**定义**: 当一个点的邻域去除该点本身, 将得到的集合称为该点的**去心邻域**, 若 $U(a)$ 表示 $a$ 的邻域, 则用 $\mathring{U}(a)$ 表示对应去心邻域, 还有 $$U_E(a):=E\cap U(a),\qquad\mathring{U}_E(a):=E\cap\mathring{U}(a)$$
**定义**: $$\bigg(\lim_{E\ni x\to a}f(x)=A\bigg):=\forall\,V_{\mathbb{R}}(A)\,\exists\,\mathring{U}_E(a)\,(f(\mathring{U}_E(a)\subset V_{\mathbb{R}}(A))$$即对于 $A$ 任意邻域, 总可以找到一个 $a$ 在 $E$ 中的邻域使得该邻域在 $f$ 下的像包含在 $A$ 的邻域中

**注意**: 这里 $a$ 的邻域需要满足一些条件
	$(B_1)$  $\mathring{U}_{E}(a)\neq\varnothing$
	$(B_2)$ $\forall\,\mathring{U}^{'}_E(a)\,\forall\,\mathring{U}^{''}_E(a)\,\exists\,\mathring{U}_E(a)\,(\mathring{U}_E(a)\subset(\mathring{U}^{'}_E(a)\cap\mathring{U}_E^{''}(a)))$

**定义**: 即便 $f$ 在定义域内并非常函数或是有界函数, 但只要满足在 $a$ 的某个去心邻域内为常函数或是有(上/下)界函数, 就称为**最终常函数**, **最终有(上/下)界函数**

_# 我认为就是局部为常函数或是局部有界_

上面是最常见对于函数极限的相关定义，定义用到的邻域的概念需要满足 $(B_1)$ , $(B_2)$ 两条性质，由此引申出下面的概念，进而对极限的概念进行推广

**定义**: 由集合 $X$ 的某些子集 $B\subset X$ 组成的集合族 $\mathfrak B$ 如果满足下面的性质: 
	$(B_1)$ $\mathring{U}_{E}(a)\neq\varnothing$
	$(B_2)$ $\forall\,\mathring{U}^{'}_E(a)\,\forall\,\mathring{U}^{''}_E(a)\,\exists\,\mathring{U}_E(a)\,(\mathring{U}_E(a)\subset(\mathring{U}^{'}_E(a)\cap\mathring{U}_E^{''}(a)))$ 
则称 $\mathfrak B$ 为 $X$ 的一个**基**

_例：
	$1^{\circ}$ $x\to a$ 意思是 $x$ 趋近于 $a$ ，可以说这类极限过程发生在一个集族上， $x$ 被 $a$ 的所有去心邻域所层层限定，这里说的集族正是一个基 $\mathfrak B$ ，其中的元素都是 $a$ 的去心邻域 $\mathring{U}(a)=\{x\in\mathbb{R}|a-\delta_1<x<a+\delta_2\}$ ，这里 $\delta_1,\delta_2>0$
	$2^\circ$ $x\to+\infty$ 意思是 $x$ 趋近于 $+\infty$ ，类似地，同样也是发生在一个集族 $\mathfrak{C}$ 上，该集族也为一个基，其中元素都为闭球的补集，或是说 $\infty$ 的"邻域" $U(\infty)=\{x\in\mathbb{R}|\delta<|x|\}$ ，这里 $\delta>0$
_

_# **基**的全称是**滤子基**_

**定义**: 设 $f:X\to\mathbb{R}$ 为集合 $X$ 上的函数, $\mathfrak B$ 为 $X$ 中的基, 若对 $A\in\mathbb{R}$ 的任意邻域 $V(A)$ , 可以找到基 $\mathfrak B$ 中的元素 $B$ , 使得 $f(B)\subset V(A)$ , 则称 $A$ 为函数 $f:X\to\mathbb{R}$ 在基 $\mathfrak B$ 上的极限, 记作: $$\lim_{\mathfrak B}f(x)=A$$
