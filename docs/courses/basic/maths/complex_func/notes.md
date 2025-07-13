# 复变函数作业答案



## 复变函数 第1次作业

Chasse_neige

5 若 $|z| = 1$，请证明对任意复数 $a$ 和 $b$，均有
$$
\left| \frac{a z + b}{\overline{b} z + \overline{a}} \right| = 1
$$
证明：由于 $|z| = 1$，所以 $z \overline{z} = 1 $
$$
\left| \frac{a z + b}{\overline{b} z + \overline{a}} \right|  = \frac{|a z + b|}{|\overline{b} z + \overline{a}|} = \frac{|a z + b|}{\left|\overline{\overline{b} z + \overline{a}}\right|} = \frac{|a z + b|}{|b \overline{z} + a|} = \frac{|a z + b|}{|z \overline{z}(b \overline{z} + a)|} = \frac{|a z + b|}{|\overline{z} (b + a z)|} = \frac{|a z + b|}{|\overline{z}| |a z + b|} = 1
$$
6 请利用单倍角的三角函数表示 $\cos(n\theta)$ 和 $\sin(n\theta)$，并给出 $\cos(3\theta)$ 和 $\sin(3\theta)$ 的具体表达式。
$$
\cos (n \theta) = \frac{e^{i n \theta} + e^{- i n \theta}}{2} = \frac{1}{2} ((\cos \theta + i \sin \theta)^{n} + (\cos \theta - i \sin \theta)^{n}) \\ = \frac{1}{2} (\sum_{k = 0}^{n} i^{k} C_{n}^{k} \cos^{n - k} \theta \sin^{k} \theta + \sum_{k = 0}^{n} (-i)^{k} C_{n}^{k} \cos^{n-k} \theta \sin^{k} \theta) = \frac{1}{2} (2 \sum_{k = 0}^{[\frac{n}{2}]} i^{2k} C_{n}^{2k} \cos^{n-2k} \sin^{2k} \theta) \\ = \sum_{k = 0}^{[\frac{n}{2}]} i^{2k} C_{n}^{2k} \cos^{n-2k} \theta \sin^{2k} \theta
$$

$$
\sin (n \theta)  = \frac{e^{i n \theta} - e^{- i n \theta}}{2 i} = \frac{1}{2i} ((\cos \theta + i \sin \theta)^{n} - (\cos \theta - i \sin \theta)^{n}) \\ = \frac{1}{2i} (\sum_{k = 0}^{n} i^{k} C_{n}^{k} \cos^{n - k} \theta \sin^{k} \theta - \sum_{n = 0}^{k} (-i)^{k} \cos^{n - k} \theta \sin^{k} \theta) = \frac{1}{2i} (2i \sum_{n = 0}^{[\frac{n}{2}]} i^{2k} C_{n}^{2k + 1} \cos^{n - 2k - 1} \theta \sin^{2k + 1} \theta) \\ = 
\sum_{n = 0}^{[\frac{n}{2}]} i^{2k} C_{n}^{2k + 1} \cos^{n - 2k - 1} \theta \sin^{2k + 1} \theta
$$

特别地，对于 $n = 3$
$$
\cos (3 \theta) = \sum_{k = 0}^{1} i^{2k} C_{3}^{2k} \cos^{3-2k} \theta \sin^{2k} \theta \\ =
\cos^{3} \theta - 3 \cos \theta \sin^{2} \theta
$$

$$
\sin (3 \theta) = \sum_{n = 0}^{1} i^{2k} C_{3}^{2k + 1} \cos^{3 - 2k - 1} \theta \sin^{2k + 1} \theta \\ =
3 \cos^{2} \theta \sin \theta - \sin^{3} \theta
$$

7 请利用多倍角三角函数的线性关系表达 $\cos^n\theta$ 和 $\sin^n\theta$，并给出 $\cos^3\theta$ 和 $\sin^3\theta$ 的具体表达式。
$$
\cos^{n} \theta = \left( \frac{e^{i  \theta} + e^{- i \theta}}{2} \right)^{n}  = \sum_{k = 0}^{[\frac{n + 1}{2}]} C_{n}^{k} \frac{e^{i (n - 2k) \theta} + e^{- i (n - 2k) \theta}}{2^{n}} = 
\frac{1}{2^{n - 1}} \sum_{k = 0}^{[\frac{n + 1}{2}]} C_{n}^{k} \cos ((n - 2k) \theta)
$$

$$
\sin^{n} \theta = \left( \frac{e^{i  \theta} - e^{- i \theta}}{2 i} \right)^{n}  = \sum_{k = 0}^{[\frac{n + 1}{2}]} C_{n}^{k} \frac{(-1)^{k} e^{i (n - 2k) \theta} + (-1)^{n - k} e^{- i (n - 2k) \theta}}{(2i)^{n}} \\ = 
\begin{cases} \frac{1}{(2i)^{n - 1}} \sum_{k = 0}^{[\frac{n}{2}]} (-1)^{k} C_{n}^{k} \sin ((n - 2k) \theta) & (\text{n为奇数}) \\ \frac{1}{(2i)^{n}} \sum_{k = 0}^{[\frac{n}{2}]} 2 (-1)^{k} C_{n}^{k} \cos ((n - 2k) \theta) & (\text{n为偶数}) \end{cases}
$$

特别地，对于 $n = 3$
$$
\cos^{3} \theta = \frac{1}{2^{2}} \sum_{k = 0}^{1} C_{3}^{k} \cos ((3 - 2k) \theta) = \frac{1}{4} (\cos (3 \theta) + 3 \cos \theta)
$$

$$
\sin^{3} \theta = \frac{1}{(2i)^{2}} \sum_{k = 0}^{1} (-1)^{k}  C_{3}^{k} \sin ((3 - 2k) \theta) = - \frac{1}{4} (\sin (3 \theta) - 3 \sin \theta)
$$

11 证明下列 Cauchy-Riemann 条件，其中 $w = u + iv = \rho e^{i\varphi}$，$z = x + iy = r e^{i\theta}$：

(a) 
$$
\frac{\partial u}{\partial r} = \frac{1}{r} \frac{\partial v}{\partial \theta}, \quad \frac{\partial v}{\partial r} = -\frac{1}{r} \frac{\partial u}{\partial \theta}
$$

考虑沿着径向的逼近方式：
$$
\lim_{\Delta z \to 0} \frac{\Delta w}{\Delta z} = \lim_{\Delta r \to 0} \frac{\Delta u + i \Delta v}{e^{i \theta} \Delta r} = \frac{\partial u}{\partial r} \cos \theta + \frac{\partial v}{\partial r} \sin \theta + i (\frac{\partial v}{\partial r} \cos \theta - \frac{\partial v}{\partial r} \sin \theta)
$$
再考虑沿着角向的逼近方式：
$$
\lim_{\Delta z \to 0} \frac{\Delta w}{\Delta z} = \lim_{\Delta \theta \to 0} \frac{\Delta u + i \Delta v}{r (i \cos \theta - \sin \theta) \Delta \theta} = \frac{1}{r} ((\frac{\partial v}{\partial \theta} \cos \theta - \frac{\partial u}{\partial \theta} \sin \theta) - i (\frac{\partial u }{\partial \theta} \cos \theta + \frac{\partial v}{\partial \theta} \sin \theta))
$$
对比上述二式，得到
$$
\frac{\partial u}{\partial r} \cos \theta + \frac{\partial v}{\partial r} \sin \theta =  \frac{1}{r} (\frac{\partial v}{\partial \theta} \cos \theta - \frac{\partial u}{\partial \theta} \sin \theta) \\
\frac{\partial v}{\partial r} \cos \theta - \frac{\partial v}{\partial r} \sin \theta = - \frac{1}{r} (\frac{\partial u }{\partial \theta} \cos \theta + \frac{\partial v}{\partial \theta} \sin \theta)
$$
即
$$
\frac{\partial u}{\partial r} = \frac{1}{r} \frac{\partial v}{\partial \theta}, \quad \frac{\partial v}{\partial r} = -\frac{1}{r} \frac{\partial u}{\partial \theta}
$$
14 已知函数 $f(z) = u + iv$ 在区域 $G$ 中解析，则对于常实数 $a$ 和 $b$，$au + bv$ 在区域中也解析的条件为什么？并据此证明若在 $G$ 中 $\text{Im}\, f(z) = 0$，则 $f(z)$ 为常函数。

也解析的条件：由于 $f (z)$ 解析，所以 $f(z)$ 的各个偏导数在区域 $G$ 中连续，即 $au + bv$ 的各个偏导数在区域 $G$ 中连续，所以 $au + bv$ 在区域中也解析的充要条件即为 Cauchy-Riemann 条件：
$$
a \frac{\partial u}{\partial x} + b \frac{\partial v}{\partial x} = \frac{\partial u}{\partial y} + b \frac{\partial v}{\partial y} = 0
$$
若在 $G$ 中 $\text{Im}\, f(z) = 0$，则 $v = 0$，即有
$$
\frac{\partial u}{\partial x} = \frac{\partial u}{\partial y} = 0
$$
由于由于 $f (z)$ 解析，所以在区域 $G$ 中$u \in C^{1}$，所以在区域 $G$ 中 $\mathrm{d} u = 0$

所以对于任意路径的积分有
$$
u (\mathbf{x}) - u(\mathbf{x}_{0}) = \int_{\mathbf{x}_{0}}^{\mathbf{x}} \mathrm{d}u =0
$$
即$f(z)$ 为常函数。





## 复变函数 第2次作业

Chasse_neige

#### 第二章习题 初等函数与多值函数

1.请证明下列等式

