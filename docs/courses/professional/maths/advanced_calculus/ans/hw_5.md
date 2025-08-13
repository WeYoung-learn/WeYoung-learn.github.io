# 高等微积分 （2） 第5次作业

Chasse_neige

### 1. 计算偏导数

(1) 设 $f \in C^1(\mathbb{R}, \mathbb{R})$, $z = xy + xf\left( \dfrac{y}{x} \right)$. 求 $x \dfrac{\partial z}{\partial x} + y \dfrac{\partial z}{\partial y}$
$$
\begin{aligned}
\frac{\partial z}{\partial x} &= y + f\left(\frac{y}{x}\right) + x f'\left(\frac{y}{x}\right) \cdot \left(-\frac{y}{x^2}\right) = y + f\left(\frac{y}{x}\right) - \frac{y}{x}f'\left(\frac{y}{x}\right) \\\\
\frac{\partial z}{\partial y} &= x + x f'\left(\frac{y}{x}\right) \cdot \frac{1}{x} = x + f'\left(\frac{y}{x}\right) \\\\
x \frac{\partial z}{\partial x} + y \frac{\partial z}{\partial y} &= x\left(y + f\left(\frac{y}{x}\right) - \frac{y}{x}f'\left(\frac{y}{x}\right)\right) + y\left(x + f'\left(\frac{y}{x}\right)\right) \\\\
&= xy + xf\left(\frac{y}{x}\right) - yf'\left(\frac{y}{x}\right) + xy + yf'\left(\frac{y}{x}\right) \\\\
&= 2xy + xf\left(\frac{y}{x}\right) = 2xy + z - xy = xy + z
\end{aligned}
$$

(2) 设 $f \in C^2(\mathbb{R}^2, \mathbb{R})$, $z = f(x, xy)$. 求 $\dfrac{\partial^2 z}{\partial y^2}$

$$
\begin{aligned}
\frac{\partial z}{\partial y} &= f_{2}' (x, xy) \cdot x \\\\
\frac{\partial^2 z}{\partial y^2} &= \frac{\partial}{\partial y} \left(x f_{2}'(x, xy)\right) = x \cdot \left(f_{22}'' (x, xy) \cdot x\right) = x^2 f_{22}'' (x, xy)
\end{aligned}
$$

(3) 设 $f, g \in C^2(\mathbb{R}, \mathbb{R})$, $z = xf\left( \dfrac{y}{x} \right) + yg\left( \dfrac{x}{y} \right)$. 求 $\dfrac{\partial^2 z}{\partial x \partial y}$
$$
\begin{aligned}
\frac{\partial z}{\partial y} &= x f'\left(\frac{y}{x}\right) \cdot \frac{1}{x} + g\left(\frac{x}{y}\right) + y g'\left(\frac{x}{y}\right) \cdot \left(-\frac{x}{y^2}\right) = f'\left(\frac{y}{x}\right) + g\left(\frac{x}{y}\right) - \frac{x}{y}g'\left(\frac{x}{y}\right) \\\\
\frac{\partial^2 z}{\partial x \partial y} &= \frac{\partial}{\partial x} \left( f'\left(\frac{y}{x}\right) + g\left(\frac{x}{y}\right) - \frac{x}{y}g'\left(\frac{x}{y}\right) \right) \\\\
&= f''\left(\frac{y}{x}\right)\left(-\frac{y}{x^2}\right) + g'\left(\frac{x}{y}\right)\frac{1}{y} - \left[ \frac{1}{y}g'\left(\frac{x}{y}\right) + \frac{x}{y} g''\left(\frac{x}{y}\right) \frac{1}{y} \right] \\\\
&= -\frac{y}{x^2}f''\left(\frac{y}{x}\right) - \frac{x}{y^2}g''\left(\frac{x}{y}\right)
\end{aligned}
$$

(4) 设 $f \in C^1(\mathbb{R}, \mathbb{R})$, $z = \dfrac{y}{f(x^2 - y^2)}$. 求 $\dfrac{1}{x} \dfrac{\partial z}{\partial x} + \dfrac{1}{y} \dfrac{\partial z}{\partial y}$
$$
\begin{aligned}
\frac{\partial z}{\partial x} &= y \cdot \left(-\frac{1}{f^2(x^2-y^2)}\right) \cdot f'(x^2-y^2) \cdot (2x) = -\frac{2xy f'(x^2-y^2)}{f^2(x^2-y^2)} \\\\
\frac{\partial z}{\partial y} &= \frac{1 \cdot f(x^2-y^2) - y \cdot f'(x^2-y^2) \cdot (-2y)}{f^2(x^2-y^2)} = \frac{f(x^2-y^2) + 2y^2 f'(x^2-y^2)}{f^2(x^2-y^2)} \\\\
\frac{1}{x} \frac{\partial z}{\partial x} + \frac{1}{y} \frac{\partial z}{\partial y} &= \frac{1}{x}\left(-\frac{2xy f'}{f^2}\right) + \frac{1}{y}\left(\frac{f + 2y^2 f'}{f^2}\right) \\\\
&= -\frac{2y f'}{f^2} + \frac{1}{yf} + \frac{2y f'}{f^2} \\\\
&= \frac{1}{yf(x^2-y^2)} = \frac{z}{y^2}
\end{aligned}
$$

