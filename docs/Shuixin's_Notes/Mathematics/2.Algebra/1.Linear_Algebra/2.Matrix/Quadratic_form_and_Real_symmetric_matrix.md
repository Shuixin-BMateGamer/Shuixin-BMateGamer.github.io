
**定义**: 如果对于 $\mathbb{R}^{n}$ 中任意的非零列向量 $\alpha$ 都有 $\alpha^{'}A\alpha>0$, 就将 $n$ 元实二次型 $x^{'}Ax$ 称为**正定的**

**定理**: $n$ 元二次型 $x^{'}Ax$ 为正定的当且仅当它的正惯性指数为 $n$
**[证明]**:
	(必要性) 设 $x^{'}Ax$ 是正定的, 做非退化线性替换 $x=Cy$ , 使得化为规范形: $$y_{1}^{2}+\cdots+y_{p}^{2}-y_{p+1}^{2}-\cdots-y_{r}^{2}$$如若 $p<n$ , 则 $y_{n}^{2}$ 的系数或者为 $0$ , 或者为 $-1$ , 取 $y_{0}=(0,\cdots,0,1)^{'}$ , $x_{0}=Cy_{0}$ 
    由于有 $y_{0}^{'}C^{'}ACy_{0}=0$ 或 $y_{0}^{'}C^{'}ACy_{0}=-1$ , 即有 $x_{0}^{'}Ax_{0}=0$ 或 $x_{0}^{'}Ax_{0}=-1$ , 这就与 $x^{'}Ax$ 正定矛盾, 于是 $p=n$
    (充分性) 显然

**推论**:  $n$ 元实二次型 $x^{'}Ax$ 正定
$\iff$ 规范形为 $y_{1}^{2}+y_{2}^{2}+\cdots+y_{n}^{2}$
$\iff$ 它的标准形中的 $n$ 个系数全都大于 $0$

**定义**: 如果实二次型 $x^{'}Ax$ 是正定的, 即对于 $\mathbb{R}^{n}$ 中的任意非零列向量 $\alpha$ , 有 $\alpha^{'}A\alpha>0$, 称实对称矩阵 $A$ 为**正定**的, 正定的实对称矩阵称为**正定矩阵**

**定理**:  $n$ 级实对称矩阵 $A$ 为正定的
$\iff$ $A$ 的正惯性指数等于 $n$
$\iff$ $A\simeq I$ 
$\iff$ $A$ 的合同标准形中主对角元全大于 $0$
$\iff$ $A$ 的特征值全大于 $0$

**推论**:
	$(1)$ 与正定矩阵合同的实对称矩阵为正定矩阵
	$(2)$ 与正定二次型等价的实二次型为正定的, 也就是说非退化线性替换不改变实二次型的正定性
	$(3)$ 正定矩阵的行列式大于零

**定理**: 实对称矩阵 $A$ 为正定矩阵的充要条件为 $A$ 的所有顺序主子式都大于零
**[证明]**:
	(必要性) 设 $A=\begin{bmatrix}A_{k}&B_{1}\\ B_{1}^{'}&B_{2}\end{bmatrix}$ , $A_{k}$ 为 $A$ 的 $k$ 阶顺序主子式
	 由于 $A$ 正定, 那么取 $\delta=\begin{bmatrix}\delta_{k}\\0\end{bmatrix}$ , 这里 $\delta_{k}$ 为 $\mathbb{R}^{k}$ 中的任意非零列向量, 使得 $\delta$ 为 $n$ 维非零列向量, 则有:$$0<\delta^{'}A\delta=\begin{bmatrix}\delta_{k}^{'}&0\end{bmatrix}\begin{bmatrix}A_{k}&B_{1}\\ B_{1}^{'}&B_{2}\end{bmatrix}\begin{bmatrix}\delta_{k}\\0\end{bmatrix}=\delta_{k}^{'}A_{k}\delta_{k}$$这就说明了 $A_{k}$ 是正定的
	 (充分性) 对 $A$ 的级数 $n$ 归纳
	 $n=1$ 时显然成立, 
	 假设级数为 $n-1$ 时命题成立, 则对于级数为 $n$ 时, 设 $$A=\begin{bmatrix}A_{n-1}&\beta_{1}\\ \beta_{1}^{T}&b_{0}\end{bmatrix}$$注意到 $A$ 的 $1\sim n-1$ 阶的顺序主子式就为 $A_{n-1}$ 的所有顺序主子式, 由题设它们都大于零, 由归纳假设应有 $A_{n-1}$ 正定, 那么 $A_{n-1}\simeq I_{n-1}$ , 故存在 $n-1$ 阶可逆阵 $C_{0}$ 使得 $$C_{0}^{'}A_{n-1}C_{0}=I_{n-1}$$那么若取 $C=\begin{bmatrix}C_{0}&0\\0&1\end{bmatrix}$ , 就有 $$\begin{bmatrix}C_{0}^{'}&0\\0&1\end{bmatrix}\begin{bmatrix}A_{n-1}&0\\ 0&b\end{bmatrix}\begin{bmatrix}C_{0}&0\\0&1\end{bmatrix}=\begin{bmatrix}C_{0}^{'}A_{n-1}C_{0}&0\\0&b\end{bmatrix}=\begin{bmatrix}I_{n-1}&0\\0&b\end{bmatrix}$$**引理**: 若 $$A=\begin{bmatrix}A_{1}&A_{2}\\A_{3}&A_{4}\end{bmatrix}$$为 $n$ 级对称矩阵, $A_{1}$ 为 $r$ 级可逆矩阵, 则有 $$A\simeq\begin{bmatrix}A_{1}&O\\O&A_{4}-A_{2}^{'}A_{1}^{-1}A_{2}\end{bmatrix}$$**[证明]**:
		 首先有 $A_{3}=A_{2}^{'}$ , 由于 $$\begin{bmatrix}I_{r}&O\\-A_{2}^{'}A_{1}^{-1}&I_{n-r}\end{bmatrix}\begin{bmatrix}A_{1}&A_{2}\\A_{2}^{'}&A_{4}\end{bmatrix}\begin{bmatrix}I_{r}&-{(A_{1}^{'})}^{-1}A_{2}\\O&I_{n-r}\end{bmatrix}=\begin{bmatrix}A_{1}&O\\O&A_{4}-A_{2}^{'}A_{1}^{-1}A_{2}\end{bmatrix}$$并且 $\begin{bmatrix}I_{r}&O\\-A_{2}^{'}A_{1}^{-1}&I_{n-r}\end{bmatrix}^{'}=\begin{bmatrix}I_{r}&-{(A_{1}^{'})}^{-1}A_{2}\\O&I_{n-r}\end{bmatrix}$ , 故 $A\simeq\begin{bmatrix}A_{1}&O\\O&A_{4}-A_{2}^{'}A_{1}^{-1}A_{2}\end{bmatrix}$
		 即证
	由引理可由 $A=\begin{bmatrix}A_{n-1}&\beta_{1}\\ \beta_{1}^{T}&b_{0}\end{bmatrix}$ 得到 $A\simeq\begin{bmatrix}A_{n-1}&O\\ O&b_{0}-\beta_{1}^{T}A_{n-1}^{-1}\beta_{1}\end{bmatrix}$ , 记 $b=b_{0}-\beta_{1}^{T}A_{n-1}^{-1}\beta_{1}$ , 现在有 $$A\simeq\begin{bmatrix}A_{n-1}&O\\ O&b\end{bmatrix},\quad \begin{bmatrix}A_{n-1}&O\\ O&b\end{bmatrix}\simeq\begin{bmatrix}I_{n-1}&O\\ O&b\end{bmatrix}$$故有 $$A\simeq\begin{bmatrix}I_{n-1}&O\\ O&b\end{bmatrix}$$另一方面 $$|A|=\lambda^{2}|A_{n-1}|b>0\implies b>0$$故 $$A\simeq\begin{bmatrix}I_{n-1}&O\\ O&1\end{bmatrix}=I_{n}$$这就证明了 $A$ 为正定矩阵, 即阶数为 $n$ 时成立
	由归纳法可知对阶数为任意的正整数 $n$ 时结论成立

**推论**: 实二次型 $x^{'}Ax$ 正定当且仅当 $A$ 的所有顺序主子式大于零

**定义**: 如果对于 $\mathbb{R}^n$ 的任一非零向量 $\alpha$ , 有 $\alpha^{'}A\alpha\geq0$ , 则称 $n$ 元实二次型 $x^{'}Ax$ 称为**半正定的**

**定义**: 如果实二次型 $x^{'}Ax$ 是半正定的, 则称实对称矩阵 $A$ 为**半正定的**

类似还可以定义**负定的**, **半负定的**
如果实对称矩阵或是实二次型**既不半正定也不半负定**, 就称它是**不定的**

**定理**:  $n$ 元实二次型 $x^{'}Ax$ 半正定
$\iff$ 其正惯性指数为它的秩
$\iff$ 规范形为 $y_{1}^{2}+y_{2}^{2}+\cdots+y_{r}^{2}$ , $(0\leq r\leq n)$
$\iff$ 标准形的 $n$ 个系数非负

**推论**: $n$ 级实对称矩阵 $A$ 半正定
$\iff$ $A$ 的正惯性指数为它的秩
$\iff$ $A\simeq\begin{bmatrix}I_{r}&O\\O&O\end{bmatrix}$ , $r=\mathrm{rank}(A)$
$\iff$ $A$ 的合同标准形的 $n$ 个主对角元非负
$\iff$ $A$ 的特征值全非负

**定理**: 实对称矩阵 $A$ 半正定当且仅当 $A$ 的所有主子式非负