(b)
$$
\sin(z_1 + z_2) = \sin z_1 \cos z_2 + \cos z_1 \sin z_2
$$
$$
\cos(z_1 + z_2) = \cos z_1 \cos z_2 - \sin z_1 \sin z_2
$$

证明
$$
\sin(z_{1} + z_{2}) = \frac{e^{i (z_{1} + z_{2})} - e^{-i (z_{1} + z_{2})}}{2i} = \frac{(e^{i z_{1}} + e^{-i z_{1}}) (e^{i z_{2}} - e^{-i z_{2}}) + (e^{i z_{1}} - e^{-i z_{1}})(e^{i z_{2}} + e^{-i z_{2}})}{4i} \\ = 
\frac{e^{i z_{1}} + e^{-i z_{1}}}{2} \frac{e^{i z_{2}} - e^{-i z_{2}}}{2i} + \frac{e^{i z_{1}} - e^{-i z_{1}}}{2i} \frac{e^{i z_{2}} + e^{-i z_{2}}}{2} = \sin z_1 \cos z_2 + \cos z_1 \sin z_2
$$

$$
\cos (z_{1} + z_{2}) = \frac{e^{i (z_{1} + z_{2})} + e^{-i (z_{1} + z_{2})}}{2} = \frac{(e^{i z_{1}} + e^{-i z_{1}}) (e^{i z_{2}} + e^{-i z_{2}}) + (e^{i z_{1}} - e^{-i z_{1}})(e^{i z_{2}} - e^{-i z_{2}})}{4} \\ = 
\frac{e^{i z_{1}} + e^{-i z_{1}}}{2} \frac{e^{i z_{2}} + e^{-i z_{2}}}{2} - \frac{e^{i z_{1}} - e^{-i z_{1}}}{2i} \frac{e^{i z_{2}} - e^{-i z_{2}}}{2i} = \cos z_1 \cos z_2 - \sin z_1 \sin z_2
$$

(d)
$$
\cosh^2 z - \sinh^2 z = 1, \quad 1 - \tanh^2 z = \text{sech}^2 z
$$

证明
$$
\cosh^{2} z - \sinh^{2} z = \left(\frac{e^{z} + e^{-z}}{2}\right)^{2} - \left(\frac{e^{z} - e^{-z}}{2}\right)^{2} \\ =
\frac{e^{2z} + e^{-2z} + 2}{4} - \frac{e^{2z} + e^{-2z} - 2}{4} = 1
$$

$$
1 - \tanh^{2} z = 1 - \frac{\sinh^{2} z}{\cosh^{2} z} = \frac{\cosh^{2} z - \sinh^{2} z}{\cosh^{2} z} = \frac{1}{\cosh^{2} z} = \sech^{2} z
$$

(f)
$$
\frac{d}{dz} \sinh z = \cosh z, \quad \frac{d}{dz} \cosh z = \sinh z
$$
证明
$$
\frac{d}{dz} \sinh z = \frac{d}{dz} \frac{e^{z} - e^{-z}}{2} = \frac{e^{z} + e^{-z}}{2} = \cosh z
$$

$$
\frac{d}{dz} \cosh z = \frac{d}{dz} \frac{e^{z} + e^{-z}}{2} = \frac{e^{z} - e^{-z}}{2} = \sinh z
$$



2.请证明不等式 ($x$ 和 $y$ 均为实数)
$$
|\sinh y| \leq |\sin(x + iy)| \leq |\cosh y|
$$

$$
|\sinh y| \leq |\cos(x + iy)| \leq |\cosh y|
$$

证明
$$
\sin (x + iy) = \sin x \cosh y + i \cos x \sinh y
$$

$$
|\sin (x + iy)| = \sqrt{\sin^{2} x \cosh^{2} y + \cos^{2} x \sinh^{2} y}
$$

$$
\sqrt{\sin^{2} x \cosh^{2} y + \cos^{2} x \sinh^{2} y} = \sqrt{\sin^{2} x \cosh^{2} y + \cos^{2} x (\cosh^{2} y - 1)} \\ =
\sqrt{\cosh^{2} y - \cos^{2} x} \leq |\cosh y|
$$

$$
\sqrt{\sin^{2} x \cosh^{2} y + \cos^{2} x \sinh^{2} y} = \sqrt{\sin^{2} x (1 + \sinh^{2} y) + \cos^{2} x \sinh^{2} y} \\ =
\sqrt{\sin^{2} x + \sinh^{2} y} \geq |\sinh y|
$$

$$
\therefore \,\, |\sinh y| \leq |\sin(x + iy)| \leq |\cosh y|
$$

$$
\cos (x + iy) = \cos x \cosh y - i \sin x \sinh y
$$

$$
|\cos (x + iy)| = \sqrt{\cos^{2} x \cosh^{2} y + \sin^{2} x \sinh^{2} y}
$$

$$
\sqrt{\cos^{2} x \cosh^{2} y + \sin^{2} x \sinh^{2} y} = \sqrt{\cos^{2} x \cosh^{2} y + \sin^{2} x (\cosh^{2} y - 1)} \\ =
\sqrt{\cosh^{2} y - \sin^{2} x} \leq |\cosh y|
$$

$$
\sqrt{\cos^{2} x \cosh^{2} y + \sin^{2} x \sinh^{2} y} = \sqrt{\cos^{2} x (1 + \sinh^{2} y) + \sin^{2} x \sinh^{2} y} \\ =
\sqrt{\cos^{2} x + \sinh^{2} y} \geq |\sinh y|
$$

$$
\therefore \,\, |\sinh y| \leq |\cos(x + iy)| \leq |\cosh y|
$$

4.判断下列函数是否为多值函数, 若为多值函数, 请分析其支点的情况

(1) $\sqrt{1 - z^3}$

是多值函数

可能支点：$z = 1, z = - \frac{1}{2} + \frac{\sqrt{3}}{2} i, - \frac{1}{2} - \frac{\sqrt{3}}{2} i, z = \infty$

判断

1. $z=1$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点
2. $z = - \frac{1}{2} + \frac{\sqrt{3}}{2} i$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点
3. $z = - \frac{1}{2} - \frac{\sqrt{3}}{2} i$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点
4. 无穷远点：此时$z$绕行一圈后$w$ 的辐角变化$3 \pi$，是支点

(2) $\sqrt[3]{z^2 - 1}$

是多值函数

可能支点：$z = 1, z = -1, z = \infty$

判断

1. $z = 1$：此时$z$绕行一圈后$w$ 的辐角变化$\frac{2}{3} \pi$，是支点
2. $z = - 1$：此时$z$绕行一圈后$w$ 的辐角变化$\frac{2}{3} \pi$，是支点
3. 无穷远点：此时$z$绕行一圈后$w$ 的辐角变化$\frac{4}{3} \pi$，是支点

(3) $\sqrt{\cos z}$

是多值函数

可能支点：$\cos z = 0$，即 $z = \frac{\pi}{2} + k \pi$

判断

$z = \frac{\pi}{2} + k \pi \quad (k \in \mathbb{Z})$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点# 复变函数 第3次作业

吴桐 2024012555

4.判断下列函数是否为多值函数, 若为多值函数, 请分析其支点的情况

(1) $\sqrt{1 - z^3}$

是多值函数

可能支点：$z = 1, z = - \frac{1}{2} + \frac{\sqrt{3}}{2} i, - \frac{1}{2} - \frac{\sqrt{3}}{2} i, z = \infty$

判断

1. $z=1$：此时$z$绕行一圈后$w$ 的辐角变化 $\pi$，是支点
2. $z = - \frac{1}{2} + \frac{\sqrt{3}}{2} i$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点
3. $z = - \frac{1}{2} - \frac{\sqrt{3}}{2} i$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点
4. 无穷远点：此时$z$绕行一圈后$w$ 的辐角变化$3 \pi$，是支点

(2) $\sqrt[3]{z^2 - 1}$

是多值函数

可能支点：$z = 1, z = -1, z = \infty$

判断

1. $z = 1$：此时$z$绕行一圈后$w$ 的辐角变化$\frac{2}{3} \pi$，是支点
2. $z = - 1$：此时$z$绕行一圈后$w$ 的辐角变化$\frac{2}{3} \pi$，是支点
3. 无穷远点：此时$z$绕行一圈后$w$ 的辐角变化$\frac{4}{3} \pi$，是支点

(3) $\sqrt{\cos z}$

是多值函数

可能支点：$\cos z = 0$，即 $z = \frac{\pi}{2} + k \pi$

判断

$z = \frac{\pi}{2} + k \pi \quad (k \in \mathbb{Z})$：此时$z$绕行一圈后$w$ 的辐角变化$\pi$，是支点

(6)$\frac{\sin \sqrt{z}}{\sqrt{z}}$

是多值函数

可能支点：$\sin \sqrt{z} = 0$，即$z = k^{2} \pi^{2}$

判断

1. $z = 0$ ： 此时 $z$ 绕行一圈之后 $w$ 的辐角变化为 $0$ ，不是支点
2. $z = k^{2} \pi^{2} \quad (k \neq 0)$ ： 此时 $z$ 绕行一圈之后 $w$ 的辐角变化为 $\pi$ ，是支点

5.函数 $w (z) = z + \sqrt{z - 1}$, 规定 $w(2) =1$, 试分别求当 $z$ 沿着图中 $C1$ 和 $C2$连续变化时 $w(−3)$ 的值

<img src="/Users/wutong/Library/Application Support/typora-user-images/image-20250425155000791.png" alt="image-20250425155000791" style="zoom:50%;" />

函数支点为 $z = 1$ 以及无穷远点，由于 $w (2) = 1$，所以函数在 $x$ 轴正半轴上辐角为 $2 \pi$