(5) 设 $f \in C^1(\mathbb{R}^3, \mathbb{R})$, $u = f(x, xy, xyz)$. 求 $\dfrac{\partial u}{\partial x}, \dfrac{\partial u}{\partial y}, \dfrac{\partial u}{\partial z}$
$$
\begin{aligned}
\frac{\partial u}{\partial x} &= f_{1}'(x, xy, xyz) \cdot 1 + f_{2}'(x, xy, xyz) \cdot y + f_{3}'(x, xy, xyz) \cdot yz \\\\
\frac{\partial u}{\partial y} &= f_{1}'(x, xy, xyz) \cdot 0 + f_{2}'(x, xy, xyz) \cdot x + f_{3}'(x, xy, xyz) \cdot xz = x f_{2}' + xz f_{3}' \\\\
\frac{\partial u}{\partial z} &= f_{1}'(x, xy, xyz) \cdot 0 + f_{2}'(x, xy, xyz) \cdot 0 + f_{3}'(x, xy, xyz) \cdot xy = xy f_{3}'
\end{aligned}
$$
*这里, 我们称函数 $f : \mathbb{R}^n \rightarrow \mathbb{R}$ 是 $C^k$ 光滑的, 记作 $f \in C^k(\mathbb{R}^n, \mathbb{R})$, 如果 $f$ 的各个 $k$ 阶 (偏) 导函数都存在且连续。*

### 2.
给定 $C^1$ 光滑的函数 $F : \mathbb{R}^3 \rightarrow \mathbb{R}$. 求函数
$$
F(u^2 - x^2, u^2 - y^2, u^2 - z^2)
$$
对 $x, y, z, u$ 的偏导数
$$
\begin{aligned}
\frac{\partial F}{\partial x} &= F_{1}'(u^2-x^2, \dots) \cdot (-2x) = -2x F_{1}' \\\\
\frac{\partial F}{\partial y} &= F_{2}'(u^2-x^2, \dots) \cdot (-2y) = -2y F_{2}' \\\\
\frac{\partial F}{\partial z} &= F_{3}'(u^2-x^2, \dots) \cdot (-2z) = -2z F_{3}' \\\\
\frac{\partial F}{\partial u} &= F_{1}' \cdot (2u) + F_{2}' \cdot (2u) + F_{3}' \cdot (2u) = 2u (F_{1}' + F_{2}' + F_{3}')
\end{aligned}
$$

### 3.
给定 $n \times n$ 的对称实矩阵 $(A_{ij})_{1 \leq i,j \leq n}$(即对任何 $i, j$, 有 $A_{ij} = A_{ji}$). 定义二次函数
$$
Q(x_1, \ldots, x_n) = \sum_{i=1}^n \sum_{j=1}^n A_{ij} x_i x_j, \quad \forall (x_1, \ldots, x_n) \in \mathbb{R}^n
$$

(1) 求 $Q$ 的微分
$$
\begin{aligned}
\frac{\partial Q}{\partial x_k} &= \sum_{i=1}^n \sum_{j=1}^n A_{ij} (\delta_{ik} x_j + x_i \delta_{jk}) = \sum_{j=1}^n A_{kj} x_j + \sum_{i=1}^n A_{ik} x_i = 2 \sum_{j=1}^n A_{kj} x_j \\\\
dQ &= \sum_{k=1}^n \frac{\partial Q}{\partial x_k} dx_k = 2 \sum_{k=1}^n \sum_{j=1}^n A_{kj} x_j dx_k
\end{aligned}
$$

