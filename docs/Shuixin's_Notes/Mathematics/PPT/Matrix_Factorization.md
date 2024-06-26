# 引言
我们知道矩阵实际上为欧式空间中的线性变换，或是说变换
对于如一个 $n$ 维向量左乘一个 $n$ 级矩阵得到一个变换后 $n$ 维向量实际上视作将原向量在 $n$ 维空间中旋转拉伸，在单步的左乘矩阵中，这个过程如下理解：$$\begin{align}\begin{bmatrix}a_{11}&a_{12}&\cdots&a_{1n}\\a_{21}&a_{22}&\cdots&a_{2n}\\\vdots&\vdots&\ddots&\vdots\\a_{n1}&a_{n2}&\cdots&a_{nn}\end{bmatrix}\begin{bmatrix}x_{1}\\x_{2}\\\vdots\\x_{n}\end{bmatrix}&=\begin{bmatrix}{\color{red}a_{11}}&{\color{blue}a_{12}}&\cdots&{\color{orange}a_{1n}}\\{\color{red}a_{21}}&{\color{blue}a_{22}}&\cdots&{\color{orange}a_{2n}}\\{\color{red}\vdots}&{\color{blue}\vdots}&\ddots&{\color{orange}\vdots}\\{\color{red}a_{n1}}&{\color{blue}a_{n2}}&\cdots&{\color{orange}a_{nn}}\end{bmatrix}\bigg(x_{1}\begin{bmatrix}1\\0\\\vdots\\0\end{bmatrix}+x_{2}\begin{bmatrix}0\\1\\\vdots\\0\end{bmatrix}+\cdots+x_{n}\begin{bmatrix}0\\0\\\vdots\\1\end{bmatrix}\bigg)\\&=x_{1}\begin{bmatrix}\color{red}a_{11}\\\color{red}a_{21}\\\color{red}\vdots\\\color{red}a_{n1}\end{bmatrix}+x_{2}\begin{bmatrix}\color{blue}a_{12}\\\color{blue}a_{22}\\\color{blue}\vdots\\\color{blue}a_{n2}\end{bmatrix}+\cdots+x_{n}\begin{bmatrix}\color{orange}a_{1n}\\\color{orange}a_{2n}\\\color{orange}\vdots\\\color{orange}a_{nn}\end{bmatrix}\end{align}$$即相当于把标准正交基换成了左乘矩阵的列向量，可以说是将**坐标轴**旋转拉伸成为新的基，进而使得空间中的向量也一同被旋转拉伸了
注意这里的**旋转拉伸**，因为向量的位置其实只由**方向**和**模长**决定，因此无论左乘的方阵如何复杂，也只是将作用于的向量经过了两种操作**旋转**以及**拉伸**，姑且将反射变换算作为负向的拉伸
如此，旋转变换对应的便为**正交矩阵**，拉伸变换对应的便为**对角矩阵**
将矩阵如此分解首先就是旨在将空间中复杂的线性变换剖析开来
即将一个矩阵**分解为若干正交矩阵以及对角矩阵乘积**
下面的论述中，矩阵和线性变换的表述并不做区别
# 方阵与特征分解

既从图形角度考虑入手，那么即使是我们已经熟悉的对角化，也要想想看这么做的动机是什么
对于 $n$ 维向量空间 $V$ ，有一个 $n$ 阶实方阵 $A$ ，它的列向量组为 $\alpha_{1},\alpha_{2},...,\alpha_{n}$ ，
**特征向量**代表的

# 实对称矩阵与谱分解

实对称矩阵拥有十分良好的性质，即任意实对称矩阵都可以被正交相似对角化
这意味着实对称矩阵总能够找到可以作为标准正交基的特征向量组

# 矩阵与奇异值分解