$z$ 沿着图中 $C1$ 变化时
$$
w (-3) = 3 e^{i 3 \pi} + |\sqrt{-3 - 1}| e^{i \frac{3 \pi}{2}} = -3 - 2 i
$$
$z$ 沿着图中 $C2$ 变化时 
$$
w(-3) = 3 e^{i \pi} + |\sqrt{-3 -1}| e^{i \frac{\pi}{2}} = -3 + 2i
$$
7.函数 $\ln \frac{1 - z}{1 + z}$, 规定 $w(0) = 0$, 试讨论当 $z$ 分别限制在图 $(a)$ 和 $(b)$ 中变化时, $w(3)$ 为多少? $w(∞)$ 又是多少?

<img src="/Users/wutong/Library/Application Support/typora-user-images/image-20250425160157331.png" alt="image-20250425160157331" style="zoom:50%;" />

当 $z$ 限制在图 $(a)$  中变化时
$$
w (3) = \ln \left( \left| \frac{1 - 3}{1 + 3} \right| e^{i (\pi - 0)} \right) = - \ln 2 + i \pi
$$

$$
w (\infty) = \ln \left( \left| -1 \right| e^{i \pi} \right) = i \pi
$$

当 $z$ 限制在图 $(b)$  中变化时
$$
w (3) = \ln \left( \left| \frac{1 - 3}{1 + 3} \right| e^{i (- \pi - 0)} \right) = - \ln 2 - i \pi
$$

$$
w (\infty) = \ln ( \left| -1 \right| e^{- i \pi}) = - i \pi
$$

8.设 $ f(z)=\dfrac{z^{1-p}(1-z)^p}{2 z }$ ， $-1 < p < 2$ ，取割线为实轴上从 $0$ 到 $1$ 的线段，且割线上岸辐角为 $0$ 。试求 $f(\pm \mathrm{i})$ ， $ f(\infty)$  
$$
f  (i) = \left| \frac{i^{1 - p} (1 - i)^{p}}{2 i} \right| e^{i ((1 - p) \frac{\pi}{2}- p \frac{\pi}{4} - \frac{\pi}{2})} = 2^{\frac{p}{2} - 1} e^{- i p \frac{3 \pi}{4}}
$$

$$
f  (- i) = \left| \frac{(-i)^{1 - p} (1 + i)^{p}}{- 2 i} \right| e^{i ((1 - p) \frac{3 \pi}{2} + p \frac{\pi}{4} - \frac{3 \pi}{2})} = 2^{\frac{p}{2} - 1} e^{- i p \frac{5 \pi}{4}}
$$

$$
f (\infty) = \left| \frac{1}{2} \right| e^{i (p (- \pi) - 0)} = \frac{1}{2} e^{- i p \pi}
$$# 复变函数 第4次作业

Chasse_neige

2.请计算如下积分

（1）
$$
\int_{|z|=1} \frac{\text{d}z}{z}
$$

$$
\int_{|z| = 1} \frac{d z}{z} = 2 \pi i
$$

（2）
$$
\int_{|z|=1} \frac{\text{d}z}{|z|}
$$

$$
\int_{|z| = 1} \frac{d z}{|z|} = \int_{|z|  = 1} d z = 0
$$

（3）
$$
\int_{|z|=1} \frac{|\text{d}z|}{z}
$$

$$
\int_{|z| = 1} \frac{|d z|}{z} = \int_{|z| = 1} \frac{d \theta}{e^{i \theta}} = 0
$$

（4）
$$
\int_{|z|=1} \left|\frac{\text{d}z}{z}\right|
$$

$$
\int_{|z| = 1} \left| \frac{d z}{z} \right| = \int_{|z| = 1} d \theta = 2 \pi
$$

5.计算下列积分

（1）
$$
\oint_{|z|=2} \frac{\cos z}{z} \text{d}z
$$

$$
\oint_{|z| = 2} \frac{\cos z}{z} d z = 2 \pi i \cos (0) = 2 \pi i
$$

（2）
$$
\oint_{|z|=2} \frac{\sin z}{z^2} \text{d}z
$$

$$
\oint_{|z| = 2} \frac{\sin z}{z^{2}} d z = \frac{2 \pi i }{1 !} \sin' (0) = 2 \pi i
$$

（3）
$$
\oint_{|z|=2} \frac{\text{e}^z}{z^3} \text{d}z
$$

$$
\oint_{|z| = 2} \frac{e^{z}}{z^{3}} d z = \frac{2 \pi i}{2!} e''^{0} = \pi i
$$

（4）
$$
\oint_{|z|=2} \frac{|z|\text{e}^z}{z^2} \text{d}z
$$

$$
\oint_{|z| = 2} \frac{|z| e^{z}}{z^{2}} dz = 2 \oint_{|z| = 2} \frac{e^{z}}{z^{2}} d z = 2 \cdot 2 \pi i e'^{0} = 4 \pi i
$$

6.对于什么样的 $a$ 值，函数
$$
F(z) = \int_{z_0}^z \text{e}^z \left(\frac{1}{z} + \frac{a}{z^3}\right) \text{d}z
$$

是单值的。
$$
\oint e^{z} \left( \frac{1}{z} + \frac{a}{z^{3}} \right) d z = 0
$$
即可保证该函数的单值性

