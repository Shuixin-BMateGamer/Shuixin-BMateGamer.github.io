在已经简化了许多内容的讨论过[[Fourier级数]]过后，下面将对其重新严格化广义化讨论
# 一般概念

做为对[[有度量的线性空间]]中内积空间的实例应用，我们讨论以函数作为‘‘向量’‘的函数系，并且在 $\mathfrak R_{2}[X,\mathbb{C}]$ 中定义了内积 $$\langle f,g\rangle:=\int_{X}(f\cdot g)(x)\,\mathrm{d}x\tag{1}$$
可以举出正交函数系的例子，并且也是接下来我们要研究的：
	指数函数系 $\{e^{inx}:n\in\mathbb{Z}\}$ 是空间 $\mathfrak R_{2}([-\pi,\pi],\mathbb{C})$ 中关于内积 $(1)$ 的正交函数系;
	三角函数系 $\{1,\cos nx,\sin nx:n\in\mathbb{N}\}$ 是 $\mathfrak R_{2}([-\pi,\pi],\mathbb{R})$ 中的正交函数系
	（由欧拉公式，上面两个函数系可以彼此线性表出，因此他们是等价的，也将上面提到的指数函数系称作**三角函数系**，更精确的，**复形式的三角函数系**）$$\bigg\{\frac{1}{\sqrt{2l}}e^{\frac{i\pi nx}{l}}:n\in\mathbb{Z}\bigg\}\qquad\qquad\bigg\{\frac{1}{\sqrt{2l}},\frac{1}{\sqrt{l}}\cos\frac{\pi}{l}nx,\frac{1}{\sqrt{l}}\sin\frac{\pi}{l}nx:n\in\mathbb{N}\bigg\}$$则分别为它们对应的规范正交函数系

对于内积空间中求正交向量组的**Gram-Schmidt正交化方法**，连同一带的**规范(单位)化**在函数空间中表示为：$$\varphi_{1}=\frac{\psi_{1}}{||\psi_{1}||},\qquad\varphi_{2}=\frac{\psi_{2}-\langle\psi_{2},\varphi_{1}\rangle\varphi_{1}}{||\psi_{2}-\langle\psi_{2},\varphi_1\rangle\varphi_{1}||},\qquad\cdots\qquad\varphi_{n}=\frac{\psi_{n}-\sum\limits_{k=1}^{n-1}\langle\psi_{n},\varphi_{k}\rangle\varphi_{k}}{||\psi_{n}-\sum\limits_{k=1}^{n-1}\langle\psi_{n},\varphi_{k}\rangle\varphi_{k}||}$$作为一个与规范正交方法相关的例子：参考[[Legendre多项式]]