(2) 设 $f : \mathbb{R}^n \rightarrow \mathbb{R}$ 是 $C^1$ 光滑的函数. 定义函数
$$
g(x_1, \ldots, x_n) = f(x_1, \ldots, x_n) e^{- \frac{1}{2} Q(x_1, \ldots, x_n)}.
$$
计算 $g$ 的各个偏导数 $\dfrac{\partial g}{\partial x_1}, \ldots, \dfrac{\partial g}{\partial x_n}$.
$$
\begin{aligned}
\frac{\partial g}{\partial x_{k}} &= \frac{\partial f}{\partial x_k} e^{- \frac{1}{2} Q} + f \cdot e^{- \frac{1}{2} Q} \cdot \left(-\frac{1}{2} \frac{\partial Q}{\partial x_k}\right) \\\\
&= f_{k}' e^{- \frac{1}{2} Q} - \frac{1}{2} f e^{- \frac{1}{2} Q} \left(2 \sum_{j=1}^n A_{kj} x_j\right) \\\\
&= \left( f_{k}' - f \sum_{j=1}^n A_{kj} x_j \right) e^{- \frac{1}{2} Q}
\end{aligned}
$$

### 4.
设 $f : \mathbb{R}^3 \rightarrow \mathbb{R}$ 是 $C^1$ 光滑的函数, 即 $f$ 的各个偏导数都存在且连续.

(1) 对于给定的点 $(x, y, z) \in \mathbb{R}^3$, 考虑关于 $t$ 的一元函数
$$
g(t) = f(tx, ty, tz).
$$
求 $g'(t)$

$$
g'(t) = f_{x}' (tx, ty, tz) \cdot x + f_{y}' (tx, ty, tz) \cdot y + f_{z}' (tx, ty, tz) \cdot z
$$

(2) 证明: 对任何 $(x, y, z) \in \mathbb{R}^3$, 有
$$
f(x, y, z) = f(0, 0, 0) + x \int_0^1 f_x(tx, ty, tz) \, dt + y \int_0^1 f_y(tx, ty, tz) \, dt + z \int_0^1 f_z(tx, ty, tz) \, dt
$$
**证明：**
根据微积分基本定理，我们有 $g(1) = g(0) + \int_0^1 g'(t) dt$。
代入 $g(t)$ 的定义：
$$
\begin{aligned}
f(x, y, z) &= f(0, 0, 0) + \int_0^1 \left( x f_{x}'(tx, ty, tz) + y f_{y}'(tx, ty, tz) + z f_{z}' (tx, ty, tz) \right) dt \\\\
&= f(0, 0, 0) + x \int_0^1 f_x(tx, ty, tz) \, dt + y \int_0^1 f_y(tx, ty, tz) \, dt + z \int_0^1 f_z(tx, ty, tz) \, dt
\end{aligned}
$$

在本题 (3), (4) 小问中假设 $f$ 满足: 对任何 $(x, y, z) \in \mathbb{R}^3$ 都有
$$
x f_x(x, y, z) + y f_y(x, y, z) + z f_z(x, y, z) = n f(x, y, z),
$$
其中 $n$ 是某个给定的正整数.

(3) 对于给定的点 $(x, y, z) \in \mathbb{R}^3$, 考虑关于 $t$ 的一元函数
$$
h(t) = \dfrac{f(tx, ty, tz)}{t^n}.
$$
求 $h'(t)$
$$
\begin{aligned}
h'(t) &= \frac{g'(t) \cdot t^n - g(t) \cdot n t^{n-1}}{(t^n)^2} \\\\
&= \frac{t \cdot g'(t) - n \cdot g(t)}{t^{n+1}} \\\\
&= \frac{t(x f'_x + y f'_y + z f'_z) - n f(tx, ty, tz)}{t^{n+1}}
\end{aligned}
$$

(4) 证明: 对任何 $(x, y, z) \in \mathbb{R}^3$ 与 $t > 0$, 都有
$$
f(tx, ty, tz) = t^n f(x, y, z)
$$
**证明：**
根据齐次函数的条件，令 $x' = tx, y' = ty, z' = tz$，我们有
$$
x' f_x(x', y', z') + y' f_y(x', y', z') + z' f_z(x', y', z') = n f(x', y', z')
$$
代入 $g(t)$ 和 $g'(t)$ 的表达式，得到：
$$
t \cdot g'(t) = (tx) f_{x}' (tx,...) + (ty) f_{y}' (tx,...) + (tz) f_{z}' (tx,...) = n f(tx, ty, tz) = n g(t)
$$
这就给出了一个关于 $g(t)$ 的微分方程：$t g'(t) = n g(t)$。
分离变量得：
$$
\frac{dg}{g} = n \frac{dt}{t}
$$
对两边从 $1$ 到 $t$ 进行积分：
$$
\begin{aligned}
\int_{g(1)}^{g(t)} \frac{d\gamma}{\gamma} &= n \int_{1}^{t} \frac{d\tau}{\tau} \\\\
\ln|g(t)| - \ln|g(1)| &= n (\ln|t| - \ln|1|) \\\\
\ln\left(\frac{g(t)}{g(1)}\right) &= n \ln(t) = \ln(t^n) \\\\
g(t) &= g(1) \cdot t^n
\end{aligned}
$$
代回 $f$ 的定义，即得：
$$
f(tx, ty, tz) = t^n f(x, y, z)
$$