当环路内包括$z = 0$ 时
$$
\oint e^{z} \left( \frac{1}{z} + \frac{a}{z^{3}} \right) d z  = 2 \pi i(e^{0} + \frac{1}{2!} a e'^{0}) = 0
$$
所以 $a = -2$ 

当环路内不包括 $z = 0$ 时
$$
\oint e^{z} \left( \frac{1}{z} + \frac{a}{z^{3}} \right) d z   = 0 + 0 = 0
$$
综上，$a = -2$

8.设 $f(z)$ 在一个包含圆域 $|z| \leq R$ 的区域中解析，$\zeta = r \text{e}^{\text{i}\theta}$ 为圆内一点，$0 \leq r < R$，证明下式（Poisson 公式）成立
$$
f(\zeta) = \frac{1}{2\pi} \int_0^{2\pi} \frac{R^2 - r^2}{R^2 - 2Rr \cos(\theta - \phi) + r^2} f\left(R \text{e}^{\text{i}\phi}\right) \text{d} \phi
$$
证明：设$z = R e^{i \phi}$
$$
\frac{1}{2\pi} \int_0^{2\pi} \frac{R^2 - r^2}{R^2 - 2Rr \cos(\theta - \phi) + r^2} f\left(R \text{e}^{\text{i}\phi}\right) \text{d} \phi  \\  = 
\frac{1}{2 \pi} \oint_{|z| = R} \frac{R^{2} - r^{2}}{|\zeta - z|^{2}} f (\zeta) \frac{1}{i z} d z \\ = 
- i \frac{R^{2} - r^{2}}{2 \pi} \oint_{|z| = R} \frac{f (z)}{z (z- \zeta)(\frac{R^{2}}{z} - \frac{r^{2}}{\zeta})} dz \\ = 
i \frac{R^{2} - r^{2}}{2 \pi} \oint_{|z| = R} \frac{ \frac{\zeta}{r^{2}} f (z)}{(z- \zeta)(z - \frac{R^{2}}{r^{2}} \zeta)} dz \\ =
i \frac{R^{2} - r^{2}}{2 \pi} \frac{\zeta}{r^{2}} \left( 2 \pi i \frac{f (\zeta)}{\zeta (1 - \frac{R^{2}}{r^{2}})} \right)  = f (\zeta)
$$
## 复变函数 第5次作业

Chasse_neige

1.$\sum_{n=1}^{\infty} a_n$ 与 $\sum_{n=1}^{\infty} b_n$ 均为正项级数，下列说法是否正确？若正确，请给出证明；若不正确，试举反例说明之。

(a) 若 $\lim_{n\to\infty} n a_n = 0$，则 $\sum_{n=1}^{\infty} a_n$ 收敛；

不正确

取$a_{n} = \frac{1}{n \ln n}$

由Cauchy反常积分判别法，原级数的收敛发散性质与积分
$$
\int_{1}^{\infty} \frac{1}{n \ln n} dn = \int_{0}^{\infty} \frac{d u}{u}
$$
相同，所以级数发散

(b) 若 $a_{2n} < a_{2n+1}$，则 $\sum_{n=1}^{\infty} a_n$ 发散；

不正确
$$
a_{2} = \frac{1}{100} \\
a_{2n} = \frac{1}{(2 n)^{3}} \quad (n \neq 1)\\ 
a_{2n + 1} = \frac{1}{(2n + 1)^{2}}
$$
此时$a_{2n} < a_{2n + 1}$，但是
$$
\sum_{n = 1}^{\infty} a_{n} < \sum_{n = 1}^{\infty} \frac{1}{n^{2}} = \frac{\pi^{2}}{6}
$$
由比较定理， $\sum_{n=1}^{\infty} a_n$ 收敛

(c) 若 $\lim_{n\to\infty} \frac{a_{2n+1}}{a_{2n}} = \infty$，则 $\sum_{n=1}^{\infty} a_n$ 发散；

不正确
$$
a_{2n} = \frac{1}{(2 n)^{3}} \\ 
a_{2n + 1} = \frac{1}{(2n + 1)^{2}}
$$

$$
\lim_{n \to \infty} \frac{a_{2n + 1}}{a_{2n}} = \lim_{n \to \infty} \frac{(2n)^{3}}{(2n + 1)^{2}} = \infty
$$

但是
$$
\sum_{n = 1}^{\infty} a_{n} < \sum_{n = 1}^{\infty} \frac{1}{n^{2}} = \frac{\pi^{2}}{6}
$$
由比较定理， $\sum_{n=1}^{\infty} a_n$ 收敛

(d) 若 $\sum_{n=1}^{\infty} a_n$ 与 $\sum_{n=1}^{\infty} b_n$ 发散，则 $\sum_{n=1}^{\infty} \sqrt{a_n b_n}$ 发散。

不正确，反例
$$
a_{2n} = \frac{1}{2n}, \qquad a_{2n + 1} = \frac{1}{(2n + 1)^{2}} \\
b_{2n} = \frac{1}{(2n)^{2}}, \qquad b_{2n + 1} = \frac{1}{2n + 1}
$$
此时
$$
\sqrt{a_{n} b_{n}}  = \frac{1}{n^{\frac{3}{2}}}
$$
$\sum_{n=1}^{\infty} \sqrt{a_n b_n}$ 收敛。

2.判断下列级数的收敛性以及绝对收敛性
(1) $\sum_{n=2}^{\infty} \frac{i^n}{\ln n}$；

由狄利克雷判别法

$\frac{1}{\ln n}$ 单调递减且趋于0，并且部分和
$$
|\sum_{n} i^{n}| = |i - 1 - i + 1 + \cdots| < \sqrt{2}
$$
所以该级数收敛

但是
$$
|\frac{i^{n}}{\ln n}| = \frac{1}{\ln n} > \frac{1}{n}
$$
由于调和级数发散，由比较判别法，原级数并非绝对收敛。

(2) $\sum_{n=1}^{\infty} \frac{i^n}{n}$

$\frac{1}{ n}$ 单调递减且趋于0，并且部分和
$$
|\sum_{n} i^{n}| = |i - 1 - i + 1 + \cdots| < \sqrt{2}
$$
所以该级数收敛

但是
$$
|\frac{i^{n}}{n}| = \frac{1}{n}
$$
由于调和级数发散，所以原级数并非绝对收敛。

(3) $\sum_{n=1}^{\infty} \frac{\sin(n\pi/6)}{n^2}$

$\frac{1}{n^{2}}$ 单调递减且趋于0，并且部分和
$$
|\sum_{k = 1}^{n} \sin (\frac{k \pi}{6})| = \left| \frac{\cos (\frac{\pi}{12}) - \cos{(n + \frac{1}{2}}) \frac{\pi}{6}}{2 \sin \frac{\pi}{12}} \right| \leq  \frac{\cos (\frac{\pi}{12}) + 1}{2 \sin \frac{\pi}{12}}
$$
所以该级数收敛
$$
\left|  \frac{\sin(\frac{n \pi}{6})}{n^2}\right| \leq \frac{1}{n^{2}}
$$
由比较定理，该级数绝对收敛

3.证明级数
$$
\sum_{n=1}^{\infty} \frac{z^{n-1}}{\left(1-z^n\right)\left(1-z^{n+1}\right)}, \quad |z| \neq 1
$$
收敛，并求其和。
提示：$z^{n-1} = \frac{z^n - z^{n+1}}{z(1-z)}$

证明

当$|z| < 1$ 时
$$
\left| \frac{z^{n-1}}{\left(1-z^n\right)\left(1-z^{n+1}\right)} \right| \leq \frac{|z|^{n - 1}}{(1 - |z|)^{2}}
$$
因为$|z| < 1$，由比较定理，原级数绝对收敛，可以进行裂项

当 $|z| > 1$ 时
$$
\left| \frac{z^{n-1}}{\left(1-z^n\right)\left(1-z^{n+1}\right)} \right| \leq \frac{|z|^{n - 1}}{(|z|^{n} - 1) (|z|^{n + 1} - 1)} = \frac{|z|^{n - 1}}{|z|^{2n + 1} - |z|^{n + 1} - |z|^{n}} \\
\leq \frac{1}{ |z|^{n + 2} - |z|^{2} - |z|} \leq \frac{1}{|z|} \frac{1}{|z|^{n + 1} - 2 |z|} = \frac{1}{|z|^{2}} \frac{1}{|z|^{n} - 2}
$$
由比较定理，原级数绝对收敛，可以进行裂项
$$
\sum_{n=1}^{\infty} \frac{z^{n-1}}{\left(1-z^n\right)\left(1-z^{n+1}\right)} = \sum_{n=1}^{\infty} \frac{z^n - z^{n+1}}{\left(1-z^n\right)\left(1-z^{n+1}\right) z(1-z)} \\ = 
\sum_{n = 1}^{\infty} \frac{1}{z (1 - z)} \left(\frac{1}{1 - z^{n}} - \frac{1}{1 - z^{n + 1}} \right) \\ = 
\begin{cases} 
\frac{1}{z (1 - z)^{2}} \qquad (|z| > 1) \\ 
\frac{1}{(1 - z)^{2}} \qquad (|z| < 1)
\end{cases}
$$
## 复变函数 第6次作业

Chasse_neige

5.试确定下列级数的收敛半径（或收敛区域）

(1) 
$$
\sum_{n=1}^{\infty} \frac{z^n}{n^n}
$$

$$
c_{n} = \frac{1}{n^{n}}
$$

$$
R = \lim_{n \to \infty}  \frac{1}{\sup (c_{n})^{\frac{1}{n}}} = \lim_{n \to \infty} n  = \infty
$$

对于任意 $z$ ，当 $n > 2 |z|$  时
$$
\left|\frac{z^{n}}{n^{n}}\right| < \frac{1}{2}^{n}
$$
由比较判别法，该级数绝对收敛

所以该级数在 $\mathbb{C}$ 上收敛

(2) 
$$
\sum_{n=1}^{\infty} \frac{n!}{n^n} z^n
$$

$$
c_{n} = \frac{n!}{n^{n}}
$$

根据达朗贝尔判别法
$$
R = \lim_{n \to \infty} \left| \frac{c_{n}}{c_{n + 1}} \right| = \lim_{n \to \infty} \left| \frac{n + 1}{n}^{n} \right| = \lim_{n \to \infty} (1 + \frac{1}{n})^{n} = e
$$


7.证明级数 
$$
\sum_{n=0}^{\infty} \left(\frac{z^{n+1}}{n+1} - \frac{2z^{2n+3}}{2n+3}\right)
$$
的和函数在 $z=1$ 点不连续

证明

在  $z=1$ 点，级数
$$
\sum_{n=0}^{\infty} \left(\frac{z^{n+1}}{n+1} - \frac{2z^{2n+3}}{2n+3}\right) = \sum_{n = 0}^{\infty} \frac{1}{(n + 1) (2n + 3)} \leq \sum_{n = 0}^{\infty} \frac{1}{2} \frac{1}{n^{2}}
$$
收敛

所以在 $|z| < 1$ 上该级数绝对收敛，在该开区间上
$$
S (z) = \sum_{n=0}^{\infty} \left(\frac{z^{n+1}}{n+1} - \frac{2z^{2n+3}}{2n+3}\right) = \ln (1 - z) - \ln (\frac{1 + z}{1 - z}) + 2z = 2z - \ln (1 + z)
$$
所以从收敛圆内趋近于该点的极限
$$
\lim_{z \to 1} S (z) = 2 - \ln 2
$$
该点的级数收敛于
$$
\sum_{n = 0}^{\infty} \frac{1}{(n + 1) (2n + 3)} = 2 \sum_{n = 0}^{\infty} \frac{1}{2n + 2} - \frac{1}{2n + 3} = 2 (1 - \ln 2) = 2 - 2 \ln 2 
$$
所以该点和函数不连续

这与阿贝尔第二定理并不矛盾，因为阿贝尔第二定理只对单一幂级数成立。

如果一定要把这个级数的和函数在该点的极限表示出来，那么实际上应该写为
$$
S (z) = \ln (1 - z) - \ln (\frac{1 + z}{1 - z}) + 2z
$$
的形式，该点是两个发散值的抵消，会造成奇异性。

8.求下列级数的和

(1) 
$$
\sum_{n=1}^{\infty} \frac{\cos n\theta}{n}, \quad 0 < \theta < 2\pi
$$
判断收敛性

因为 $\frac{1}{n}$ 递减切趋于0

又因为 $\cos n \theta$ 部分和
$$
\sum_{n = 1}^{\infty} \cos n \theta = \frac{\sin (n + \frac{1}{2}) \theta - \sin \frac{1}{2} \theta }{2 \sin \frac{\theta}{2}}
$$
有界，所以原级数收敛
$$
\sum_{n=1}^{\infty} \frac{\cos n\theta}{n} = \Re \left[\sum_{n = 1}^{\infty} \frac{e^{i n \theta}}{n} \right] \\ = 
- \Re [\ln (1 - e^{i \theta})] = - \frac{1}{2} \ln (2 - 2 \cos \theta) = - \ln (2 \sin \frac{\theta}{2})
$$
(3) 
$$
\sum_{n=0}^{\infty} \frac{\cos (2n+1)\theta}{2n+1}, \quad 0 < \theta < \pi
$$
由于(1)中的级数收敛，由比较定理，此级数收敛
$$
\sum_{n=0}^{\infty} \frac{\cos (2n+1)\theta}{2n+1} = \Re \left[\sum_{n = 1}^{\infty} \frac{e^{i (2n + 1) \theta}}{2n + 1}\right] = \frac{1}{2} \Re[\ln (1 + e^{i \theta}) - \ln (1 - e^{i \theta})] \\ = 
\frac{1}{4} (\ln (2 + 2 \cos \theta) - \ln (2 - 2 \cos \theta)) = \frac{1}{2} \ln (\cot \frac{\theta}{2})
$$
(5) 
$$
\sum_{n=0}^{\infty} \frac{(-1)^n \sin (2n+1)\theta}{(2n+1)^2}, \quad -\pi/2 \leq \theta \leq \pi/2
$$
证明收敛性
$$
\left|\frac{(-1)^n \sin (2n+1)\theta}{(2n+1)^2}\right| \leq \frac{1}{(2n + 1)^{2}}
$$
由于级数 $\sum_{n} \frac{1}{n^{2}}$ 收敛，所以该级数绝对收敛
$$
\sum_{n=0}^{\infty} \frac{(-1)^n \sin (2n+1)\theta}{(2n+1)^2} = \sum_{n = 0}^{\infty} \int_{0}^{\theta} \frac{(-1)^{n} \cos (2n + 1) \theta}{2n + 1} d \theta \\ = 
\int_{0}^{\theta} \left(\sum_{0}^{\infty} \frac{(-1)^{n} \cos (2n + 1) \theta}{2n + 1} \right) d \theta = \int_{0}^{\theta} \frac{\pi}{4} \text{sgn} (\cos \theta) d \theta = \frac{\pi}{4} \theta
$$
1.将下列函数在指定点展开成 Taylor 级数，并给出收敛半径

(a) $1-z^3$ 在 $z=1$ 展开
$$
1 - z^{3} = -3 (z - 1) - 3 (z - 1)^{2} -  (z - 1)^{3}
$$
收敛半径为 $\infty$

(b) $$\frac{1}{1+z+z^2}$$ 在 $z=0$ 展开
$$
\frac{1}{1 + z + z^{2}} = \frac{1}{\sqrt{3} i} \left( \frac{1}{z + \frac{1 - \sqrt{3} i}{2}} - \frac{1}{z + \frac{1 + \sqrt{3} i}{2}} \right) \\ = 
\frac{1}{\sqrt{3} i} \left( \frac{1 + \sqrt{3} i}{2} \sum_{n = 0}^{\infty} (- \frac{1 + \sqrt{3} i}{2} z)^{n} - \frac{1 - \sqrt{3} i}{2} \sum_{n = 0}^{\infty} (- \frac{1 - \sqrt{3} i}{2} z)^{n} \right) \\ =
\sum_{n = 0}^{\infty} \left( \frac{3 - \sqrt{3} i}{6}  (- \frac{1 + \sqrt{3} i}{2})^{n} + \frac{3 + \sqrt{3} i}{6} (- \frac{1 - \sqrt{3} i}{2})^{n} \right) z^{n}
$$
收敛半径为 $1$

(c) $\frac{\sin z}{1 - z}$ 在 $z = 0$ 展开
$$
\frac{\sin z}{1 - z} = \sum_{k =0}^{\infty} \sum_{l = 0}^{\infty} \frac{(-1)^{k}}{(2 k + 1)!} z^{2k + 1} z^{l} \\ = 
\sum_{k =0}^{\infty} \sum_{l = 0}^{\infty} \frac{(-1)^{k}}{(2 k + 1)!} z^{2k + l + 1} \\ = 
\sum_{n = 0}^{\infty} \left(\sum_{k = 0}^{[\frac{n - 1}{2}]} \frac{(-1)^{k}}{(2 k + 1)!} \right) z^{n} 
$$
收敛半径为 $1$# 复变函数 第7次作业

Chasse_neige

1.将下列函数在指定点展开成 Taylor 级数, 并给出收敛半径

(e) 
$$
\sec z
$$
 在 $z = 0$ 展开

使用待定系数法
$$
\cos z = \sum_{n = 0}^{\infty} \frac{(-1)^{n}}{(2n)!} z^{2n}
$$
所以
$$
1 = \sum_{l = 0}^{\infty} \sum_{k = 0}^{\infty} \frac{(-1)^{l}}{(2l)!} a_{2k} z^{2l + 2k} = \sum_{n = 0}^{\infty} \sum_{k = 0}^{n} \frac{(-1)^{n - k}}{(2(n - k))!} a_{2k} z^{2n}
$$
所以
$$
\sum_{k = 0}^{n} \frac{(-1)^{n - k}}{(2(n - k))!} a_{2k} = \begin{cases} 1 \qquad (n = 0) \\ 0 \qquad (n \neq 0) \end{cases}
$$

$$
a_{0} = 1
$$

Taylor 系数可以通过一下递推式得出
$$
a_{2n} = \sum_{k = 0}^{n - 1} \frac{(-1)^{n - k + 1}}{(2 (n - k))!} a_{2k}
$$
前几项为
$$
a_{0} = 1, a_{2} = \frac{1}{2}, a_{4} = \frac{5}{24}, a_{6} = \frac{61}{720}
$$
收敛半径为 $ \frac{\pi}{2} $

2.将下列函数在指定点展开成 Taylor 级数, 并给出收敛半径

(b) 将
$$
\ln \frac{1 + z}{1 - z}
$$
在 $z = \infty$ 展开

支点为 $z = 1$ 和 $z = -1$

假设割线为从 $z = 1$ 沿 $x$ 方向延伸到无穷远，在从 $-x$ 方向从无穷远延伸到 $z = -1$ ，并且在割线上岸 $\arg (\frac{1 + z}{1 - z}) = \pi$
$$
\ln (1 + z) = \sum_{n = 1}^{\infty} \frac{(-1)^{n + 1}}{n} z^{n}
$$

$$
\ln (1 - z)  = - \sum_{n = 1}^{\infty}  \frac{1}{n} z^{n}
$$

所以
$$
\ln \frac{1 + z}{1 - z} = \sum_{n = 0}^{\infty} \frac{2}{2n + 1} z^{2n + 1}
$$
收敛半径为 $1$

(c) 将 
$$
\sqrt{\frac{1-z}{1+z}}
$$
在 $z = 0$ 以及 $z = \infty$ 处展开

在 $z = 0$ 处

支点为 $z = 1$ 和 $z = -1$

假设割线为从 $z = 1$ 沿 $x$ 方向延伸到无穷远，在从 $-x$ 方向从无穷远延伸到 $z = -1$ ，并且在割线上岸 $\arg (\frac{1 - z}{1 + z}) = - \pi$
$$
\sqrt{\frac{1-z}{1+z}} = (1 - z) (1 - z^{2})^{- \frac{1}{2}} = (1 - z) \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ - \frac{1}{2} \end{pmatrix} z^{2n} = \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ - \frac{1}{2} \end{pmatrix} (z^{2n} - z^{2n + 1})
$$
收敛半径为 $1$

在 $z = \infty$ 处

支点为 $z = 1$ 和 $z = -1$

割线为从 $z = -1$ 到 $z = 1$ 沿 $x$ 轴的连线，并且在割线上岸 $\arg (\frac{1 - z}{1 + z}) = 0 $
$$
\sqrt{\frac{1-z}{1+z}} = \sqrt{\frac{\frac{1}{z} - 1}{\frac{1}{z} + 1}} = i (\frac{1}{z} - 1) (1 - \frac{1}{z^{2}})^{- \frac{1}{2}} = i (\frac{1}{z} - 1) \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ - \frac{1}{2} \end{pmatrix} \frac{1}{z}^{2n} \\ = 
i \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ - \frac{1}{2} \end{pmatrix} (\frac{1}{z}^{2n + 1} - \frac{1}{z}^{2n})
$$
收敛半径为 $\left|\frac{1}{z}\right| < 1$

(d) 将  
$$
\frac{z^{(1-p)}(1-z)^p}{2z}
$$
在 $z = \infty$ 处展开，其中 $ -1 < p < 2 $  

支点为 $z = 0$ 和 $z = 1$ 

划分割线为从 $z = 0$ 沿着 $x$ 轴指向 $z = 1$ 的连线，并且在割线上岸 $\arg \frac{1 - z}{z} = 0$
$$
\frac{(1 - z)^{p}}{2 z^{p}} = e^{-i p \pi} \frac{1}{2} \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ p \end{pmatrix} \frac{1}{z}^{n} = e^{-i p \pi} \sum_{n = 0}^{\infty}  \frac{(-1)^{n}}{2} \begin{pmatrix} n \\ p \end{pmatrix} \frac{1}{z}^{n}
$$
收敛半径为 $\left|\frac{1}{z}\right| < 1$

3.验证等式  
$$
\sum_{n=0}^\infty \frac{(-1)^n}{a + nb} = \int_0^1 \frac{t^{a-1}}{1 + t^b} dt, \quad a, b > 0
$$

证明
$$
\int_0^1 \frac{t^{a-1}}{1 + t^b} dt = \int_{0}^{1} \sum_{n = 0}^{\infty} (-1)^{n} t^{nb + a - 1} dt \\ = 
\sum_{n = 0}^{\infty} \int_{0}^{1} (-1)^{n} t^{nb + a - 1} dt = \sum_{n=0}^\infty \frac{(-1)^n}{a + nb}
$$
据此求出以下级数之和：  

(a)  
$$
1 - \frac{1}{4} + \frac{1}{7} - \frac{1}{10} + \cdots
$$

$$
\sum_{n = 0}^{\infty} \frac{(-1)^{n}}{1 + 3n} = \int_{0}^{1} \frac{1}{1 + t^{3}} dt = \frac{\sqrt{3} \pi + \ln 8}{9}
$$

(b)  
$$
\frac{1}{2} - \frac{1}{5} + \frac{1}{8} - \frac{1}{11} + \cdots
$$

$$
\sum_{n = 0}^{\infty} \frac{(-1)^{n}}{2 + 3n} = \int_{0}^{1} \frac{t}{1 + t^{3}} dt =  \frac{\sqrt{3} \pi - \ln{8}}{9}
$$

(c)  
$$
1 - \frac{1}{5} + \frac{1}{9} - \frac{1}{13} + \cdots
$$

$$
\sum_{n = 0}^{\infty} \frac{(-1)^{n}}{1 + 4n} = \int_{0}^{1} \frac{1}{1 + t^{4}} dt = \frac{\pi + 2\coth^{-1} (\sqrt{2}) }{4 \sqrt{2}}
$$

## 复变函数 第8次作业

Chasse_neige

1.求将下列函数的 Laurent 展开  

(a)  
$$
\frac{1}{z^2(z-1)}  
$$
在 $z=1$ 附近以及 $|z-1|>1$ 展开

在 $z=1$ 附近 ($0 < |z - 1| < 1$) 展开


$$
\frac{1}{z^{2} (z - 1)} = \frac{1}{z - 1} \frac{1}{(1 + (z - 1))^{2}} = \frac{1}{z - 1} \sum_{n = 0}^{\infty} \begin{pmatrix} n \\ -2 \end{pmatrix} (z - 1)^{n} = \sum_{n = -1}^{\infty}  \begin{pmatrix} n + 1 \\ -2 \end{pmatrix} (z - 1)^{n}
$$

在$|z-1|>1$ 展开
$$
\frac{1}{z^{2} (z - 1)} = \frac{1}{(z - 1)^{3}} \frac{1}{(1 + \frac{1}{z - 1})^{2}} = \frac{1}{(z - 1)^{3}} \sum_{n = 0}^{\infty} \begin{pmatrix} n \\ -2 \end{pmatrix} (z - 1)^{-n} = \sum_{n = 0}^{\infty}  \begin{pmatrix} n \\ -2 \end{pmatrix} (z - 1)^{- n - 3}
$$
(b)   
$$
\frac{1}{z^2 - 3z + 2}
$$
在 $1 < |z| < 2$ 以及 $|z| > 2$ 区域内展开

在 $1 < |z| < 2$ 上展开
$$
\frac{1}{z^{2} - 3z + 2} = \frac{1}{(z - 1) (z - 2)} = - \frac{1}{z - 1} \frac{1}{1 - (z - 1)} \\ =
- \frac{1}{z - 1} \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ -1 \end{pmatrix} (z - 1)^{n} \\ =
\sum_{n = -1}^{\infty} (-1)^{n}  \begin{pmatrix} n + 1 \\ -1 \end{pmatrix} (z - 1)^{n}
$$
在 $|z| > 2$ 区域内展开
$$
\frac{1}{z^{2} - 3z + 2} = \frac{1}{(z - 1) (z - 2)} = \frac{1}{(z - 1)^{2}} \frac{1}{1 - \frac{1}{(z - 1)}} \\ =
\frac{1}{(z - 1)^{2}} \sum_{n = 0}^{\infty} (-1)^{n} \begin{pmatrix} n \\ -1 \end{pmatrix} (z - 1)^{- n} \\ =
\sum_{n = 0}^{\infty} (-1)^{n}  \begin{pmatrix} n \\ -1 \end{pmatrix} (z - 1)^{- n - 2}
$$
(e)  
$$
\ln^{-1} \frac{1 + z}{1 - z}
$$
在 $z = 0$ 以及 $z = \infty$ 的邻域在不同单位分支内的展开，割线为 $|z| = 1$ 的下半圆弧

支点为 $z = -1$ 以及 $z = 1$，割线为 $|z| = 1$ 的下半圆弧，假设 $z = -1$ 到 $z = 1$ 连线上宗量辐角为 $2 k \pi， (k \in \mathbb{Z})$  ，此时
$$
\ln^{-1} \frac{1 + z}{1 - z} = \frac{1}{\ln \frac{1 + z}{1 - z}} = \frac{1}{i 2 k \pi + \sum_{n = 1}^{\infty} \frac{(-1)^{n + 1}}{n} z^{n} + \frac{1}{n} z^{n}}
$$
在$z = 0$ 邻域内

当$k = 0$ 时
$$
\ln^{-1} \frac{1 + z}{1 - z} = \frac{1}{\sum_{n = 0}^{\infty} \frac{2}{2n + 1} z^{2n + 1}} = \frac{1}{2z} \frac{1}{1 + \sum_{n = 1}^{\infty} \frac{1}{2n + 1} z^{2n}} \\ = 
\frac{1}{2 z} - \frac{1}{6} z - \frac{2}{45} z^{3} - \cdots
$$
当 $k \neq 0$ 时
$$
\ln^{-1} \frac{1 + z}{1 - z} = \frac{1}{i 2 k \pi} \frac{1}{1 + \sum_{n = 0}^{\infty} \frac{z^{2n + 1}}{i (2n + 1) k \pi}} \\ = 
- \frac{i}{2 k \pi} + \frac{1}{2 k^{2} \pi^{2}} z + \frac{i}{2 k^{3} \pi^{3}} z^{2} + \cdots
$$
在$z = \infty$ 邻域内，假设 $z = -1$ 到 $z = 1$ 连线上宗量辐角为 $2 k \pi， (k \in \mathbb{Z})$  ，此时在无穷远点宗量辐角为 $(2k + 1) \pi$
$$
\ln^{-1} \frac{1 + z}{1 - z} = \frac{1}{i (2 k + 1) \pi} \frac{1}{1 + \sum_{n = 0}^{\infty} \frac{2z^{- 2n - 1}}{i (2n + 1) (2k + 1) \pi}} \\ = 
- \frac{i}{(2 k + 1) \pi} + \frac{2}{(2 k + 1)^{2} \pi^{2}} \frac{1}{z} + \frac{4i}{(2 k + 1)^{3} \pi^{3}} \frac{1}{z^{2}} + \cdots
$$
## 复变函数 第9次作业

Chasse_neige

2.证明  
$$
f_1(z) = 1 + az + a^2z^2 + \cdots  
$$
与  
$$
f_2(z) = \frac{1}{1 - z} - \frac{(1 - a)z}{(1 - z)^2} + \frac{(1 - a)^2z^2}{(1 - z)^3} - \cdots  
$$
互为解析延拓。  

证明

$f_{1}$ 的收敛区域为
$$
|az| < 1
$$
即
$$
|z| < \frac{1}{|a|}
$$
在收敛域内
$$
f_{1} = \sum_{n = 0}^{\infty} (az)^{n} = \frac{1}{1 - az}
$$
$f_{2}$  的收敛区域
$$
f_{2} (z) = \sum_{n = 0}^{\infty} \frac{(-1)^{n} (1 - a)^{n} z^{n}}{(1 - z)^{n + 1}}
$$
所以 $f_{2}$ 在 
$$
\left| (1 - a) \frac{z}{1 - z} \right| < 1
$$
时收敛

所以收敛域为 $|\frac{z}{1 - z}| < \frac{1}{|1 - a|}$

收敛域内
$$
f_{2} (z) = \sum_{n = 0}^{\infty} \frac{(-1)^{n} (1 - a)^{n} z^{n}}{(1 - z)^{n + 1}} = \frac{1}{1 - z} \sum_{n = 0}^{\infty} \frac{- (1 - a) z}{1 - z}^{n} = \frac{1}{1 - z} \frac{1}{1 + \frac{(1 - a)z}{1- z}} = \frac{1}{1 - az}
$$
所以在两收敛域的交集内两个函数均收敛于 $\frac{1}{1 - az}$，即二者互为解析延拓。

3.请证明级数  
$$
\sum_{n=1}^{\infty} \left( \frac{1}{1 - z^{n+1}} - \frac{1}{1 - z^n} \right)
$$
在区域 $|z| < 1$ 与 $|z| > 1$ 内分别代表两个解析函数，但不互为解析延拓。  

证明

在区域 $|z| < 1$ 内
$$
\sum_{n=1}^{\infty} \left( \frac{1}{1 - z^{n+1}} - \frac{1}{1 - z^n} \right) = - \frac{1}{1- z} + 1
= - \frac{z}{1 - z}
$$
在区域 $|z| > 1$ 内
$$
\sum_{n=1}^{\infty} \left( \frac{1}{1 - z^{n+1}} - \frac{1}{1 - z^n} \right) = - \frac{1}{1- z} 
$$
当 $|z| = 1$ 时对于 $\arg z \in Q$ 来说，必然会存在 $ \frac{1}{1 - z^{n}}$ 没有定义的情况，也就是说在收敛圆边界上有无穷个奇点，且每个点均为奇点集的聚点

二者的解析域没有交集，也就是说不互为解析延拓

4.已知  
$$
f(z) = \sum_{n=0}^{\infty} z^{2^n} = z + z^2 + z^4 + z^8 + \cdots, \quad |z| < 1.
$$

(a) 证明：$z = 1$ 是 $f(z)$ 的奇点

证明

原函数在 $z = 1$ 处满足
$$
f (z) = 1 + 1 + 1 + \cdots
$$
所以 $\forall n \in \mathbb{N}$
$$
\exist k \in \mathbb{N}, s.t. \sum_{i = 0}^{k} z^{2^{i}} > n
$$
所以该级数在$z = 1$ 处发散，$z = 1$ 是 $f(z)$ 的奇点

(b) 证明：$f(z) = z + f(z^2)$，因此 $z^2 = 1$ 的根也是 $f(z)$ 的奇点

证明
$$
z + f (z^{2}) = z + \sum_{n = 0}^{\infty} (z^{2})^{2^{n}} = z + \sum_{n = 1}^{\infty} z^{2^{n}} = \sum_{n = 0}^{\infty} z^{2^{n}} = f (z)
$$
所以因此 $z^2 = 1$ 的根也是 $f(z)$ 的奇点

(c) 进一步证明：$z^{2^k} = 1$ 的 $2^k$ 个根也是 $f(z)$ 的奇点，$k$ 为任意正整数

证明

$k$ 为任意正整数，对于 $k$ 而言
$$
f (z) = \sum_{n = 0}^{k - 1} z^{2^{n}} + \sum_{n = k}^{\infty} z^{2^{n}} = \sum_{n = 0}^{k - 1} z^{2^{n}} + \sum_{n = 0}^{\infty} (z^{2^{k}})^{2^{n}} = \sum_{n = 0}^{k - 1} z^{2^{n}} + f(z^{2^{k}})
$$
所以$z^{2^k} = 1$ 的 $2^k$ 个根也是 $f(z)$ 的奇点，$k$ 为任意正整数

(d) 最后证明：不可能将 $f(z)$ 延拓到单位圆外

证明

由于$z^{2^k} = 1$ 的 $2^k$ 个根是 $f(z)$ 的奇点，$k$ 为任意正整数，所以对于 $z = e^{i \theta}$ 而言，$e^{i 2^{k} \theta} = 1$ 的根均为奇点，所以
$$
\theta = \frac{2 n \pi}{2^{k}} \qquad (n \in \mathbb{Z}, k \in \mathbb{N})
$$
均为奇点，所以
$$
\forall \theta \in [0, 2 \pi) , \forall \epsilon > 0, \exist k, s.t. \frac{1}{2^{k}} < \epsilon
$$
此时用将 $[0, 2 \pi)$ 划分为 $2^{k}$ 个小格，对于 $\theta$ 所在的那个小格
$$
\left| \theta - \frac{n}{2^{k}} 2 \pi \right| < \epsilon
$$
所以在收敛圆边界上每点的邻域内均存在奇点

所以不存在收敛域跨越 $|z| = 1$ 的 Taylor 展开，也就是不能将函数解析延拓至 $|z| = 1$ 外

1.讨论下列函数奇点的性质，如果是孤立奇点，则求出函数在该点的留数  

(3) 
$$
\frac{\cos az - \cos bz}{z^3}
$$

$z = 0$ 是一阶极点，是孤立奇点，留数为
$$
a_{-1} = - \frac{1}{2} (a^{2} - b^{2})
$$
(5) 
$$
\frac{\sin z}{z^2} - \frac{1}{z}
$$
$z = 0$ 是可去奇点，是孤立奇点，留数为
$$
a_{-1} = \lim_{z \to 0} \frac{\sin z - z}{z} = 0
$$
(8)
$$
\frac{z}{1 - \cos z}
$$
$z = 2 k \pi, \quad (k \in \mathbb{Z})$ 处

当 $k = 0$ 时为一阶极点，为孤立奇点，留数为
$$
a_{-1} = 2 
$$
当 $k \neq 0$ 时为二阶极点，为孤立奇点，留数为
$$
a_{-1} = 2
$$
(9) 
$$
\frac{1}{(z - 1) \ln z}
$$
规定割线为$z = 0$ 沿 $x$ 轴延伸到无穷远点的直线，在割线上岸辐角为0.此时 $z = 1$ 处为二阶极点，是孤立奇点，留数为
$$
a_{-1} = \frac{1}{2}
$$
在割线下岸辐角为 $2 \pi$ ，此时 $z = 1$ 为一阶极点，是孤立奇点，留数为
$$
a_{-1} = \frac{1}{2 \pi i}
$$
其它叶上的不同辐角以此类推。

2.指出下列函数在 $\infty$ 点的性质，并求其留数  

(2) 
$$
\frac{\cos z}{z}
$$

换元 $w = \frac{1}{z}$
$$
\frac{\cos z}{z} = w {\cos \frac{1}{w}}
$$
所以在无穷远点原函数为本性奇点，留数为
$$
a_{-1} = - \Res (\frac{1}{w} {\cos \frac{1}{w}}, w = 0) = -1
$$
(3) 
$$
\frac{z}{\cos z}
$$

换元 $w = \frac{1}{z}$
$$
\frac{z}{\cos z} = \frac{1}{w \cos \frac{1}{w}}
$$
所以在无穷远点原函数为非孤立奇点，不存在留数

(6) 
$$
\sqrt{(z - 1)(z - 2)}
$$
换元 $w = \frac{1}{z}$
$$
\sqrt{(z - 1)(z - 2)} = \sqrt{(\frac{1}{w} - 1) (\frac{1}{w} - 2)}
$$
所以无穷远点为原函数三阶极点，留数为
$$
a_{-1} = - \Res (\frac{1}{w^{2}} \sqrt{(\frac{1}{w} - 1) (\frac{1}{w} - 2)}, w = 0) = \frac{1}{8}
$$
## 复变函数 第10次作业

Chasse_neige

#### 3. 利用留数定理计算下面的积分  

(a)  
$$
\int_{0}^{\pi} \frac{dx}{1 - 2p \cos x + p^2}, \quad 0 < p < 1
$$

$$
\int_{0}^{\pi} \frac{dx}{1 - 2p \cos x + p^2} = \frac{1}{2} \oint_{|z| = 1} \frac{1}{1 - 2p \frac{z + \frac{1}{z}}{2} + p^{2}} \frac{d z}{i z} \\ =
\frac{i}{2} \oint_{|z| = 1} \frac{d z}{(pz - 1)(z - p)} = \frac{i}{2} (2 \pi i \Res f (p)) = \frac{\pi}{1 - p^{2}}
$$

(b)  
$$
\int_{0}^{\pi} \frac{d\theta}{1 + \sin^2 \theta}
$$

$$
\int_{0}^{\pi} \frac{d\theta}{1 + \sin^2 \theta} = \frac{1}{2} \oint_{|z| = 1} \frac{1}{1 + (\frac{z- \frac{1}{z}}{2i})^{2}} \frac{dz}{i z} = \frac{1}{2} \oint_{|z| = 1} \frac{i 4z}{z^{4} - 6z^{2} + 1} dz \\ =
2i \oint_{|z^{2}| = 1} \frac{d z^{2}}{z^{4} - 6 z^{2} + 1} = 2i (2 \pi i \Res f(3 - 2 \sqrt{2})) \\ = 
- 4 \pi \frac{1}{- 4 \sqrt{2}} = \frac{\sqrt{2} \pi}{2}
$$

#### 4. 利用留数定理计算下面的积分  

(b)  
$$
\int_{-\infty}^{\infty} \frac{x^2 \, dx}{(x^2 + 1)(x^2 + 2x \cos \theta + 1)}, \quad \cos \theta \neq \pm 1
$$

取围道为上半平面逆时针。由于 $z \to \infty$ 时， $z \frac{z^2}{(z^2 + 1)(z^2 + 2z \cos \theta + 1)} \to 0$ ，所以根据大圆弧引理，实积分等于留数之和
$$
\int_{-\infty}^{\infty} \frac{x^2 \, dx}{(x^2 + 1)(x^2 + 2x \cos \theta + 1)} = 2 \pi i (\Res f (i) + \Res f (- \cos \theta + i \sin \theta)) \\ =
2 \pi i (\frac{1}{4 \cos \theta} + \frac{- \sin \theta - i \cos \theta}{4 \cos \theta \sin \theta}) = \frac{\pi}{2 \sin \theta}
$$
(d)  
$$
\int_{0}^{\infty} \frac{dx}{(1+x^2)\cosh\frac{\pi x}{2}}
$$

如图取围道

<img src="/Users/wutong/Library/Application Support/typora-user-images/image-20250527234852191.png" alt="image-20250527234852191" style="zoom:50%;" />

处了刨去的一条之外，$z \to \infty$ 时 $z \frac{1}{(1 + z^{2}) \cosh z} \to 0$ ，所以根据大圆弧引理
$$
\int_{0}^{\infty} \frac{dx}{(1+x^2)\cosh\frac{\pi x}{2}} = \pi i \sum_{n = 1}^{\infty} \Res f ((2n + 1) i)  =  \pi i (\frac{-i}{2 \pi} + \sum_{n = 1}^{\infty} \frac{(-1)^{n} i}{2 n (n + 1) \pi} ) \\ = 
\frac{1}{2} (1 + \sum_{n = 1}^{\infty} \frac{(-1)^{n + 1}}{n (n + 1)}) = \frac{1}{2} (1 + 2 \ln 2 - 1) = \ln 2  
$$

#### 1. 利用留数定理计算下面的积分  

(a)  
$$
\int_{0}^{\infty} \frac{\cos x}{1 + x^4} \, dx  
$$

$$
\frac{\cos x}{1 + x^{4}}  = \Re [\frac{e^{ix}}{1 + x^{4}}] 
$$

取围道为包围第一象限逆时针。由于 $z \to \infty$ 时， $\frac{1}{1 + z^{4}} \to 0$ ，所以根据 Jordan 引理，实积分等于留数之和
$$
\int_{0}^{\infty} \frac{\cos x}{1 + x^{4}} dx = \frac{1}{2} \Re [2 \pi i (\Res f (e^{i \frac{\pi}{4}}) + \Res f (e^{i \frac{3 \pi}{4}}))] = \frac{1}{2} \Re [2 \pi i (\frac{e^{- \frac{\sqrt{2}}{2}} e^{i (\frac{\sqrt{2}}{2} - \frac{\pi}{4})}}{4i} - \frac{e^{- \frac{\sqrt{2}}{2}} e^{- i( \frac{3 \pi}{4} + \frac{\sqrt{2}}{2})}}{4i})] \\ =
\frac{\sqrt{2} \pi}{4} e^{- \frac{\sqrt{2}}{2}} (\cos \frac{\sqrt{2}}{2} + \sin \frac{\sqrt{2}}{2})
$$
(b)  
$$
\int_{0}^{\infty} \frac{x \sin bx}{x^2 + a^2} \, dx, \quad a, \, b > 0
$$

$$
\frac{x \sin bx}{x^{2} + a^{2}} = \Im \frac{z e^{i b z}}{z^{2} + a^{2}}
$$

取围道为上半空间逆时针。由于 $z \to \infty$ 时， $\frac{z e^{i b z}}{z^{2} + a^{2}} \to 0$ ，所以根据 Jordan 引理，实积分等于留数之和
$$
\int_{0}^{\infty} \frac{x \sin bx}{x^2 + a^2} \, dx = \frac{1}{2} \Im [2 \pi i \Res f (ia)] =\frac{\pi}{2} e^{- ab}
$$

#### 2. 利用留数定理计算下面的积分  

(b)  
$$
\int_{0}^{\infty} \frac{\cos ax - \cos bx}{x^2} \, dx, \quad a, \, b > 0
$$

$$
\frac{\cos ax - \cos bx}{x^2} = \Re [\frac{e^{i a z} - e^{i b z}}{z^{2}}]
$$

函数在 $z = 0$ 处有奇点。

取围道为上半空间逆时针。由于 $z \to \infty$ 时， $\frac{1}{z^{2}} \to 0$ ，所以根据 Jordan 引理，实积分等于
$$
\int_{0}^{\infty} \frac{\cos ax - \cos bx}{x^2} \, dx = \frac{1}{2} \left(\pi i \Res f (0) \right) = \frac{\pi}{2} (b - a)
$$
(d)  
$$
\int_{0}^{\infty} \frac{x - \sin x}{x^3(1 + x^2)} \, dx
$$

$$
\frac{x - \sin x}{x^3(1 + x^2)} =  \frac{z}{z^{3} (1 + z^{2})} - \Im \frac{e^{iz}}{z^{3} (1 + z^{2})} = f (z) + \Im g (z)
$$

函数在 $z = 0$  处有奇点。

取围道为上半空间逆时针。由于 $z \to \infty$ 时， $\frac{1}{z^{3} (1 + z^{2})} \to 0$ ，$z \frac{z}{z^{3} (1 + z^{2})} \to 0$ 所以根据 Jordan 引理和大圆弧引理，实积分等于
$$
\int_{0}^{\infty} \frac{x - \sin x}{x^3(1 + x^2)} \, dx = \frac{1}{2} (\pi i \Res f (0) + 2 \pi i (\Res f (i))) + \Im \frac{1}{2} (\pi i \Res g (0) + 2 \pi i (\Res g (i))) \\ = 
 \frac{1}{2} (2 \pi i \frac{i}{2}) + \frac{1}{2} \Im (\pi i \frac{3}{2} - 2 \pi i \frac{1}{2e}) = \frac{\pi}{4} - \frac{\pi}{2e}
$$
(e)  
$$
\int_{0}^{\infty} \frac{\sin^3 x}{x^3} \, dx
$$

$$
\frac{\sin^3 x}{x^3} = \frac{e^{i 3z} - 3e^{iz} + 3 e^{- iz} - e^{-i 3z}}{-8 i z^{3}}
$$

函数在 $z = 0$  处有奇点。

取围道为上半空间逆时针。由于 $z \to \infty$ 时， $\frac{1}{z^{2}} \to 0$ ，所以根据 Jordan 引理，实积分等于
$$
\int_{0}^{\infty} \frac{\sin^3 x}{x^3} \, dx = \frac{1}{2} \Re \left( \pi i \Res [\frac{e^{i 3z} - 3 e^{i z}}{- 4 i z^{3}}, z = 0]\right) = \frac{3 \pi}{8}
$$
## 复变函数 第11次作业

Chasse_neige

#### 3. 利用留数定理计算下面的积分

(a)  
$$
\int_{0}^{\infty} \frac{x^s}{(1+x^2)^2} \, dx, \quad -1 < s < 3
$$

函数支点为 $z = 0$ 以及无穷远点。取割线为 $z=0$ 沿着 $x$ 轴正半轴指向无穷远点的直线，并且割线上岸宗量辐角为 $0$

取围道为沿着割线上下岸、半个原点的小圆弧以及整个大圆弧。
$$
I (1 - e^{i 2 \pi s}) = 2 \pi i (\Res f (i) + \Res f(-i)) = 2 \pi i (\frac{(s - 1) i^{s + 1}}{4} + \frac{(s - 1) (-i)^{s + 1}}{4})
$$

$$
I = \frac{\pi (s - 1)}{2} \frac{i^{s + 2} - (-i)^{s + 2}}{1 - e^{i 2 \pi s}} = - \frac{\pi (s - 1)}{2} \frac{\sin (\frac{s \pi}{2})}{\sin (s \pi)} = - \frac{\pi (s - 1)}{4 \cos (\frac{s \pi}{2})}
$$

(b)  
$$
\int_{0}^{\infty} \frac{x^{-p}}{1+2x\cos\theta + x^2} \, dx, \quad -1 < p < 1, \quad 0 < \theta < \pi
$$

函数支点为 $z = 0$ 以及无穷远点。取割线为 $z=0$ 沿着 $x$ 轴正半轴指向无穷远点的直线，并且割线上岸宗量辐角为 $0$

取围道为沿着割线上下岸、半个原点的小圆弧以及整个大圆弧。
$$
I (1 - e^{- i 2 \pi p}) = 2 \pi i (\Res f (- e^{i \theta}) + \Res f (- e^{- i \theta})) = 
2 \pi i (\frac{e^{- i p (\theta + \pi)}}{ - 2 i \sin \theta} + \frac{e^{i p (\theta + \pi)}}{2 i \sin \theta})
$$

$$
I = \frac{\pi}{\sin \theta} \frac{e^{i p (\theta + \pi)} - e^{- i p (\theta + \pi)}}{1 - e^{-i 2 \pi p}} = \frac{\pi (\sin p \theta)}{\sin \theta \sin (p \pi)}
$$



#### 4. 利用留数定理计算下面的积分  

(b)  
$$
\int_{0}^{\infty} \frac{1}{x^3+a^3} \, dx, \quad a>0
$$

$$
f (z) = \frac{\ln z}{z^{3} + a^{3}}
$$

函数支点为 $z = 0$ 以及无穷远点。取割线为 $z=0$ 沿着 $x$ 轴正半轴指向无穷远点的直线，并且割线上岸宗量辐角为 $0$

取围道为沿着割线上下岸、半个原点的小圆弧以及整个大圆弧，计算 $f$ 沿着围道的积分


$$
- 2 \pi i  \int_{0}^{\infty} \frac{1}{x^3+a^3} \, dx = 2 \pi i (\Res f (a e^{i \frac{\pi}{3}}) + \Res f(a e^{i \pi}) + \Res f (a e^{i \frac{5 \pi}{3}}))) \\ = 
2 \pi i \left( \frac{a + i \frac{\pi}{3}}{a^{2} (e^{i \frac{\pi}{3}} - e^{i \pi}) (e^{i \frac{\pi}{3}} - e^{i \frac{5 \pi}{3}})} + \frac{a + i \pi}{a^{2} (e^{i \pi} - e^{i \frac{\pi}{3}}) (e^{i \pi} - e^{i \frac{5 \pi}{3}})} + \frac{a + i \frac{5 \pi}{3}}{a^{2} (e^{i \frac{5 \pi}{3}} - e^{i \pi}) (e^{i \frac{5 \pi}{3}} - e^{i \frac{\pi}{3}})} \right)
$$

$$
\int_{0}^{\infty} \frac{1}{x^3+a^3} \, dx = \frac{2\pi}{3 \sqrt{3}a^2}
$$

(d)  
$$
\int_{0}^{\infty} \frac{\ln x}{x^2+a^2} \, dx, \quad a>0
$$

$$
f (z) = \frac{\ln^{2}z - 2 \pi i \ln z}{z^{2} + a^{2}}
$$

函数支点为 $z = 0$ 以及无穷远点。取割线为 $z=0$ 沿着 $x$ 轴正半轴指向无穷远点的直线，并且割线上岸宗量辐角为 $0$

取围道为沿着割线上下岸、半个原点的小圆弧以及整个大圆弧，计算 $f$ 沿着围道的积分
$$
- 4 \pi i \int_{0}^{\infty} \frac{\ln x}{x^2+a^2} \, dx = 2 \pi i (\Res f (i a) + \Res f (-ia)) \\ = 2 \pi i (- \frac{\pi \ln a}{a})
$$

$$
\int_{0}^{\infty} \frac{\ln x}{x^2+a^2} \, dx = \frac{\pi \ln a}{2 a}
$$

#### 5. 利用留数定理计算下面的积分

(d)  
$$
\int_0^1 \frac{\sqrt[4]{x(1-x)^3}}{(1+x)^3} \, dx
$$
函数支点为 $z = 0$ 以及 $z = 1$。取割线为 $z=0$ 沿着 $x$ 轴正半轴指向 $z = 1$ 的线段，并且割线上岸宗量辐角为 $0$

取围道为沿着割线上下岸、半个原点的小圆弧、半个 $z = 1$ 的小圆弧以及整个大圆弧，计算 $f$ 沿着围道的积分
$$
I (1 - i) = 2 \pi i \Res f (-1)
$$

$$
I = \frac{2 \pi i }{1 - i} (-2^{\frac{3}{4}} \frac{3}{128} e^{i \frac{\pi}{4}}) = \frac{3 \pi}{64} 2^{\frac{1}{4}}
$$

