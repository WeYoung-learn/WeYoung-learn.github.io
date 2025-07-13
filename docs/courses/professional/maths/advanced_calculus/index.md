## 高等微积分（2） 第1次作业 

Chasse_neige

##### 1.  判断如下级数的收敛发散性，需要给出证明。

(1) 级数 $\sum_{n=1}^{\infty} \frac{\sin(n\theta)}{n^2}$，其中 $\theta$ 是给定的实数。
$$
\left|\frac{\sin(n \theta)} {n^{2}} \right| \leq \frac{1}{n^{2}}
$$

$$
\therefore \,\, \sum_{n=1}^{\infty} \left| \frac{\sin(n\theta)}{n^2} \right| \leq \sum_{n=1}^{\infty} \frac{1}{n^2} = \frac{\pi^{2}}{6}
$$

由比较定理，绝对收敛。

(2) 级数 $\sum_{n=1}^{\infty} \frac{n!}{n^n}$ 。

作 Ratio Test：
$$
\lim_{ n \to \infty} \frac{a_{n+1}}{a_{n}} = \lim_{ n \to \infty} \frac{n}{n+1}^{n} = \lim_{ n \to \infty} \left((1 - \frac{1}{n+1})^{- (n+1)} \right)^{- \frac{n}{n+1}} = \frac{1}{e} < 1
$$
收敛。

(3) 级数 $\sum_{n=1}^{\infty} \frac{n! a^n}{n^n}$，其中 $a > 0$ 是给定的实数。

作 Ratio Test：
$$
\lim_{ n \to \infty} \frac{a_{n+1}}{a_{n}} = \lim_{ n \to \infty} a \frac{n}{n+1}^{n} = \frac{a}{e}
$$
当 $a>e$ 时，发散；当 $a<e$ 时，收敛。

当 $a=e$ 时：
$$
\because \,\, e^{n} > \sum_{i=0}^{n} \frac{n^{i}}{i!} \geq \frac{n^{n}}{n!}
$$

$$
\therefore \,\, a_{n} \geq 1
$$

发散。

(4) 级数 $\sum_{n=2}^{\infty} \frac{n^{\ln n}}{(\ln n)^n}$.
$$
a_{n} = e^{(\ln n)^{2} - n \ln(\ln(n))}
$$
作 Root Test：
$$
\lim_{n \to \infty} {a_{n}}^{\frac{1}{n}} = \lim_{n \to \infty} e^{\frac{(\ln n)^{2}}{n} - \ln(\ln(n))} = 0 < 1
$$
收敛。

(5) 级数 $\sum_{n=1}^{\infty} \frac{(\ln n)^p}{1+n^2}$，其中 $p$ 是给定的正数。
$$
\frac{(\ln n)^p}{1+n^2} < \frac{(\ln n )^{p}}{n^{2}}
$$
对 $(\ln n)^{p}$ 进行分析：取$\alpha > 0$ ，
$$
\frac{(\ln n)^{p}}{n^{\alpha}} = \left( \frac{p}{\alpha} \frac{\ln n^{\frac{\alpha}{p}}}{n^{\frac{\alpha}{p}}}\right)^{p}
$$

$$
\therefore \,\, \lim_{n \to \infty} \frac{(\ln n)^{p}}{n^{\alpha}} = 0
$$

所以总可以找到 $N$ 使得在 $n > N$ 时，
$$
\frac{(\ln n)^{p}}{n^{\alpha}} <1
$$
回归本题，取 $0 < \alpha <1$ ，

级数 $\sum_{n}\frac{(\ln n )^{p}}{n^{2}}$ 在 $n$ 足够大时小于 $\sum \frac{1}{n^{2-\alpha}}$ 这个正项收敛级数。

所以由比较定理，级数$\sum_{n=1}^{\infty} \frac{(\ln n)^p}{1+n^2}$ 收敛。

(6) 级数 $\sum_{n=1}^{\infty} \frac{(\ln n)^q}{n^p}$，其中 $p, q$ 是给定的正数。

当 $p \leq 1$ 时， $\frac{(\ln n)^q}{n^p} > \frac{1}{n}$，故发散。

当 $p > 1$ 时，利用上一题的结论，在 $n$ 充分大时，$\frac{(\ln n)^q}{n^p} < \frac{1}{n^{p - \delta}}$，$\delta \in (0, p-1)$，由于 $\sum \frac{1}{n^{p - \delta}}$ 收敛，由比较定理，原级数收敛。

(7) 级数 $\sum_{n=1}^{\infty} \left( \frac{1}{n^\alpha} - \sin \frac{1}{n^\alpha} \right)$，其中 $\alpha$ 是给定的正数。

因为 $\frac{1}{n^{\alpha}}$ 单调递减且趋于零，所以
$$
\lim_{ n \to \infty} \frac{\frac{1}{n^{\alpha}} - \sin \frac{1}{n^{\alpha}}}{\frac{\frac{1}{n^{\alpha}}^{3}}{6}} = 1
$$
由比较定理的极限形式，级数 $\sum_{n=1}^{\infty} \left( \frac{1}{n^\alpha} - \sin \frac{1}{n^\alpha} \right)$ 与级数$\sum_{n=1}^{\infty} \frac{1}{6 n^{3 \alpha}}$ 收敛性质相同。

所以当 $\alpha \leq \frac{1}{3}$ 时，原级数收敛；当 $\alpha > \frac{1}{3}$ 时，原级数发散。

(8) 级数 $1 - \frac{1}{2^{2p}} + \frac{1}{3^p} - \frac{1}{4^{2p}} + \cdots + \frac{1}{(2n-1)^p} - \frac{1}{(2n)^{2p}} + \cdots$，其中 $p$ 是给定的正数。

当$p > 1$ 时，

该交错级数的绝对值 $1 + \frac{1}{2^{2p}} + \frac{1}{3^p} + \frac{1}{4^{2p}} + \cdots + \frac{1}{(2n-1)^p} + \frac{1}{(2n)^{2p}} + \cdots < 1 + \frac{1}{2^{p}} + \frac{1}{3^p} + \frac{1}{4^{p}} + \cdots + \frac{1}{(2n-1)^p} + \frac{1}{(2n)^{p}} + \cdots$ 收敛，故原级数绝对收敛。

当 $p \leq 1$ 时，
$$
1 - \frac{1}{2^{2p}} + \frac{1}{3^p} - \frac{1}{4^{2p}} + \cdots + \frac{1}{(2n-1)^p} - \frac{1}{(2n)^{2p}} + \cdots \\ = 1 - \frac{1}{2^{p}} + \frac{1}{2^p} - \frac{1}{2^{2p}} + \frac{1}{3^p} - \frac{1}{4^{p}} + \frac{1}{4^p} - \frac{1}{4^{2p}}  + \cdots + \frac{1}{(2n-1)^p} - \frac{1}{(2n)^{p}} + \frac{1}{(2n)^{p}}- \frac{1}{(2n)^{2p}} + \cdots
$$
拆分成两个级数：
$$
1 - \frac{1}{2^{2p}} + \frac{1}{3^p} - \frac{1}{4^{2p}} + \cdots + \frac{1}{(2n-1)^p} - \frac{1}{(2n)^{2p}} + \cdots \\ = 
1 - \frac{1}{2^{p}} + \frac{1}{3^p} - \frac{1}{4^{p}} + \cdots + \frac{1}{(2n-1)^p} - \frac{1}{(2n)^{p}} + \cdots + \sum_{n} \frac{1}{(2n)^{p}} - \frac{1}{(2n)^{2p}} 
$$
由 Leibniz Test，第一部分的绝对值单调递减且趋于零，所以收敛。故原级数的收敛性等价于第二部分收敛性。

利用比较定理的极限形式，构造 $b_{n} = \frac{1}{(2n)^{p}}$，
$$
\lim_{n \to \infty} \frac{a_{n}}{b_{n}} = \lim_{n \to \infty} (1 - \frac{1}{(2n)^{p}}) = 1
$$
所以第二部分收敛性等于 $ \sum \frac{1}{(2n)^{p}}$的收敛性。

所以当 $p \leq 1$时 $ \sum \frac{1}{(2n)^{p}}$ 发散，故原级数发散。

(9) 级数 $\sum_{n=1}^{\infty} \frac{\sin n}{n^\alpha}$，其中 $\alpha > 0$。

作 Dirichlet Test：
$$
\frac{\sin n}{n^{\alpha}} = \frac{1}{n^{\alpha}} \cdot \sin n 
$$
其中 $\frac{1}{n^{\alpha}}$ 递减且趋于零，
$$
\sum_{k=1}^{n} \sin k = \frac{\cos \frac{1}{2} - \cos (n+ \frac{1}{2})}{2 \sin (\frac{1}{2})}
$$
有界，所以原级数收敛。

##### 2. 证明如下的 Cauchy condensation test.

设 $f: [1, +\infty) \to \mathbb{R}_{\geq 0}$ 是取值为非负实数的不增函数，则级数 $\sum_{n=1}^{\infty} f(n)$ 收敛当且仅当级数 $\sum_{n=1}^{\infty} 2^n f(2^n)$ 收敛。

证明：因为$f: [1, +\infty) \to \mathbb{R}_{\geq 0}$ 是取值为非负实数的不增函数
$$
\sum_{n=1}^{\infty} f(n) = f(1) + f(2) + f(3) + \cdots \leq \sum_{n=0}^{\infty} 2^{n} f(2^{n})
$$

$$
\sum_{n=1}^{\infty} f(n) \geq \sum_{n=1}^{\infty} 2^{n-1} f(2^{n})
$$

充分性：因为$\sum_{n=1}^{\infty} 2^n f(2^n)$ 收敛，由比较定理，正项级数$\sum_{n=1}^{\infty} f(n)$ 收敛。

必要性：因为 $\sum_{n=1}^{\infty} f(n)$ 收敛，由比较定理，$\sum_{n=1}^{\infty} 2^{n-1} f(2^{n})$ 收敛。所以 $\sum_{n=1}^{\infty} 2^n f(2^n) = 2 \sum_{n=1}^{\infty} 2^{n-1} f(2^{n})$ 收敛。 

##### 3. 设 $\sum_{n=1}^{\infty} a_n$ 是正项级数，满足 $\lim_{n \to \infty} a_n = 0$。证明：级数 $\sum_{n=1}^{\infty} \ln(1 + a_n)$ 收敛当且仅当级数 $\sum_{n=1}^{\infty} a_n$ 收敛。

证明：

证法1: 显然级数 $\sum_{n=1}^{\infty} \ln(1 + a_n)$ 为正项级数。

充分性：利用不等式 $\ln (1 + a_{n}) \leq a_{n}$ ，

因为级数 $\sum_{n=1}^{\infty} a_n$ 收敛，由比较定理，正项级数 $\sum_{n=1}^{\infty} \ln(1 + a_n)$ 收敛。

必要性：
$$
\sum_{k=1}^{n} \ln(1 + a_k) = \ln \prod_{k=1}^{n}(1 + a_{k})
$$

$$
\lim_{n \to \infty} \sum_{k=1}^{n} \ln (1 + a_{n}) = A
$$

利用 $\ln$ 函数的连续性：
$$
\lim_{n \to \infty} \prod_{k=1}^{n}(1 + a_{k}) = e^{A}
$$

$$
\prod_{k=1}^{n}(1 + a_{k}) \geq 1 + \sum_{k=1}^{n} a_{k}
$$



所以由比较定理，正项级数 $\sum_{k=1}^{n} a_{k}$ 收敛。

证法2: 利用比较定理的极限形式：
$$
\lim_{n \to \infty} \frac{\ln (1 + a_{n})}{a_{n}} = \lim_{x \to 0} \frac{\ln (1+x)}{x} =\lim_{x \to 0} \frac{\frac{1}{1+x}}{1} = 1
$$
所以二者有相同的收敛发散性质。# 高等微积分 （2） 第2次作业

Chasse_neige

##### 1 幂级数的收敛域与求和公式

考虑幂级数 $\sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + ...$

(1) 确定上述幂级数的收敛域

利用 Ratio Test：
$$
\lim_{n \to \infty} \frac{|a_{n+1}|}{|a_{n}|} = \lim_{n \to \infty} \frac{n}{n+1} =1
$$

$$
\therefore \,\, R = \frac{1}{1} = 1
$$

(2) 证明: 对任何 $|x| < 1$, 有

$$
\sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = \ln(1 + x)
$$

证明：由（1）的收敛半径可知，对任何 $|x| < 1$，级数 $\sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = x - \frac{x^2}{2} + \frac{x^3}{3} - \frac{x^4}{4} + ...$绝对收敛。

对函数 $\ln (1+x)$ 作 Taylor 展开：
$$
\frac{\mathrm{d}^{n}}{\mathrm{d} x^{n}} \ln (1+x) = (-1)^{n-1} \frac{(n-1)!}{(1+x)^{n}}
$$

$$
\therefore \,\, \ln (1+x) = \sum_{n=1}^{\infty} \frac{(-1)^{n-1}}{n!} (n-1)! x^{n}
$$

已经证明在 $|x| < 1$ 时该级数绝对收敛，所以 $\sum_{n=1}^{\infty} (-1)^{n-1} \frac{x^n}{n} = \ln(1 + x) \quad \forall |x| < 1$

(3) 证明:
$$
\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{n} = \ln 2
$$

对该交错级数作 Leibniz Test：

$\frac{1}{n}$ 递减且趋于零，故该级数条件收敛。由 Abel Theorem，该级数对应的和函数在 $x = 1$处左连续，所以$\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{n} = \ln 2$

##### 2 函数的幂级数展开

(1) 将函数 $f(x) = \arctan x$ 在 $x = 0$ 附近表示成幂级数.

作 Taylor 展开：
$$
\arctan x = \sum_{n=0}^{\infty} \frac{(-1)^{n}}{2n+1} x^{2n+1}
$$
(2) 确定上述级数的收敛半径.

作 Ratio Test ：
$$
\lim_{n \to \infty} \frac{|a_{n+1}|}{|a_{n}|} = \lim_{n \to \infty} \frac{2n + 1}{2n + 3} = 1
$$
所以收敛半径为1

(3) 证明:
$$
\frac{\pi}{4} = \sum_{n=0}^{\infty} (-1)^n \frac{1}{2n + 1} = 1 - \frac{1}{3} + \frac{1}{5} - \frac{1}{7} + ...
$$

对该交错级数作 Leibniz Test：

$\frac{1}{2n + 1}$ 递减且趋于零，故该级数条件收敛。由 Abel Theorem，该级数对应的和函数在 $x = 1$处左连续，所以$\sum_{n=1}^{\infty} (-1)^{n-1} \frac{1}{2n + 1} = \frac{\pi}{4}$

##### 3 函数项级数的性质

考虑函数项级数 $\zeta(x) = \sum_{n=1}^{\infty} \frac{1}{n^x}$.

(1) 求上述函数项级数的收敛域 $X$.

当 $x > 1$ 时：使用积分判别法，考虑积分 $\int_{1}^{\infty} \frac{1}{t^x} \, dt$。对于 $x > 1$，该积分收敛，因此级数 $\sum_{n=1}^{\infty} \frac{1}{n^x}$ 收敛。

当 $x = 1$ 时：此时级数变为调和级数 $\sum_{n=1}^{\infty} \frac{1}{n}$，发散。

当 $x < 1$ 时：此时通项 $\frac{1}{n^x}$ 大于 $\frac{1}{n}$，而 $\sum_{n=1}^{\infty} \frac{1}{n}$ 发散，根据比较定理，$\sum_{n=1}^{\infty} \frac{1}{n^x}$ 发散。
所以收敛域为 $(1, +\infty)$

(2) $\zeta(x)$ 在 $X$ 上是否连续? 请详细说明理由.

连续，理由如下：

$\zeta(x)$ 在 $X$ 上连续等价于函数序列 $a_{n}(x) = \frac{1}{n^{x}}$ 一致收敛。$\forall b >1$ ，对在 其作 M-Test :

$a_{n} (x) < \frac{1}{n^{{b}}} \quad \forall x > b$ ，又因为 $\sum M_{n} = \zeta (b)$ 收敛，所以 $a_{n}(x)$ 在 $(b, + \infty)$ 上一致收敛，即 $\zeta (x)$ 在 $(b, + \infty)$ 上连续，对任意 $x > 1$，总能找到 $1 < b < x$ ，所以 $\zeta(x)$ 在 $X$ 上连续。

(3) $\zeta(x)$ 在 $X$ 上是否可导, 求出其导函数 $\zeta'(x)$. 

可导，理由如下：

$\zeta(x)$ 在 $X$ 上可导等价于 $\zeta' (x)$ 对应的函数级数连续且在$X$ 上一致收敛且$\zeta(x)$ 在 $X$ 上点点收敛。$\zeta(x)$ 在 $X$ 上点点收敛已经在（1）中说明，现在证明 $\zeta' (x)$ 对应的函数级数在$X$ 上一致收敛。
$$
\frac{\mathrm{d}}{\mathrm{d} x} \frac{1}{n^{x}} = - \ln n  \frac{1}{n^{x}}
$$
对级数  $\sum_{n=1}^{\infty} - \ln n \frac{1}{n^x}$ 作M-Test：

$M_{n} = \frac{\ln n }{n^{b}}$ ，有 $\sum M_{n}$ 与级数 $\sum \frac{n^{\epsilon}}{n^{b}}$ 收敛性一致 $(\forall \epsilon > 0)$，所以取 $0 < \epsilon < b-1$ 得到 $\sum M_{n}$收敛，故级数  $\sum_{n=1}^{\infty} - \ln n \frac{1}{n^x}$ 一致收敛。所以$\forall x > b$ $\zeta (x)$ 在 $(b, + \infty)$ 上可导，对任意 $x > 1$，总能找到 $1 < b < x$ ，所以 $\zeta(x)$ 在 $X$ 上可导。

##### 4 幂级数的收敛半径与函数展开

(1) 确定幂级数 $\sum_{n=0}^{\infty} \binom{2n}{n} x^n$ 的收敛半径, 其中 $\binom{2n}{n} = \frac{(2n)!}{n!n!}$.

作 Ratio Test ：
$$
\lim_{n \to \infty} \frac{|a_{n+1}|}{|a_{n}|} = \lim_{n \to \infty} \frac{(2n + 2)(2n + 1)}{(n + 1)^{2}} = 4
$$
所以收敛半径为 $\frac{1}{4}$

(2) 将函数 $f(x) = \frac{1}{\sqrt{1 - x}}$ 在 $x = 0$ 附近表示成幂级数, 只需叙述结果.
$$
f(x) = \frac{1}{\sqrt{1 - x}} = 1 + \sum_{n=1}^{\infty} \frac{(2n - 1)!!}{2^{n} n!} x^{n} \qquad \forall |x| < 1
$$
(3) 将函数 $g(x) = \arcsin x$ 在 $x = 0$ 附近表示成幂级数, 需要说明理由.

理由：
$$
\frac{\mathrm{d}}{\mathrm{d} x} \arcsin x = \frac{1}{\sqrt{1 - x^{2}}} = \sum_{n=1}^{\infty}
\binom{-1/2}{m} (-x^2)^m = \sum_{m=0}^{\infty} \frac{(2m)!}{(m!)^2 4^m} x^{2m} \qquad \forall \, |x| < 1
$$
在证明这一级数的可积性：由于幂级数在收敛半径内连续可积所以由 Ratio Test 容易得到该级数在 $|x| < 1$ 内可积。

利用逐项积分：
$$
\arcsin x = \int_{0}^{x} \frac{1}{\sqrt{1 - x^{2}}} \mathrm{d} x = \sum_{m=0}^{\infty} \int_{0}^{x} \frac{(2m)!}{(m!)^2 4^m} x^{2m} \mathrm{d} x = \sum_{m=0}^{\infty} \frac{(2m)!}{(m!)^2 4^m (2m+1)} x^{2m+1} \qquad \forall \, |x| < 1
$$


##### 5 函数级数的收敛性与可导性

对每个正整数 $n$, 设 $M_n$ 是非负实数, 函数 $f_n$ 在 $[a, b]$ 上连续且在 $(a, b)$ 上处处可导, 满足如下条件:

(i) 级数 $\sum_{n=1}^{\infty} M_n$ 收敛.

(ii) 对任何正整数 $n$, 对任何 $x \in (a, b)$, 有 $|f_n'(x)| \leq M_n$.

(iii) 级数 $\sum_{n=1}^{\infty} f_n(a)$ 收敛.

(1) 证明: 函数级数 $\sum_{n=1}^{\infty} f_n(x)$ 在区间 $[a, b]$ 上点点收敛到某个和函数 $S(x)$.

证明：因为级数 $\sum_{n=1}^{\infty} M_n$ 收敛，所以根据M-Test，级数 $\sum_{n=1}^{\infty} f_n'(x)$ 一致收敛，假设其收敛至 $g (x)$。
$$
\sum_{n=1}^{\infty} \int_{a}^{x} f_{n}' (x) \mathrm{d} x = \sum_{n=1}^{\infty} f_{n} (x) - f_{n} (a) \qquad x \in [a,b]
$$

$$
\sum_{n=1}^{\infty} |f_{n} (x) - f_{n} (a)| \leq \sum_{n=1}^{\infty} \int_{a}^{x} |f_{n}' (x)| dx \leq \sum_{n=1}^{\infty} M_{n} (x - a)
$$

由于级数 $\sum_{n=1}^{\infty} M_n$ 收敛，所以由比较定理级数 $\sum_{n=1}^{\infty} f_{n} (x) - f_{n} (a)$ 绝对收敛。所以级数 $\sum_{n=1}^{\infty} f_n(x) = \sum_{n=1}^{\infty} f_{n} (x) - f_{n} (a) + \sum_{n=1}^{\infty} f_{n} (a)$ 点点收敛。  

(2) 假设对每个正整数 $n$, $f_n'$ 在 $(a, b)$ 上连续. 证明: $S(x)$ 在区间 $(a, b)$ 上处处可导。

证明：由于$f_n'$ 在 $(a, b)$ 上连续，且级数 $\sum_{n=1}^{\infty} f_n'(x)$ 一致收敛，所以$g (x)$连续可积。
$$
\int_{a}^{x} g (t) \mathrm{d} t = \sum_{n=1}^{\infty} \int_{a}^{x} f_{n}' (x) \mathrm{d} x = \sum_{n=1}^{\infty} f_{n} (x) - f_{n} (a) \qquad x \in [a,b]
$$
记 $\sum_{n=1}^{\infty} S_{n} (x) = f (x) $ ，$\sum_{n=1}^{\infty} f_{n} (a) = S(a)$
$$
S (x) = S(a) + \int_{a}^{x} g (t) \mathrm{d} t
$$
根据微积分基本定理的结果，$S(x)$ 在区间 $(a, b)$ 上处处可导。

##### 6 一致收敛的 Dirichlet 判别法

设函数序列 $\{a_n(x)\}_{n=1}^\infty$ 在区间 $I$ 上一致收敛到零函数, 且对每个 $x \in I$, $\{a_n(x)\}_{n=1}^\infty$ 关于 $n$ 是单调的; 设 $\{b_n(x)\}_{n=1}^\infty$ 的部分和序列在区间 $I$ 上一致有界, 即存在正数 $M$, 使得

$$
|b_1(x) + ... + b_n(x)| \leq M, \forall n \in \mathbb{Z}^+, \forall x \in I.
$$

证明: 函数级数 $\sum_{n=1}^{\infty} a_n(x) b_n(x)$ 在区间 $I$ 上一致收敛.

证明：利用柯西准则证明。记$\{b_n(x)\}_{n=1}^\infty$ 的部分和 $\sum_{k = 1}^{n} b_{k} (x) = B_{n} (x)$
$$
\sum_{k=n+1}^{m} a_k(x) b_k(x) = \sum_{k=n+1}^{m} a_{k} (x) (B_{k} (x) - B_{k - 1} (x)) \\ = a_{m}(x) B_m(x) - a_{n+1}(x) B_n(x) + \sum_{k=n+1}^{m-1} (a_k(x) - a_{k+1}(x)) B_k(x)
$$

$$
\Big|\sum_{k=n+1}^{m} a_k(x) b_k(x) \Big| \leq |a_{m}(x) B_m(x)| + |a_{n+1}(x) B_n(x)| + \sum_{k=n+1}^{m-1} (a_k(x) - a_{k+1}(x)) |B_k(x)| \\ \leq |a_{n} (x)| M + |a_{m} (x)| M + |a_{n+1} (x) - a_{m} (x)| M
$$

由于函数序列 $\{a_n(x)\}_{n=1}^\infty$ 在区间 $I$ 上一致收敛到零函数，所以 $\forall \epsilon > 0 ,\exist N, s.t. \forall x \in I, \forall n > N, |a_{n} (x)| < \frac{\epsilon}{4M}$
$$
\Big|\sum_{k=n+1}^{m} a_k(x) b_k(x) \Big| < \epsilon
$$
所以根据柯西准则，函数级数 $\sum_{n=1}^{\infty} a_n(x) b_n(x)$ 在区间 $I$ 上一致收敛。

##### 7 一致收敛的 Abel 判别法

设对每个 $x \in I$, $\{a_n(x)\}_{n=1}^\infty$ 关于 $n$ 是单调的, 且函数序列 $\{a_n(x)\}_{n=1}^\infty$ 在区间 $I$ 上一致有界, 即存在正数 $K$, 使得

$$
|a_n(x)| \leq K, \forall n \in \mathbb{Z}_+, \forall x \in I;
$$

设函数级数 $\sum_{n=1}^{\infty} b_n(x)$ 在区间 $I$ 上一致收敛. 证明: 函数级数 $\sum_{n=1}^{\infty} a_n(x) b_n(x)$ 在区间 $I$ 上一致收敛.
证明：设 $B_n(x) = \sum_{k=1}^n b_k(x)$，由于 $\sum_{n=1}^{\infty} b_n(x)$ 一致收敛，则 $\{B_n(x)\}$ 在 $I$ 上一致收敛到某个函数 $B(x)$。
由于 $\{B_n(x)\}$ 一致收敛，根据一致收敛的柯西准则，对任意 $\epsilon > 0$，存在 $N \in \mathbb{Z}^+$，使得对任意 $m > n \geq N$ 和任意 $x \in I$，有
$$
|B_m(x) - B_n(x)| < \frac{\epsilon}{3K}
$$
同时由于 $\{a_n(x)\}_{n=1}^\infty$ 关于 $n$ 是单调且一致有界的，所以$\{a_n(x)\}_{n=1}^\infty$ 在区间 $I$ 上点点收敛到函数$a (x)$ 。
$$
\sum_{k=n+1}^m a_k(x) b_k(x) = \sum_{k=n+1}^m a_k(x) (B_k(x) - B_{k-1}(x)).
$$
由于 $\{a_n(x)\}$ 是单调的，假设其单调递减（单调递增的情况类似），则 $a_k(x) - a_{k+1}(x) \geq 0$。
$$
\sum_{k=n+1}^{m} a_k(x) b_k(x) = a_{m}(x) B_m(x) - a_{n+1}(x) B_n(x) + \sum_{k=n+1}^{m-1} (a_k(x) - a_{k+1}(x)) B_k(x) \\ = a_{m} (x) (B_{m} (x) - B_{n} (x)) + \sum_{k = n + 1}^{m - 1} (a_{k} (x) - a_{k+1} (x))(B_{k} (x) - B_{n} (x)) \\ \leq |a_{m} (x)||B_{m} (x) - B_{n} (x)| + \sum_{k = n + 1}^{m - 1} |a_{k} (x) - a_{k+1} (x)||B_{k} (x) - B_{n} (x)| \leq \frac{\epsilon}{3} + (a_{n+1} (x) - a_{m} (x)) \epsilon \\ =
\frac{\epsilon}{3} + \frac{2}{2} \epsilon = \epsilon
$$

这表明 $\sum_{n=1}^{\infty} a_n(x) b_n(x)$ 满足一致收敛的柯西准则，所以 函数级数 $\sum_{n=1}^{\infty} a_n(x) b_n(x)$ 在区间 $I$ 上一致收敛。

##### 8 幂级数的 Abel 第二定理

设幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 在点 $x_0 > 0$ 处收敛. 证明: 该幂级数在 $[0, x_0]$ 上一致收敛.

取 $0 < b < x_{0}$ ，对区间 $[0,b)$ 上的幂级数作M-Test：

$|a_{n} x^{n}| < |a_{n}|b^{n}$ 因为b在收敛半径之内，所以级数 $\sum_{n=0}^{\infty} a_{n=0} b^{n}$ 绝对收敛，即级数 $\sum_{n=0}^{\infty} |a_{n}|b^{n}$ 收敛。

所以幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 在区间 $[0,b)$ 上一致收敛。

故幂级数$\sum_{n=0}^{\infty} a_n x^n$ 在区间 $[0,x_{0})$ 上一致收敛，记其收敛至 $f(x)$。
$$
\forall \epsilon > 0 , \exist N \in \Z_{+} , s.t. \forall n > N |f (x) - \sum_{k=0}^{n} a_k x^k| < \epsilon \quad x \in [0, x_{0})
$$
又因为幂级数 $\sum_{n=0}^{\infty} a_n x^n$ 在点 $x_0 > 0$ 处收敛吗，记其收敛至 $f(x_{0})$。
$$
\forall \epsilon > 0 , \exist N_{x_{0}} \in \Z_{+} , s.t. \forall n > N_{x_{0}} |f (x_{0}) - \sum_{k=0}^{n} a_k x_{0}^k| < \epsilon
$$

$$
\therefore \,\, \forall \epsilon > 0 , N' = \max\{ N, N_{x_{0}} \}, s.t. \forall n > N' |f (x) - \sum_{k=0}^{n} a_k x^k| < \epsilon \quad x \in [0, x_{0}]
$$

所以该幂级数在 $[0, x_0]$ 上一致收敛.# 高等微积分 （2） 第3次作业

Chasse_neige

1. 给定有界闭区间 $I = [a, b]$，令 $C = C(I)$ 为由 $I$ 上的所有连续函数所构成的集合，对 $f, g \in C$，定义它们之间的距离为

$$
d(f, g) = \max_{x \in I} |f(x) - g(x)|
$$

(1) 证明：$d$ 是 $C$ 上的一个度量。

证明：逐条验证度量的三大性质：

对称性：$d(f, g) = \max_{x \in I} |f(x) - g(x)| = d (g, f)$ 

正定性：显然满足

三角不等式：
$$
d (f, g) + d (g, h) = \max_{x \in I} |f (x) - g (x)| + \max_{x \in I} |g (x) - h (x)| \geq \max_{x \in I} |f (x) - h(x)| = d (f, h)
$$
成立，所以$d$ 是 $C$ 上的一个度量。

(2) 称 $C$ 中的序列 $\{f_n\}$ 收敛到 $f \in C$，记作 $\lim_{n \to \infty} f_n = f$，如果对任何 $\epsilon > 0$，存在正整数 $N$，使得对 $n \geq N$ 都有 $d(f_n, f) < \epsilon$。

称 $\{f_n\}_{n=1}^\infty$ 是一个 Cauchy 列，如果对任何 $\epsilon > 0$，存在正整数 $N$，使得对任何 $n, m \geq N$ 总有 $d(f_n, f_m) < \epsilon$。

证明：$C$ 中的任何 Cauchy 列都收敛，即对 $C$ 中的任何 Cauchy 列 $\{f_n\}_{n=1}^\infty$，存在 $f \in C$ 使得 $\lim_{n \to \infty} f_n = f$

证明：因为对任何 $\epsilon > 0$，存在正整数 $N$，使得对 $n \geq N$ 都有 $d(f_n, f) < \epsilon$，所以 $\forall x_{0} \in I$ ，  $f_{n}(x_{0})$ 为 Cauchy 列。记  $f_{n}(x_{0})$收敛至 $f (x_{0})$，所以  $f_{n} (x)$ 点点收敛至 $f$ 

2. 设 $f, g$ 是 $[a, b]$ 上的可积函数。证明：

$$
\left( \int_a^b f(x)g(x) \, dx \right)^2 \leq \left( \int_a^b f(x)^2 \, dx \right) \cdot \left( \int_a^b g(x)^2 \, dx \right).
$$

证明：
$$
\int_{a}^{b} (f (x) + t g(x))^{2} dx = \int_{a}^{b} f^{2} (x) + 2 t f (x) g (x) + t^{2} g^{2} (x) dx \geq 0
$$
 对于所有参数 $t$ 均成立，所以关于 $t$ 的判别式小于零：
$$
4 \left( \int_a^b f(x)g(x) \, dx \right)^2 \leq 4 \left( \int_a^b f(x)^2 \, dx \right) \cdot \left( \int_a^b g(x)^2 \, dx \right).
$$
即 $\left( \int_a^b f(x)g(x) \, dx \right)^2 \leq \left( \int_a^b f(x)^2 \, dx \right) \cdot \left( \int_a^b g(x)^2 \, dx \right).$

3. 证明：$U$ 是 $\mathbb{R}^n$ 的开集当且仅当 $U$ 可以表示成一族开球邻域的并。

必要性⇒
假设 $U$ 是 $\mathbb{R}^n$ 中的开集。根据开集的定义，对任意 $x \in U$，存在半径 $r_x > 0$，使得开球 $B_{r_{x}} (x) = \{ y \in \mathbb{R}^n \mid \|y - x\| < r_x \}$ 完全包含在 $U$ 中，考虑所有这样的开球的并集：
$$
U = \bigcup_{x \in U} B_{r_{x}} (x)
$$
每个 $x \in U$ 都属于对应的 $B_{{r_{x}}} (x)$，因此 $U \subseteq \bigcup_{x \in U} B_{r_{x}} (x)$。

每个 $B_{r_{{x}}} (x)$ 是 $U$ 的子集，因此它们的并集 $\bigcup_{x \in U} B_{r_{x}} (x) \subseteq U$。

综上，$U$ 可表示为一族开球邻域的并。

充分性⇐
假设 $U$ 可以表示为一族开球的并，即存在集合 $\Lambda$，使得：
$$
U = \bigcup_{\lambda \in \Lambda} B_{r_{\lambda}} (x_\lambda)
$$
其中每个 $B_{r_{\lambda}} (x_\lambda)$ 是 $\mathbb{R}^n$ 中的开球。 
由于每个开球 $B_{r_{\lambda}} (x_\lambda)$ 本身是开集，而开集的任意并集仍然是开集，因此 $U$ 是开集。

4. 计算极限。

(1)
$$
\lim_{(x, y) \to 0} \frac{1 - \cos(xy)}{x^2 + y^2}
$$

利用不等式 $\cos (xy) \geq 1- \frac{x^{2} y^{2}}{2}$
$$
 \frac{1 - \cos(xy)}{x^2 + y^2} \leq \frac{x^{2} y^{2}}{2 (x^{2} + y^{2})} = \frac{1}{2} \frac{1}{\frac{1}{x^{2}} + \frac{1}{y^{2}}} \leq \frac{1}{8} (x^{2} + {y^{2}})
$$
由于 $\frac{1 - \cos(xy)}{x^2 + y^2} > 0$，且 $\lim_{(x,y) \to 0} \frac{1}{8} (x^{2} + y^{2}) = 0$，所以由夹逼定理
$$
\lim_{(x, y) \to 0} \frac{1 - \cos(xy)}{x^2 + y^2} = 0
$$
(2)
$$
\lim_{(x, y) \to (0, 0)} \frac{-3x^2y + y^3 - 4xy}{x^2 + y^2}
$$

极限不存在，证明：

上述极限可以拆为两部分：
$$
\lim_{(x, y) \to (0, 0)} \frac{-3x^2y + y^3 - 4xy}{x^2 + y^2} = \lim_{(x,y) \to (0,0)} \frac{-3 x^{2} y + y^{3}}{x^{2} +  y^{2}} -  \frac{4 x y}{x^{2} + y^{2}}
$$
由于 $|- 3 x^{2} y + y^{3}| \leq 3 \sqrt{x^{2} + y^{2}}^{3}$，所以
$$
\lim_{(x,y) \to (0,0)} \Big|  \frac{-3 x^{2} y + y^{3}}{x^{2} +  y^{2}} \Big| \leq \lim_{(x,y) \to (0,0)} 3 \sqrt{x^{2} + y^{2}}
$$
由夹逼定理，这一项为0

但是第二项由复合极限定理可以证明不存在：

构造 $\Delta_{k} = (t, kt)$
$$
\lim_{t \to 0} f \circ \Delta_{k} (t) = \lim_{t \to 0} \frac{4k}{1 + k^{2}}  
$$
由对  $k$ 的依赖，所以极限不存在。

(3)
$$
\lim_{(x, y) \to (0, 0)} \frac{(1 + x^2 + y^2)^{1/(x^2 + y^2)} - e}{x^2 + y^2}
$$
其中 $e = \lim_{n \to +\infty} \left(1 + \frac{1}{n}\right)^n$。

利用复合极限：定义 $f(x, y)=x^{2}+y^{2}$ ， $g(t) = \frac{(1 + t)^{\frac{1}{t}} - e}{t}$

所以
$$
\lim_{(x, y) \to (0, 0)} \frac{(1 + x^2 + y^2)^{1/(x^2 + y^2)} - e}{x^2 + y^2} = \lim_{(x, y) \to (0, 0)} g \circ f = \lim_{t \to 0} g (t) = \lim_{t \to 0} \frac{(1 + t)^{\frac{1}{t}} - e}{t} \\ = 
\lim_{t \to 0} \frac{e^{\ln (1 + t) \frac{1}{t}} - e}{t} = \lim_{t \to 0} \left(\frac{1}{1 + t} \frac{1}{t} - \frac{1}{t^{2}} \ln (1 + t) \right) e^{\ln (1 + t) \frac{1}{t}} = - \frac{e}{2}
$$
验证复合极限的适用条件：

在 $(x, y) = (0, 0)$ 附近， $f(x, y)=x^{2}+y^{2} > 0$ ，所以上述复合极限成立。

(4) 求出所有实数 $a, b$ 及正数 $\alpha$，使得如下极限式成立：
$$
\lim_{(x, y) \to (0, 0)} \frac{ax + by}{(x^2 + y^2)^\alpha} = 0
$$

$\alpha < \frac{1}{2}$ ，上式对于所有实数 $a, b$ 成立。

证明：
$$
a x + b y \leq (a + b) \sqrt{x^{2} + y^{2}}
$$

$$
\lim_{(x, y) \to (0, 0)} \frac{ax + by}{(x^2 + y^2)^\alpha} \leq \lim_{(x,y) \to )(0,0)} (a + b) (x^{2} + y^{2})^{\frac{1}{2} - \alpha} = 0
$$

由夹逼定理，极限 $\lim_{(x, y) \to (0, 0)} \frac{ax + by}{(x^2 + y^2)^\alpha}$ 为0

证明当$\alpha \geq \frac{1}{2}$ 时，对于所有 $a,b$ 上述极限不存在：

利用复合极限，构造 $\Delta_{k} = (t, kt)$
$$
\lim_{t \to 0} (f \circ \Delta_{k}) (t) = \lim_{t \to 0} t^{1 - 2 \alpha} \frac{a + bk}{(1 + k^{2})^{\alpha}}
$$
显然，对于所有  $\alpha > \frac{1}{2}$ ，上述极限趋于 $\infty$，对于所有 $\alpha = \frac{1}{2}$ ，上述极限不存在。

所以当且仅当$\alpha < \frac{1}{2}$ ， $\lim_{(x, y) \to (0, 0)} \frac{ax + by}{(x^2 + y^2)^\alpha} = 0$ 对于所有实数 $a, b$ 成立。

5. 给定 $x_0 \in \mathbb{R}^n$。定义函数 $f : \mathbb{R}^n \to \mathbb{R}$ 为

$$
f(x) = d(x_0, x), \quad \forall x \in \mathbb{R}^n.
$$
证明：$f$ 是连续函数。

 $\forall \epsilon > 0, \exist \delta = \epsilon, s.t. \forall d (x_{1}, x) < \delta, |d(x_{0},x) -d (x_{0}, x_{1})| \leq d (x_{1}, x) < \delta = \epsilon$

所以$f$ 是连续函数。

6. 设 $D$ 是 $\mathbb{R}^n$ 的子集，$f, g : D \to \mathbb{R}$ 是连续函数。定义函数 $h : D \to \mathbb{R}$ 为

$$
h(x) = \min\{f(x), g(x)\}, \quad \forall x \in D.
$$
证明：$h$ 是连续函数。

证明：由于$f, g : D \to \mathbb{R}$ 是连续函数，由连续函数的定义
$$
\forall \epsilon > 0, \exist \delta_{1}, \delta_{2} , s.t. \forall d (x_{0}, x) < \delta_{1}, |f(x) -f (x_{0})| < \epsilon ; \forall d (x_{0}, x) < \delta_{2}, |g(x) - g (x_{0})| < \epsilon
$$

$$
\therefore \,\, \forall \epsilon > 0, \exist \delta = \min \{ \delta_{1}, \delta_{2} \}, s.t. \forall d (x_{0}, x) < \delta, |h(x) - h(x_{0})| \leq \max \{ |f(x) - h(x_{0})|, |g(x) - h(x_{0})| \} \\ \leq \max \{ |f(x) - f(x_{0})|, |g(x) - g(x_{0})| \} < \epsilon
$$

所以$h$ 是连续函数。# 高等微积分（2） 第4次作业

Chasse_neige

1. 设 $f : \mathbb{R}^2 \to \mathbb{R}$ 是连续函数, 当 $x^2 + y^2 \to +\infty$ 时, $f(x, y) \to +\infty$. 证明: $f$ 在 $\mathbb{R}^2$ 上有最小值, 即存在 $(x_0, y_0) \in \mathbb{R}^2$, 使得
$$
f(x, y) \geq f(x_0, y_0), \quad \forall (x, y) \in \mathbb{R}^2.
$$

证明：

因为当 $x^2 + y^2 \to +\infty$ 时, $f(x, y) \to +\infty$，所以$\forall A > 0, \exist N \in \N_{+}, s.t. \forall x^{2} + y^{2} > N, f(x, y) > A$

对于  $A = f(\vec{0})$，记相应的 $N$为 $N_{0}$ 。

根据最值定理，由于集合 $X = \{(x,y) \mid x^{2} + y^{2} \leq N \}$  为 $\R^{2}$ 上的有界闭集，所以在 $X$ 上 $f$ 存在最小值 $f_{min} \leq f (\vec{0})$

所以 $\forall x^{2} + y^{2} > N_{0}, f(x, y) > f (\vec{0}) \neq f_{min}$

所以$f$ 在 $\mathbb{R}^2$ 上有最小值 $f_{min}$。

2. 令 $S$ 为平面上的单位圆周

$$
S = \{(x, y) \mid x^2 + y^2 = 1\}.
$$
(1) 证明: $S$ 是 $\mathbb{R}^2$ 的闭集.

证明：证明 $S^{\complement}$是开集，即证明 $S^{\complement}$中的每一个点均为其内点即可。
$$
S^{\complement} = \{(x, y) \mid x^{2} + y^{2} \neq 1 \}
$$
对于 $x^{2} + y^{2} < 1$ 的点 $(x_{0}, y_{0})$，取 $r_{0} = \frac{1 - d(0, (x_{0}, y_{0}))}{2}$ ，则 $\forall a \in B_{r_{0}} (x_{0}, y_{0}), d(0, a) \leq d(0, (x_{0}, y_{0})) + r_{0} = 1 - r_{0} < 1$，所以 $(x_{0}, y_{0})$ 为 $S^{\complement}$ 内点

对于 $x^{2} + y^{2} > 1$ 的点 $(x_{0}, y_{0})$，取 $r_{0} = -\frac{1 - d(0, (x_{0}, y_{0}))}{2}$ ，则 $\forall a \in B_{r_{0}} (x_{0}, y_{0}), d(0, a) \geq d(0, (x_{0}, y_{0})) - r_{0} = 1 + r_{0} > 1$，所以 $(x_{0}, y_{0})$ 为 $S^{\complement}$ 内点

综上，$S^{\complement}$是开集，所以$S$ 是 $\mathbb{R}^2$ 的闭集

(2) 设 $f : \mathbb{R}^2 \to \mathbb{R}$ 是连续函数. 证明: $f$ 在 $S$ 上能取到最大值与最小值, 即存在 $(x_0, y_0), (x_1, y_1) \in S$, 使得
$$
f(x_0, y_0) \leq f(x, y) \leq f(x_1, y_1), \quad \forall (x, y) \in S
$$

利用反证法，记 $\sup f(x,y) = M, \inf f(x,y) = m \quad \forall  (x,y) \in S$，假设 $M,m \notin U, U = \{ f(x,y) \mid (x,y) \in S \}$：

由于$S$ 是 $\mathbb{R}^2$ 的闭集且有界，所以 $S$ 紧致，又因为 $f$ 为连续函数，所以  $U=\{f(x,y) \mid (x,y) \in S\}$是紧致的。所以 $M,m \notin U$代表$M,m \in U^{\complement} $，又因为 $U^{\complement}$ 为开集，所以 $M,m$为 $U^{\complement}$ 内点，所以 $\exist r_{M}, r_{m} > 0, s.t. B_{r_{m}}(m) \in U^{\complement},B_{r_{M}} (M) \in U^{\complement}$
$$
\therefore \,\, \sup f (x,y) \leq M - r_{M} \quad \inf f(x,y) \geq m + r_{m}
$$

与 $\sup f(x,y) = M, \inf f(x,y) = m \quad \forall  (x,y) \in S$ 矛盾。

所以$f$ 在 $S$ 上能取到最大值与最小值。


3. 对于二元函数 $f : \mathbb{R}^2 \to \mathbb{R}$, 判断如下断言是否正确, 并说明理由.
    (1) 如果 $f$ 在 $(x_0, y_0)$ 处可微, 则 $f$ 在 $(x_0, y_0)$ 处连续.
    
    正确。理由：$f$ 在 $(x_0, y_0)$ 处可微，所以存在线性映射 $\mathcal{L}$ 使得
    
    $$
    f (x_{0} + h_{1}, y_{0} + h_{2}) = f (x_{0}, y_{0}) + \mathcal{L} (\mathbf{h}) + \alpha (\mathbf{h})
    $$
    所以 在 $(x_0, y_0)$ 处 
    $$
    \lim_{\mathbf{h} \to 0} f(\mathbf{x} + \mathbf{h}) = \lim_{\mathbf{h} \to 0} f (x_{0}, y_{0}) + \mathcal{L} (\mathbf{h}) + \alpha (\mathbf{h}) = f(x_{0}, y_{0})
    $$
    所以 $f$ 在 $(x_0, y_0)$ 处连续。
    
    (2) 如果 $f$ 在 $(x_0, y_0)$ 处可微, 则 $f$ 在 $(x_0, y_0)$ 处有各个方向的方向导数.
    
    正确。理由：$f$ 在 $(x_0, y_0)$ 处可微，所以存在线性映射 $\mathcal{L}$ 使得
    $$
    f (x_{0} + h_{1}, y_{0} + h_{2}) = f (x_{0}, y_{0}) + \mathcal{L} (\mathbf{h}) + \alpha (\mathbf{h})
    $$
    所以 在 $(x_0, y_0)$ 处 
    $$
    \nabla_{\vec{V}} f = \frac{\partial}{\partial t} \mathcal{L} (\vec{V} t) + \alpha (\vec{V} t) \Big|_{t = 0}  = \mathcal{L} (\vec{V})
    $$
    所以所有方向导数存在。
    
    (3) 如果 $f$ 在 $(x_0, y_0)$ 处有各个方向的方向导数, 则 $f$ 在 $(x_0, y_0)$ 处连续.
    
    错误。反例：
    $$
    f(x, y) = 
    \begin{cases} 
    \dfrac{x^2 y}{x^4 + y^2} &  (x, y) \neq (0, 0) \\
    0 &  (x, y) = (0, 0)
    \end{cases}
    $$
    沿方向向量 $\mathbf{v} = (a, b)$（其中 $a^2 + b^2 = 1$），方向导数为：
    $$
    \nabla_{\mathbf{v}} f(0, 0) = \lim_{t \to 0} \frac{f(ta, tb) - f(0, 0)}{t}
    $$
    代入 $f(ta, tb) = \dfrac{(ta)^2 (tb)}{(ta)^4 + (tb)^2} = \dfrac{t^3 a^2 b}{t^4 a^4 + t^2 b^2} = \dfrac{t a^2 b}{t^2 a^4 + b^2}$
    
    所有方向导数均存在且为 $\frac{a^{2}}{b}$
    
    但是函数在原点不连续：
    
    沿抛物线路径 $y = x^2$ 趋近原点：
    $$
    \lim_{x \to 0} f(x, x^2) = \lim_{x \to 0} \dfrac{x^2 \cdot x^2}{x^4 + (x^2)^2} = \dfrac{x^4}{2x^4} = \dfrac{1}{2} \neq f(0, 0).
    $$
    因此，函数在原点处不连续。
    
    (4) 如果 $f$ 在 $(x_0, y_0)$ 处有各个方向导数, 则对任何方向 $q = (a, b)$, 有 
    $$
    \frac{\partial f}{\partial q}\bigg|_{(x_0,y_0)} = a\frac{\partial f}{\partial x}\bigg|_{(x_0,y_0)} + b\frac{\partial f}{\partial y}\bigg|_{(x_0,y_0)}
    $$
    不正确，反例：
    $$
    f (x, y) = \begin{cases} \frac{|y| \sqrt{x^{2} + y^{2}}}{x} \qquad (x \neq 0) \\ 0 \qquad (x = 0) \end{cases}
    $$
    对于 $(0,0)$ 处的方向导数 $\vec{V} = (\cos \theta, \sin \theta)$
    $$
    \nabla_{\vec{V}} f(0,0) = \begin{cases} 0 \qquad (\cos \theta = 0) \\ \frac{|\sin \theta|}{\cos \theta} \qquad (\cos \theta \neq 0)\end{cases}
    $$
    但是对于 $f$ 的偏导而言
    $$
    f'_{1} (0,0) = 0, \quad f'_{2} (0,0) = 0
    $$
    所以 $\frac{\partial f}{\partial q}\bigg|_{(x_0,y_0)} = a\frac{\partial f}{\partial x}\bigg|_{(x_0,y_0)} + b\frac{\partial f}{\partial y}\bigg|_{(x_0,y_0)}$ 并不成立。
    
    4. 设 $f(x, y) = \sqrt{|x^2 - y^2|}$ 在 $(0, 0)$ 处沿着哪些方向 $f$ 的方向导数存在?
    
       对于 $(0,0)$ 处的方向导数  $\vec{V} = (\cos \theta, \sin \theta)$：
       $$
       \nabla_{\vec{V} } f = \lim_{t \to 0} \frac{|t|}{t} \sqrt{|\cos^{2} \theta - \sin^{2} \theta|}
       $$
       所以对于所有 $\cos^{2} \theta = \sin^{2} \theta$ 的 $\theta$ 而言方向导数存在，即对于 $\theta = \frac{\pi}{4} $ 和 $\theta = \frac{3 \pi}{4}$ ,方向导数存在

4. 计算函数的各个偏导数.
    (1) $f(x, y) = xy$
$$
  f'_{1} = y, f'_{2} = x
$$
  (2) $f(x, y) = \arctan\left(\frac{y}{x}\right)$
$$
  f'_{1} = - \frac{y}{x^{2} + y^{2}},  f'_{2} = \frac{x}{x^{2} + y^{2}}
$$
  (3) $f(x_1, \ldots, x_n) = \sqrt{x_1^2 + \ldots + x_n^2}$
$$
  f'_{k} = \frac{x_{k}}{\sqrt{x_{1}^{2} + \cdots + x_{n}^{2}}} \qquad (1 \leq k \leq n)
$$

5. (1) $f(x, y) = \sqrt{|xy|}$ 在 $(0, 0)$ 处是否可微?

  不可微。理由：

   $f(x, y) = \sqrt{|xy|}$ 在 $(0, 0)$ 处的偏导
$$
  f'_{1} = f'_{2} = 0
$$
  但是
$$
  \lim_{(x,y) \to 0}  \sqrt{\abs{\frac{xy}{x^{2} + y^{2}}}} 
$$
  显然不存在，所以不可微。

  (2) 设 $f$ 在 $(0, 0)$ 点的某个开球邻域 $U$ 中有定义, 且满足 $|f(x, y)| \leq x^2 + y^2$, $\forall x, y \in U$. 证明: $f$ 在 $(0, 0)$ 处可微, 并计算它在 $(0, 0)$ 处的微分

  微分为0，理由：

  利用微分的定义$f$ 在 $(x_0, y_0)$ 处可微，所以存在线性映射 $\mathcal{L}$ 使得
$$
  f (x_{0} + h_{1}, y_{0} + h_{2}) = f (x_{0}, y_{0}) + \mathcal{L} (\mathbf{h}) + \alpha (\mathbf{h})
$$
  带入 $f (0,0) = 0$以及$|f(x, y)| \leq x^2 + y^2$ 可以作为 $\alpha (\mathbf{h})$，所以f$ 在 $(0, 0)$ 处的微分为0

  证明$|f(x, y)| \leq x^2 + y^2$ 可以作为 $\alpha (\mathbf{h})$可以作为误差项：
$$
  \lim_{(x, y) \to 0} \frac{|f (x, y)|}{\sqrt{x^{2} + y^{2}}}  \leq \lim_{(x, y) \to 0} \sqrt{x^{2} + y^{2}} = 0
$$
  (3) 设 $g$ 在 $(0, 0)$ 点的某个开球邻域 $U$ 中有定义, 且满足 $|g(x, y)| \leq \sqrt{x^2 + y^2}$, $\forall x, y \in U$. $g$ 在 $(0, 0)$ 处是否一定可微?

  不一定，反例：
$$
  g(x,y) = \begin{cases} \frac{xy}{\sqrt{x^2 + y^2}} \qquad (x \neq 0) \\ 0 \qquad (x = 0) \end{cases}
$$

$$
  \lim_{(x,y) \to 0} g(x,y) = \lim_{(x,y) \to 0} \frac{xy}{\sqrt{x^2 + y^2}}
$$

  不存在。

  $g$ 甚至不连续。

  ​	

  # 高等微积分 （2） 第5次作业

Chasse_neige

#### 1 

计算偏导数

(1) 设 $f \in C^1(\mathbb{R}, \mathbb{R})$, $z = xy + xf\left( \dfrac{y}{x} \right)$. 求 $x \dfrac{\partial z}{\partial x} + y \dfrac{\partial z}{\partial y}$
$$
x \dfrac{\partial z}{\partial x} + y \dfrac{\partial z}{\partial y} = x (y + f + x f' (- \frac{y}{x^{2}})) + y(x + x f' \frac{1}{x}) = 2 x y + x f
$$
(2) 设 $f \in C^2(\mathbb{R}^2, \mathbb{R})$, $z = f(x, xy)$. 求 $\dfrac{\partial^2 z}{\partial y^2}$
$$
\dfrac{\partial^2 z}{\partial y^2} = \frac{\partial}{\partial y} f'_{2} x = f''_{22} x^{2}
$$
(3) 设 $f, g \in C^2(\mathbb{R}, \mathbb{R})$, $z = xf\left( \dfrac{y}{x} \right) + yg\left( \dfrac{x}{y} \right)$. 求 $\dfrac{\partial^2 z}{\partial x \partial y}$
$$
\dfrac{\partial^2 z}{\partial x \partial y} = \frac{\partial}{\partial x} (x f' \frac{1}{x} + g + y g' (- \frac{x}{y^{2}})) = \frac{\partial}{\partial x} (f' + g - \frac{x}{y} g') \\ = - \frac{y}{x^{2}} f'' + \frac{1}{y} g' - \frac{1}{y} g' - \frac{x}{y^{2}} g'' = - \frac{y}{x^{2}} f'' - \frac{x}{y^{2}} g''
$$
(4) 设 $f \in C^1(\mathbb{R}, \mathbb{R})$, $z = \dfrac{y}{f(x^2 - y^2)}$. 求 $\dfrac{1}{x} \dfrac{\partial z}{\partial x} + \dfrac{1}{y} \dfrac{\partial z}{\partial y}$
$$
\dfrac{1}{x} \dfrac{\partial z}{\partial x} + \dfrac{1}{y} \dfrac{\partial z}{\partial y} = \frac{1}{x} ( - \frac{y}{f^{2}} f') 2x + \frac{1}{y} (\frac{1}{f} + \frac{y}{f^{2}} f' 2y) = \frac{1}{yf}
$$
(5) 设 $f \in C^1(\mathbb{R}^3, \mathbb{R})$, $u = f(x, xy, xyz)$. 求 $\dfrac{\partial u}{\partial x}, \dfrac{\partial u}{\partial y}, \dfrac{\partial u}{\partial z}$
$$
\frac{\partial u}{\partial x} = f'_{1} + y f'_{2} + yz f'_{3} \\
\frac{\partial u}{\partial y} = x f'_{2} + xz f'_{3} \\
\frac{\partial u}{\partial z} = xy f'_{3}
$$
这里, 我们称函数 $f : \mathbb{R}^n \rightarrow \mathbb{R}$ 是 $C^k$ 光滑的, 记作 $f \in C^k(\mathbb{R}^n, \mathbb{R})$, 如果 $f$ 的各个 $k$ 阶 (偏) 导函数都存在且连续.

#### 2 

给定 $C^1$ 光滑的函数 $F : \mathbb{R}^3 \rightarrow \mathbb{R}$. 求函数
$$
F(u^2 - x^2, u^2 - y^2, u^2 - z^2)
$$
对 $x, y, z, u$ 的偏导数
$$
\frac{\partial F}{\partial x} = -2x F'_{1} \\
\frac{\partial F}{\partial y} = -2y F'_{2} \\
\frac{\partial F}{\partial z} = -2z F'_{3} \\
\frac{\partial F}{\partial u} = 2u (F'_{1} + F'_{2} + F'_{3})
$$

#### 3 

给定 $n \times n$ 的对称实矩阵 $(A_{ij})_{1 \leq i,j \leq n}$(即对任何 $i, j$, 有 $A_{ij} = A_{ji}$). 定义二次函数
$$
Q(x_1, \ldots, x_n) = \sum_{i=1}^n \sum_{j=1}^n A_{ij} x_i x_j, \quad \forall (x_1, \ldots, x_n) \in \mathbb{R}^n
$$

(1) 求 $Q$ 的微分
$$
d Q = 2  \sum_{i=1}^n \sum_{j=1}^n A_{ij} x_i d x_j, \quad \forall (x_1, \ldots, x_n) \in \mathbb{R}^n
$$
(2) 设 $f : \mathbb{R}^n \rightarrow \mathbb{R}$ 是 $C^1$ 光滑的函数. 定义函数
$$
g(x_1, \ldots, x_n) = f(x_1, \ldots, x_n) e^{- \frac{1}{2} Q(x_1, \ldots, x_n)}.
$$
计算 $g$ 的各个偏导数 $\dfrac{\partial g}{\partial x_1}, \ldots, \dfrac{\partial g}{\partial x_n}$.

$$
\frac{\partial g}{\partial x_{k}} = f'_{k} e^{- \frac{1}{2} Q} - \frac{1}{2}  f  \sum_{i=1}^n \sum_{j=1}^n A_{ij} \delta_{ik} x_{j} + A_{ij} x_{i} \delta_{jk} e^{- \frac{1}{2} Q} =  f'_{k} e^{- \frac{1}{2} Q} - f  \sum_{i=1}^n A_{ik} x_{i} e^{- \frac{1}{2} Q}
$$

#### 4 

设 $f : \mathbb{R}^3 \rightarrow \mathbb{R}$ 是 $C^1$ 光滑的函数, 即 $f$ 的各个偏导数都存在且连续.

(1) 对于给定的点 $(x, y, z) \in \mathbb{R}^3$, 考虑关于 $t$ 的一元函数
$$
g(t) = f(tx, ty, tz).
$$
求 $g'(t)$
$$
g' (t) =  x f'_{1} + y f'_{2} + z f'_{3}
$$
(2) 证明: 对任何 $(x, y, z) \in \mathbb{R}^3$, 有
$$
f(x, y, z) = f(0, 0, 0) + x \int_0^1 f_x(tx, ty, tz) \, dt + y \int_0^1 f_y(tx, ty, tz) \, dt + z \int_0^1 f_z(tx, ty, tz) \, dt
$$

在本题 (3), (4) 小问中假设 $f$ 满足: 对任何 $(x, y, z) \in \mathbb{R}^3$ 都有
$$
x f_x(x, y, z) + y f_y(x, y, z) + z f_z(x, y, z) = n f(x, y, z),
$$
其中 $n$ 是某个给定的正整数.

证明：
$$
f (x, y, z) = g (1) = g (0) + \int_{0}^{1} g'(t) dt = g (0) + \int_{0}^{1} (x f'_{1} + y f'_{2} + z f'_{3}) dt \\ 
=  f(0, 0, 0) + x \int_0^1 f_x(tx, ty, tz) \, dt + y \int_0^1 f_y(tx, ty, tz) \, dt + z \int_0^1 f_z(tx, ty, tz) \, dt
$$
(3) 对于给定的点 $(x, y, z) \in \mathbb{R}^3$, 考虑关于 $t$ 的一元函数
$$
h(t) = \dfrac{f(tx, ty, tz)}{t^n}.
$$
求 $h'(t)$
$$
h' (t)  = \frac{x f'_{1} + y f'_{2} + z f'_{3}}{t^{n}} - n \frac{f}{t^{n + 1}}
$$
(4) 证明: 对任何 $(x, y, z) \in \mathbb{R}^3$ 与 $t > 0$, 都有
$$
f(tx, ty, tz) = t^n f(x, y, z)
$$

证明：

由于 $f$ 满足: 对任何 $(x, y, z) \in \mathbb{R}^3$ 都有
$$
x f_x(x, y, z) + y f_y(x, y, z) + z f_z(x, y, z) = n f(x, y, z),
$$
所以 $g' (1) = n g (1)$

对于一般的 $g (t)$ ，作换元 $x' = tx, y' = ty, z' =tz$，所以
$$
t g' (t) = n g (t) 
$$

$$
\frac{d g}{g} = n \frac{dt}{t}
$$

两遍同时积分
$$
\int_{g(1)}^{g(t)} \frac{dg}{g} = n \int_{1}^{t} \frac{dt}{t} \\
g (t) = t^{n} g (1)
$$
所以
$$
f(tx, ty, tz) = t^n f(x, y, z)
$$
## 高等微积分 （2） 第六次作业

Chasse_neige

#### 1

设 $x, y, z$ 满足方程 $x^3 + y^3 + z^3 + xyz = 4$.

(1) 证明: 在点 $(1, 1, 1)$ 附近, $z$ 可以表示成 $x, y$ 的隐函数.

证明：考虑该点处的偏导矩阵
$$
\frac{\partial F}{\partial z} \Bigg|_{(1, 1, 1)} = 3 z^{2} + xy = 4 \neq 0
$$
所以隐函数存在

(2) 把上述隐函数记作 $z = z(x, y)$, 求 $\left. \dfrac{\partial z}{\partial x} \right|_{(1,1)}, \left. \dfrac{\partial z}{\partial y} \right|_{(1,1)}$
$$
3 x^{2} + 3 z^{2} \frac{\partial z}{\partial x} + yz + xy \frac{\partial z }{\partial x} = 0
$$
带入$(x,y) = (1,1)$，$z = 1$ 
$$
3 + 3 \left. \dfrac{\partial z}{\partial x} \right|_{(1,1)} + 1 + \left. \dfrac{\partial z}{\partial x} \right|_{(1,1)} = 0
$$
所以
$$
\left. \dfrac{\partial z}{\partial x} \right|_{(1,1)} = -1
$$
同理
$$
3 y^{2} + 3 z^{2} \frac{\partial z}{\partial y} + xz + xy \frac{\partial z}{\partial y} = 0
$$
所以
$$
3 + 3 \left. \dfrac{\partial z}{\partial y} \right|_{(1,1)} + 1 + \left. \dfrac{\partial z}{\partial y} \right|_{(1,1)} = 0
$$

$$
\left. \dfrac{\partial z}{\partial y} \right|_{(1,1)} = -1
$$

(3) 求 $z(x, y)$ 在 $(1, 1)$ 附近带皮亚诺余项的泰勒公式, 要求展开至二次项, 即要求余项形如 $o \left( (\Delta x)^2 + (\Delta y)^2 \right)$.

二阶项
$$
\frac{\partial^{2} z}{\partial x^{2}} \Bigg|_{(1, 1)} = - \frac{\partial}{\partial x} \left(\frac{3 x^{2} + yz}{3 z^{2} + xy} \right) = - \frac{(6 x + y \frac{\partial z}{\partial x}) (3 z^{2} + xy) - (3 x^{2} + yz) (6 z \frac{\partial z}{\partial x} + y)}{(3 z^{2} + xy)^{2}} \\ =
- \frac{5 \cdot 4 - 4 \cdot (-5)}{4^{2}} = - \frac{5}{2}
$$

$$
\frac{\partial^{2} z}{\partial y \partial x} = - \frac{\partial}{\partial y} \left(\frac{3 x^{2} + yz}{3 z^{2} + xy} \right)  = - \frac{(z + y \frac{\partial z}{\partial y}) (3 z^{2} + xy) - (3 x^{2} + yz) (6 z \frac{\partial z}{\partial y} + x)}{(3 z^{2} + xy)^{2}} \\ = 
- \frac{0 - 4 \cdot (-5)}{4^{2}} = - \frac{5}{4}
$$

$$
\frac{\partial^{2} z}{\partial y^{2}} \Bigg|_{(1, 1)} = - \frac{\partial}{\partial y} \left(\frac{3 y^{2} + xz}{3 z^{2} + xy} \right) = - \frac{(6 y + x \frac{\partial z}{\partial x}) (3 z^{2} + xy) - (3 y^{2} + xz) (6 z \frac{\partial z}{\partial x} + x)}{(3 z^{2} + xy)^{2}} \\ =
- \frac{5 \cdot 4 - 4 \cdot (-5)}{4^{2}} = - \frac{5}{2}
$$
所以$z(x, y)$ 在 $(1, 1)$ 附近带皮亚诺余项的泰勒公式为
$$
z (x,y) = 1 - (x - 1)- (y - 1) - \frac{5}{4} (x - 1)^{2} - \frac{5}{4} (x - 1)(y - 1) - \frac{5}{4} (y - 1)^{2} + o (\Delta x^{2} + \Delta y^{2})
$$
#### 2 

设 $f, g : \mathbb{R}^2 \rightarrow \mathbb{R}$ 的各个 2 阶偏导函数都存在且连续, $g(x_0, y_0) = 0$, $g_y(x_0, y_0) \neq 0$. 设方程 $g(x, y) = 0$ 在 $(x_0, y_0)$ 附近确定 $C^2$ 光滑的隐函数 $y = y(x)$. 定义函数 $h : U \rightarrow \mathbb{R}$ 如下:
$$
h(x) = f(x, y(x)),
$$
其中 $U$ 是 $x_0$ 的某个邻域, $y = y(x)$ 在 $U$ 中有定义.

(1) 求导函数 $h'(x)$.

$$
h’ (x) = f’_{1} + f’_{2} \frac{\partial y}{\partial x}
$$

根据隐函数的性质

$$
\frac{\partial y}{\partial x} = - \frac{g_{x} (x_{0}, y_{0})}{g_{y} (x_{0}, y_{0})}
$$

所以

$$
h’ (x) = f’_{1} - f’_{2} \frac{g_{x} (x_{0}, y_{0})}{g_{y} (x_{0}, y_{0})}
$$
(2) 求 2 阶导函数 $h''(x)$.

$$
h’’ (x) = \frac{\partial}{\partial x} \left(f’_{1} (x, y (x)) + f’_{2} (x, y (x)) \frac{\partial y (x)}{\partial x} \right) \\ =
f’’_{11} + f’’_{21} \frac{\partial y}{\partial x} + f’’_{12} \frac{\partial y}{\partial x} + f’’_{22} (\frac{\partial y}{\partial x})^{2} + f’_{2} \frac{\partial^{2} y}{\partial x^{2}}
$$

带入$\frac{\partial y}{\partial x} = - \frac{g_{x} (x_{0}, y_{0})}{g_{y} (x_{0}, y_{0})}$ 以及 $\frac{\partial^{2} y}{\partial x^{2}} = - \frac{\partial}{\partial x} \frac{g_{x}}{g_{y}} = - \frac{g_{xx} g_{y} - g_{x} g_{xy}}{g_{y}^{2}}$

得到
$$
h'' (x) = f’’_{11} - 2  f’’_{21} \frac{g_{x}}{g_{y}} + f’’_{22} (\frac{g_{x}}{g_{y}})^{2} + f’_{2} \frac{g_{x} g_{xy} - g_{xx} g_{y}}{g_{y}^{2}}
$$

#### 3 

设 $L : \mathbb{R}^2 \rightarrow \mathbb{R}$ 是给定的 $C^2$ 光滑函数. 定义映射 $\phi : \mathbb{R}^2 \rightarrow \mathbb{R}^2$ 为:
$$
\phi(x, v) = \left( x, \dfrac{\partial L(x, v)}{\partial v} \right).
$$

(1) 求 $\phi$ 的 Jacobi 矩阵 $J(\phi)_{(x, v)}$
$$
J (\phi)_{(x, \nu)} = \begin{pmatrix} \frac{\partial x}{\partial x} & \frac{\partial x}{\partial \nu} \\ \frac{\partial}{\partial x} \frac{\partial L (x, \nu)}{\partial \nu} & \frac{\partial}{\partial \nu} \frac{\partial L (x, \nu)}{\partial \nu}  \end{pmatrix} \\ =
\begin{pmatrix} 1 & 0 \\ \frac{\partial^{2} L (x, \nu)}{\partial x \partial \nu} & \frac{\partial^{2} L (x, \nu)}{\partial \nu^{2}} \end{pmatrix}
$$
(2) 证明: 如果 $\dfrac{\partial^2 L(x, v)}{\partial v^2} \neq 0$, 则 $\phi$ 在 $(x, v)$ 附近有 $C^1$ 光滑的逆映射. 以下我们假定 $\phi$ 有整体的 $C^1$ 光滑的逆 $\phi^{-1}$, 并把它记作:
$$
\phi^{-1}(q, p) = (x(q, p), v(q, p)),
$$
显然 $x(q, p) = q$

证明

由于$\dfrac{\partial^2 L(x, v)}{\partial v^2} = 0$, 则 
$$
\det J (\phi)_{(x, \nu)} = \frac{\partial^{2} L}{\partial v^{2}} \neq 0
$$
所以 $d f$ 存在逆 $d^{-1} f$

根据反函数定理，映射$\phi$ 存在整体的 $C^1$ 光滑的逆 $\phi^{-1}$

(3) 定义函数 $H(q, p) = p \cdot v(q, p) - L(x(q, p), v(q, p))$, 计算
$$
\dfrac{\partial H}{\partial q}, \dfrac{\partial H}{\partial p}
$$

$$
\frac{\partial H}{\partial q} = \frac{\partial}{\partial q} ( p \cdot v(q, p) - L(x(q, p), v(q, p))) = p \frac{\partial v}{\partial q} - \frac{\partial L}{\partial x} \frac{\partial x}{\partial q} - \frac{\partial L}{\partial v} \frac{\partial v}{\partial q}
$$

带入 $x = q, \quad p = \frac{\partial L}{\partial v}$
$$
\frac{\partial H}{\partial q} = - \frac{\partial L}{\partial x}
$$

$$
\frac{\partial H}{\partial p}  = \frac{\partial }{\partial p} ( p \cdot v(q, p) - L(x(q, p), v(q, p))) = v + p \frac{\partial v}{\partial p} - \frac{\partial L}{\partial x} \frac{\partial x}{\partial p} - \frac{\partial L}{\partial v} \frac{\partial v}{\partial p} = v
$$

(4) 对于 $C^1$ 光滑映射 $\gamma : \mathbb{R} \rightarrow \mathbb{R}^2$, $\gamma(t) = (x(t), v(t))$, 把复合映射 $\phi \circ \gamma : \mathbb{R} \rightarrow \mathbb{R}^2$ 记作:
$$
\phi \circ \gamma(t) = (q(t), p(t)).
$$
证明: $(x(t), v(t)$ 满足 Euler-Lagrange 方程
$$
\begin{cases}
v(t) = \dfrac{dx(t)}{dt} \\
\dfrac{d}{dt} \dfrac{\partial L(x(t), v(t))}{\partial v} = \dfrac{\partial L(x(t), v(t))}{\partial x}
\end{cases}
$$
的充分必要条件是 $q(t), p(t)$ 满足 Hamilton 方程
$$
\begin{cases}
\dfrac{dq(t)}{dt} = \dfrac{\partial H(q(t), p(t))}{\partial p} \\
\dfrac{dp(t)}{dt} = -\dfrac{\partial H(q(t), p(t))}{\partial q}
\end{cases}
$$

证明

充分性：假设满足哈密顿方程
$$
(x (t), \frac{\partial L}{\partial v} (t)) = \phi (x (t), v (t)) = (q (t), p (t))
$$
所以
$$
\frac{d}{d t} p (t) = \frac{d}{d t} \frac{\partial L}{\partial v} = - \dfrac{\partial H}{\partial q} = \frac{\partial L}{\partial x}
$$
即
$$
\dfrac{d}{dt} \dfrac{\partial L(x(t), v(t))}{\partial v} = \dfrac{\partial L(x(t), v(t))}{\partial x}
$$
同理
$$
\frac{d}{d t} q (t) = \frac{d}{d t} x = \frac{\partial H}{\partial p} = v
$$
即
$$
\frac{d}{d t} x (t) = v (t)
$$
必要性：假设满足拉格朗日方程，则由（3）的结论
$$
\frac{\partial H (q (t), p(t))}{\partial q} = - \frac{\partial L}{\partial x} = - \frac{d}{d t} \frac{\partial L}{\partial v} = - \frac{d}{d t} p (t)
$$

$$
\frac{\partial H (q (t), p (t))}{\partial p} = v = \frac{d}{d t} x = \frac{d}{d t} q (t)
$$

#### 4 

设 $U, V$ 是 $\mathbb{R}^n$ 的开集. 已知 $f : U \rightarrow V$ 是 $C^1$ 光滑的双射, 且其逆映射 $f^{-1} : V \rightarrow U$ 是连续的.

(1) 证明: 如果在 $x_0 \in U$ 处 $f$ 的雅可比矩阵 $J_f(x_0)$ 是可逆矩阵. 证明: $f^{-1}$ 在 $f(x_0)$ 处可微.

证明

由于$f : U \rightarrow V$ 是 $C^1$ 光滑的双射, 所以其逆映射 $f^{-1} : V \rightarrow U$ 是 $C^{1}$ 的。

所以 $f^{-1}$ 在 $f(x_0)$ 处可微。这样说有点耍赖，我还是把反函数定理里的证明复述一遍吧

作平移以及换元使得$\bar{f} (0) = \bar{f}^{-1} (0) = 0$， $J_{\bar{f}} (0) = J_{\bar{f}^{-1}} (0) = I_{d}$

所以
$$
\bar{f} (u_{0} + h) = \bar{f} (u_{0}) + h + \alpha (h) \qquad \lim_{|h| \to 0} \frac{\alpha (h)}{|h|} = 0
$$

$$
\bar{f}^{-1} (v_{0} + v) = \bar{f}^{-1} (v_{0}) + v + \beta (v) 
$$

证明
$$
\lim_{|v| \to 0} \frac{\beta (v)}{|v|} = \lim_{|v| \to 0} \frac{\bar{f}^{-1} (v_{0} + v) - \bar{f}^{-1} (v_{0}) - v}{|v|} = 0
$$
即可

作换元 $\bar{f} (u_{0}) = v_{0}, \bar{f} (u_{0} + h) = v_{0} + v, \quad h = \bar{f}^{-1} (\bar{f} (u_{0}) + v) - u_{0}$
$$
\lim_{|v| \to 0} \frac{\beta (v)}{|v|} = \lim_{|v| \to 0} \frac{h - v}{|v|} = \lim_{|h| \to 0 } \frac{- \alpha (h)}{|h + \alpha (h)|} = 0
$$
所以 $\bar{f}^{-1}$ 在 $\bar{f}(u_0)$ 处可微，所以 $f^{-1}$ 在 $f(x_0)$ 处可微

(2) 假设对任何 $x \in U$, $f$ 的雅可比矩阵 $J_f(x)$ 都是可逆矩阵. 证明: $f^{-1} : V \rightarrow U$ 是 $C^1$ 光滑映射

证明

已经证明任何 $x \in U$, $f^{-1}$ 在 $f(x_0)$ 处可微，又因为$J_f(x)$ 是可逆矩阵，因为$f : U \rightarrow V$ 是 $C^1$ 光滑的，所以$J_{f}$ 的矩阵元都是连续函数

利用链式法则
$$
J_{f^{-1}} (y) = (J_{f} (f^{-1} (y)))^{-1}
$$
由于$J_f(x)$ 是可逆的所以$J_{f^{-1}} (y)$ 的矩阵元均连续，所以对任何 $x \in U$, $f^{-1}$ 各个分量的偏导均是连续的，所以$f^{-1} : V \rightarrow U$ 是 $C^1$ 光滑映射。# 高等微积分（2） 第7次作业

Chasse_neige

#### 1  
设 $f(x, y) = (2 + \sin x) \cdot \sin y$，令 $D = \{(x, y)|0 < x, y < 2\pi\}$。

(1) 求出 $f$ 在 $D$ 上的所有临界点。
$$
\frac{\partial}{\partial x} f = \cos x \sin y = 0
$$

$$
x = \frac{\pi}{2}, \frac{3 \pi}{2} 
$$

或
$$
y = \pi
$$

$$
\frac{\partial}{\partial y} f = (2 + \sin x) \cos y = 0
$$

$$
y = \frac{\pi}{2} ,\frac{3 \pi}{2}
$$

所以一共有四个临界点
$$
(x,y) = (\frac{\pi}{2}, \frac{\pi}{2}), (\frac{3 \pi}{2}, \frac{\pi}{2}), (\frac{\pi}{2}, \frac{3 \pi}{2}), (\frac{3 \pi}{2}, \frac{3 \pi}{2})
$$
(2) 判断上述每个临界点是否为 $f$ 的极值点。如果是的话，请指出它是极大值点还是极小值点。
$$
\frac{\partial^{2}}{\partial x^{2}} f = - \sin x \sin y \\
\frac{\partial^{2}}{\partial x \partial y} f = \frac{\partial^{2}}{\partial y \partial x} f = \cos x \cos y \\
\frac{\partial^{2}}{\partial y^{2}} f = - (2 + \sin x) \sin y
$$
对于 $(x, y) = (\frac{\pi}{2}, \frac{\pi}{2})$
$$
\frac{\partial^{2}}{\partial x^{2}} f = -1 < 0 \\
\frac{\partial^{2}}{\partial x \partial y} f = 0 \\
\frac{\partial^{2}}{\partial y^{2}} f = -3 < 0
$$
该点的 $H_{f}$ 负定，所以该点为极小值点

对于 $(x, y) = (\frac{3 \pi}{2}, \frac{\pi}{2})$
$$
\frac{\partial^{2}}{\partial x^{2}} f = 1 > 0 \\
\frac{\partial^{2}}{\partial x \partial y} f = 0 \\
\frac{\partial^{2}}{\partial y^{2}} f = -1 < 0
$$
该点的 $H_{f}$ 不定，所以该点并非极值点

对于 $(x, y) = (\frac{\pi}{2}, \frac{3 \pi}{2})$
$$
\frac{\partial^{2}}{\partial x^{2}} f = 1 > 0 \\
\frac{\partial^{2}}{\partial x \partial y} f = 0 \\
\frac{\partial^{2}}{\partial y^{2}} f = 3 > 0
$$
该点的 $H_{f}$ 正定，所以该点为极大值点

对于 $(x, y) = (\frac{3 \pi}{2}, \frac{3 \pi}{2})$
$$
\frac{\partial^{2}}{\partial x^{2}} f = -1 < 0 \\
\frac{\partial^{2}}{\partial x \partial y} f = 0 \\
\frac{\partial^{2}}{\partial y^{2}} f = 1 > 0
$$
该点的 $H_{f}$ 不定，所以该点并非极值点

#### 2  
设 $f(x, y, z) = x + y + z + xyz$，令 $B = \{(x, y, z)|x^2 + y^2 + z^2 \leq 1\}$。

(1) 证明：$f$ 在 $B$ 上有最大值。

证明

显然 $B$ 有界，并且 $f$ 为 $B$ 上的连续函数

再证明 $B^{\complement}$ 为开集
$$
\forall \vec{x} \in B^{\complement}, \exist \delta = \frac{|\vec{x}| - 1}{2}, s.t. B_{\delta} (\vec{x}) \subseteq B^{\complement}
$$
所以 $B^{\complement}$ 为开集，即 $B$ 为闭集，所以 $B$ 是紧致的。

又因为 $f$ 为 $B$ 上的连续函数，所以$f$ 在 $B$ 上有最大值。

(2) 利用拉格朗日（Lagrange）乘子法求出 $f$ 在 $B$ 上的最大值。

证明 $f$ 在 $B$ 上的最大值在 $\partial B$ 上

在 $\overset{\circ}{B}$ 上，$f$ 的临界点满足
$$
1 + yz = 0 \\
1 + xz = 0 \\
1 + xy = 0 \\
$$
所以 $xy = xz = yz = -1$ ，即 $(xyz)^{2} = -1$，在实数范围内无解，所以 $f$ 在 $\overset{\circ}{B}$ 上没有极值点，所以最大值在 $\partial B$ 上

利用拉格朗日乘子法
$$
L = x + y + z + xyz - \lambda (x^{2} + y^{2} + z^{2} - 1)
$$
所以极值点满足
$$
1 + yz - 2 \lambda x = 0 \\
1 + xz - 2 \lambda y = 0 \\
1 + xy - 2 \lambda z = 0 \\
x^{2} + y^{2} + z^{2} = 1
$$
所以
$$
3 + xy + xz + yz = 2 \lambda (x + y + z) \\
\frac{5}{2} + \frac{1}{2} (x + y + z)^{2} - 2 \lambda (x + y + z) = 0 \\
(x + y + z)^{2} - 4 \lambda (x + y + z) + 5 = 0 
$$
解得
$$
x + y + z =  2 \lambda \pm \sqrt{4 \lambda^{2} - 5}
$$
由上方程组的对称性，解应当满足 $x = y = z$，所以极值点有
$$
(x, y, z) = (\frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3}) \text{or} (-\frac{\sqrt{3}}{3}, -\frac{\sqrt{3}}{3}, -\frac{\sqrt{3}}{3})
$$
带入原函数
$$
f (\frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3}, \frac{\sqrt{3}}{3}) = \sqrt{3} + \frac{\sqrt{3}}{9} = \frac{10}{9} \sqrt{3} \\
f (-\frac{\sqrt{3}}{3}, -\frac{\sqrt{3}}{3}, -\frac{\sqrt{3}}{3}) = - \frac{10}{9} \sqrt{3} < \frac{10}{9} \sqrt{3}
$$
所以 $f$ 在 $B$ 上的最大值为 $\frac{10}{9} \sqrt{3}$ 

####  3  
设 $x, y, z$ 满足两个约束条件 $x + y + z = 1, x^2 + y^2 + z^2 = 1$。求函数 $f(x, y, z) = xyz$ 的最小值。
$$
L = xyz - \lambda_{1} (x + y + z - 1) - \lambda_{2} (x^{2} + y^{2} + z^{2} - 1)
$$
所以极值点满足
$$
yz - \lambda_{1} - 2 \lambda_{2} x = 0 \\
xz - \lambda_{1} - 2 \lambda_{2} y = 0 \\
xy - \lambda_{1} - 2 \lambda_{2} z = 0 \\
x + y + z = 1 \\
x^{2} + y^{2} + z^{2} = 1
$$
所以
$$
xy + xz + yz = 3 \lambda_{1} + 2 \lambda_{2}  \\
(x + y + z)^{2} = 1 + 6 \lambda_{1} + 4 \lambda_{2} = 1
$$
所以
$$
3 \lambda_{1} + 2 \lambda_{2} = 0
$$
然后进行暴力计算
$$
(xyz)^{2} = (\lambda_{1} + 2 \lambda_{2} x) (\lambda_{1} + 2 \lambda_{2} y) (\lambda_{1} + 2 \lambda_{2} z) \\ =
\lambda_{1}^{3} + 8 \lambda_{2}^{3} xyz + 2 \lambda_{1}^{2} \lambda_{2} (x + y + z) + 4 \lambda_{1} \lambda_{2}^{2} (xy + xz + yz) \\ =
\lambda_{1}^{3} + 8 \lambda_{2}^{3} xyz + 2 \lambda_{1}^{2} \lambda_{2} = \lambda_{1}^{3} (1 - 27 xyz - 3)
$$

$$
xyz (x + y + z) = (\lambda_{1} + 2 \lambda_{2} x) (\lambda_{1} + 2 \lambda_{2} y) + (\lambda_{1} + 2 \lambda_{2} x) (\lambda_{1} + 2 \lambda_{2} z) + (\lambda_{1} + 2 \lambda_{2} y) (\lambda_{1} + 2 \lambda_{2} z) \\
xyz = 3 \lambda_{1}^{2} + 4 \lambda_{1} \lambda_{2} = -3 \lambda_{1}^{2}
$$

所以
$$
9 \lambda_{1}^{4} + \lambda_{1}^{3} (2 - 81 \lambda_{1}^{2}) = 0 \\ 
\lambda_{1} = \frac{1 \pm 3}{18}
$$
所以函数 $f(x, y, z) = xyz$ 的最小值为
$$
xyz = -3 (\frac{1 + 3}{18})^{2} = - \frac{4}{27}
$$

#### 4  
给定整数 $n \geq 2$，定义 $(n - 1)$ 维球面为 
$$
S = \{(x_1, ..., x_n) \in \mathbb{R}^n | \sum_{i=1}^{n} x_i^2 = 1\}
$$
设 $f : \mathbb{R}^n \to \mathbb{R}$ 是 $C^1$ 光滑映射，$(\overline{x}_1, ..., \overline{x}_n) \in S$ 是 $f$ 在 $S$ 上的最大值点，即对任何 $(x_1, ..., x_n) \in S$，有 
$$
f(x_1, ..., x_n) \leq f(\overline{x}_1, ..., \overline{x}_n)
$$
证明：$f$ 在 $(\overline{x}_1, ..., \overline{x}_n)$ 处的梯度方向平行于向量 $(\overline{x}_1, ..., \overline{x}_n)$，即存在实数 $\lambda$，使得 
$$
\left( \frac{\partial f}{\partial x_1}, ..., \frac{\partial f}{\partial x_n} \right) |_{(\overline{x}_1, ..., \overline{x}_n)} = \lambda (\overline{x}_1, ..., \overline{x}_n)
$$
证明$S$ 是紧致的，显然 $S$ 有界，再说明 $S$ 为闭集，即 $S^{\complement}$是开集，即证明 $S^{\complement}$中的每一个点均为其内点即可。
$$
S^{\complement} = \{(x_1, ..., x_n) \in \mathbb{R}^n | \sum_{i=1}^{n} x_i^2 \neq 1\}
$$
对于 $\sum_{ i = 1}^{n} x_{i}^{2} < 1$ 的点 $x_{0}$，取 $r_{0} = \frac{1 - d(0, x_{0})}{2}$ ，则 
$$
\forall a \in B_{r_{0}} (x_{0}), d(0, a) \leq d(0, x_{0}) + r_{0} = 1 - r_{0} < 1
$$
所以 $x_{0}$ 为 $S^{\complement}$ 内点

对于 $\sum_{ i = 1}^{n} x_{i}^{2} > 1$ 的点 $x_{0}$，取 $r_{0} = - \frac{1 - d(0, x_{0})}{2}$ ，则 
$$
\forall a \in B_{r_{0}} (x_{0}), d(0, a) \geq d(0, x_{0}) - r_{0} = 1 - r_{0} > 1
$$
所以 $x_{0}$ 为 $S^{\complement}$ 内点

所以 $S$ 紧致，显然 $g$ 对于坐标的偏导不全为0，所以对于题给条件，拉格朗日定理成立，即极值点$(\overline{x}_1, ..., \overline{x}_n) \in S$ 满足
$$
L (x_{1}, x_{2}, \cdots, x_{n}, \lambda) = f (x_{1}, x_{2}, \cdots, x_{n}) - \lambda (\sum_{i = 1}^{n} x_{i}^{2} - 1) \\ 
\nabla L = \vec{0}
$$
所以
$$
\nabla f = 2 \lambda (\overline{x}_1, ..., \overline{x}_n)^{T}
$$
即
$$
\left( \frac{\partial f}{\partial x_1}, ..., \frac{\partial f}{\partial x_n} \right) |_{(\overline{x}_1, ..., \overline{x}_n)} = \lambda (\overline{x}_1, ..., \overline{x}_n)
$$

#### 5  

设 $n$ 元函数 $f(x_1, ..., x_n), g(x_1, ..., x_n)$ 与一元函数 $x_1(t), ..., x_n(t)$ 都是 $C^2$ 光滑的定义函数 
$$
h(t) = f(x_1(t), ..., x_n(t))
$$
(1) 求 $h''(t)$，请用 $f(x_1, ..., x_n)$ 与 $x_1(t), ..., x_n(t)$ 的高阶（偏）导函数表示。  
$$
h' (t) = \sum_{i = 1}^{n}  x'_{i} (t) \frac{\partial}{\partial x_{i}} f
$$

$$
h'' (t) = \sum_{i = 1}^{n}  x''_{i} (t) \frac{\partial}{\partial x_{i}} f +  \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (t) x'_{j} (t) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} f
$$

(2) 令 $p = (x_1(0), ..., x_n(0))$。假设 $p$ 是函数 $f(x_1, ..., x_n)$ 在约束条件 $g(x_1, ..., x_n) = 0$ 下的条件极值点。请叙述此情形下的拉格朗日乘子法。  
$$
L = f(x_1, ..., x_n) - \lambda g(x_1, ..., x_n)
$$
条件极值点满足
$$
\left. \nabla f \right|_{x_{i} = x_{i} (0), 1 \leq i \leq n } = \lambda \left. \nabla g \right|_{x_{i} = x_{i} (0), 1 \leq i \leq n } \\ 
g (x_{1} (0), \cdots, x_{n} (0)) = 0
$$
(3) 设 $\lambda \in \mathbb{R}$ 满足 (2) 中所述拉格朗日乘子法的结论，定义 $n$ 元函数 $F$ 为 
$$
F(x_1, ..., x_n) = f(x_1, ..., x_n) - \lambda g(x_1, ..., x_n)
$$
证明：如果对任何 $t$，都有 $g(x_1(t), ..., x_n(t)) = 0$，则 
$$
h''(0) =  \left. \sum_{i=1}^n \sum_{j=1}^n \frac{\partial^2 F}{\partial x_i \partial x_j} \right|_\mathbf{p}  x_i'(0)  x_j'(0)
$$
证明：已知
$$
h'' (0) = \left. \sum_{i = 1}^{n}  x''_{i} (0) \frac{\partial}{\partial x_{i}} f \right|_{\mathbf{p}} + \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} f \right|_{\mathbf{p}}
$$
由于
$$
\left. \frac{\partial^2 F}{\partial x_i \partial x_j} \right|_\mathbf{p} = \left. \frac{\partial^2 f}{\partial x_i \partial x_j} \right|_\mathbf{p}  - \lambda \left. \frac{\partial^2 g}{\partial x_i \partial x_j} \right|_\mathbf{p}
$$
所以
$$
h'' (0) = \left. \sum_{i = 1}^{n}  x''_{i} (0) \frac{\partial}{\partial x_{i}} f \right|_{\mathbf{p}} - \lambda  \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} g \right|_{\mathbf{p}} + \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} F \right|_{\mathbf{p}}
$$
因为 $n$ 元函数 $f(x_1, ..., x_n), g(x_1, ..., x_n)$ 与一元函数 $x_1(t), ..., x_n(t)$ 都是 $C^2$ 光滑的定义函数 ，所以导数顺序可以交换

因为对任何 $t$，都有 $g(x_1(t), ..., x_n(t)) = 0$，所以
$$
g'' (t) = 0
$$
所以
$$
g'' (t) = \sum_{i = 1}^{n}  x''_{i} (t) \frac{\partial}{\partial x_{i}} g +  \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (t) x'_{j} (t) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} g = 0
$$
所以
$$
\lambda  \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} g \right|_{\mathbf{p}} = - \lambda \left. \sum_{i = 1}^{n}  x''_{i} (t) \frac{\partial}{\partial x_{i}} g \right|_{\mathbf{p}}
$$
因为
$$
\left. \nabla f \right|_{x_{i} = x_{i} (0), 1 \leq i \leq n } = \lambda \left. \nabla g \right|_{x_{i} = x_{i} (0), 1 \leq i \leq n }
$$
所以
$$
- \lambda \left. \sum_{i = 1}^{n}  x''_{i} (t) \frac{\partial}{\partial x_{i}} g \right|_{\mathbf{p}} = - \left. \sum_{i = 1}^{n}  x''_{i} (t) \frac{\partial}{\partial x_{i}} f \right|_{\mathbf{p}}
$$
所以
$$
h'' (0) = \left. \sum_{i = 1}^{n}  x''_{i} (0) \frac{\partial}{\partial x_{i}} f \right|_{\mathbf{p}} - \lambda  \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} g \right|_{\mathbf{p}} + \left. \sum_{i = 1}^{n}  \sum_{j = 1}^{n} x'_{i} (0) x'_{j} (0) \frac{\partial^{2}}{\partial x_{j} \partial x_{i}} F \right|_{\mathbf{p}} \\ =
\left. \sum_{i=1}^n \sum_{j=1}^n \frac{\partial^2 F}{\partial x_i \partial x_j} \right|_\mathbf{p}  x_i'(0)  x_j'(0)
$$

#### 6  

设 $f, g \in C^1(\mathbb{R}^2, \mathbb{R})$，令 $D = \{(x, y)|g(x, y) \geq 0\}$。设 $g(x_0, y_0) = 0$ 且 $g_x(x_0, y_0), g_y(x_0, y_0)$ 不全为零，且对任何 $(x, y) \in D$ 有 $f(x_0, y_0) \leq f(x, y)$。

证明：存在非负实数 $\lambda$，使得 
$$
\begin{cases}  
f_x(x_0, y_0) - \lambda g_x(x_0, y_0) = 0, \\  
f_y(x_0, y_0) - \lambda g_y(x_0, y_0) = 0.  
\end{cases}
$$
证明
由于 $g(x_0, y_0) = 0 $ 且 $ \nabla g(x_0, y_0) \neq 0 $ ，根据隐函数定理，存在邻域  $U$  和唯一 $C^1$  函数  $y = \varphi(x) $，使得 $g(x, \varphi(x)) = 0$ 对所有 $ x \in U$ 成立。 
$$
h'(x_0) = f_x(x_0, y_0) + f_y(x_0, y_0) \varphi'(x_0) = 0
$$

根据隐函数定理，$\varphi'(x_0) = -\frac{g_x(x_0, y_0)}{g_y(x_0, y_0)} $
$$
f_x - f_y \cdot \frac{g_x}{g_y} = 0
$$

令  $\lambda = \frac{f_{y} (x_{0}, y_{0})}{g_{y} (x_{0}, y_{0})}$，则
$$
\begin{cases}  
f_x(x_0, y_0) - \lambda g_x(x_0, y_0) = 0, \\  
f_y(x_0, y_0) - \lambda g_y(x_0, y_0) = 0.  
\end{cases}
$$
由于 $(x_0, y_0) $$ 是 $$ f $ 在 $ D $ 上的极小值点，沿梯度 $\nabla g$ 方向
$$
\nabla f \cdot \frac{\nabla g}{\|\nabla g\|} \geq 0.
$$
结合 $\nabla f = \lambda \nabla g $
$$
\lambda \|\nabla g\|^2 \geq 0 \quad \implies \quad \lambda \geq 0.
$$

## 高等微积分（2） 第8次作业

Chasse_neige

1.给定 $0 < a < b, 0 < c < d$，设四条曲线 $xy = a, xy = b, y = cx$ 以及 $y = dx$ 在第一象限内围成的平面区域为 $D$。计算 $D$ 的面积。

作换元
$$
u = xy \\
v = \frac{y}{x}
$$
此时积分区域 $\Phi^{-1} (D)$ 变为 $u \in [a,b], v \in [c,d]$

利用换元公式
$$
S = \iint_{D} dx dy = \iint_{\Phi^{-1} (D)} \begin{vmatrix} y & - \frac{y}{x^{2}} \\ x & \frac{1}{x} \end{vmatrix}^{-1} du dv \\ =
\iint_{\Phi^{-1} (D)} \begin{vmatrix} \sqrt{uv} & - \frac{v}{\sqrt{\frac{u}{v}}} \\ \sqrt{\frac{u}{v}} & \frac{1}{\sqrt{\frac{u}{v}}} \end{vmatrix}^{-1} du dv = \iint_{\Phi^{-1} (D)} \frac{1}{2v} du dv \\ =
\frac{b - a}{2} \ln \frac{d}{c}
$$
2.设四条曲线 $x^2 - y^2 = 1, x^2 - y^2 = 4, \frac{x^2}{4} + y^2 = 1$ 以及 $\frac{x^2}{4} + y^2 = 4$ 在第一象限内围成的平面区域为 $D$。计算积分
$$
\iint_D \frac{xy}{x^2 - y^2} dxdy
$$

作换元
$$
u = x^{2} - y^{2} \\
v = \frac{x^{2}}{4} + y{2}
$$
此时积分区间变为 $\Phi^{-1} (D)$ ，即 $u \in [1,4], v \in [1,4]$            

利用换元公式
$$
\iint_D \frac{xy}{x^2 - y^2} dxdy = \iint_{\Phi^{-1} (D)} (f \circ \Phi) \det (J_{\Phi}) du dv \\ =
\iint_{\Phi^{-1} (D)} \frac{\frac{4}{5} \sqrt{(u + v) (v - \frac{u}{4})}}{u} \begin{vmatrix} \frac{1}{\sqrt{5 (u + v)}} & - \frac{1}{4} \frac{1}{\sqrt{5 (v - \frac{u}{4})}} \\ \frac{1}{\sqrt{5 (u + v)}} & \frac{1}{\sqrt{5 (v - \frac{u}{4})}} \end{vmatrix} du dv \\ =
\iint_{\Phi^{-1} (D)} \frac{1}{5u} du dv = \frac{6}{5} \ln 2
$$
3.给定 $a, b, c > 0$，令
$$
V = \{(x, y, z) | \frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} \leq 1, z \geq 0\}
$$
计算三重积分
$$
\iiint_V zdxdydz
$$

作换元
$$
x = a r \sin \theta \cos \phi \\
y = b r \sin \theta \sin \phi \\
z = c r \cos \theta
$$
其中 $r \in [0,1], \theta \in [0, \frac{\pi}{2}] , \phi \in [0, 2 \pi)$

利用换元公式
$$
\iiint_V zdxdydz = \iiint_{\Phi^{-1} (V)} (f \circ \Phi) \det (J_{\Phi}) dr d\theta d\phi \\ =
\iiint_{\Phi^{-1} (V)} c r \cos \theta abc r^{2} \sin \theta dr d \theta d \phi \\ = 
\iiint_{\Phi^{-1} (V)}abc^{2} r^{3} dr \sin \theta \cos \theta d \theta d \phi \\ =
abc^{2} \cdot \frac{1}{4} \cdot \frac{1}{2} \cdot 2 \pi = \frac{\pi}{4} abc^{2}
$$
4.考虑三维区域
$$
V = \{(x, y, z) | x^2 + y^2 + z^2 + xy + yz + zx \leq 1\}
$$
计算 $V$ 的体积 (提示: 把 $V$ 的定义式配方, 然后适当换元)
$$
x^2 + y^2 + z^2 + xy + yz + zx \leq 1  \\
(\frac{\sqrt{2}}{2} x + \frac{\sqrt{2}}{2} y)^{2} + (\frac{\sqrt{2}}{2} y + \frac{\sqrt{2}}{2} z)^{2} + (\frac{\sqrt{2}}{2} x + \frac{\sqrt{2}}{2} z)^{2} \leq 1
$$
所以作换元
$$
u = \frac{\sqrt{2}}{2} y + \frac{\sqrt{2}}{2} z \\
v = \frac{\sqrt{2}}{2} x + \frac{\sqrt{2}}{2} z \\
w = \frac{\sqrt{2}}{2} x + \frac{\sqrt{2}}{2} y
$$
利用换元公式
$$
\iiint_V dxdydz = \iiint_{\Phi^{-1} (V)} (f \circ \Phi) \det (J_{\Phi}) du dv dw \\ =
\iiint_{\Phi^{-1} (V)} \begin{vmatrix} 0 & \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} \\
\frac{\sqrt{2}}{2} & 0 & \frac{\sqrt{2}}{2} \\
\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} & 0 \end{vmatrix}^{-1} du dv dw \\ = 
\frac{1}{\frac{\sqrt{2}}{2}} \cdot \frac{4 \pi}{3} = \frac{4 \sqrt{2} \pi}{3}
$$
5.设 $f$ 在矩形区域 $[a, b] \times [c, d]$ 上连续，且有连续的偏导函数 $\frac{\partial f}{\partial x}$。

(1) 证明: 对任何 $x_0 \in [a, b]$，有
$$
\int_c^d f(x_0, y) dy = \int_c^d f(a, y) dy + \int_a^{x_0} dx \int_c^d \frac{\partial f(x, y)}{\partial x} dy
$$

证明

定义函数 $g (x) = f (x, y_{0})$

容易得知
$$
\left. \frac{d}{dx} g (x) \right|_{x = x_{0}} = \left. \frac{\partial f}{\partial x} \right|_{ (x,y) = (x_{0}, y_{0})}
$$
由于偏导数 $\frac{\partial f}{\partial x}$ 连续，所以 $g'$ 连续，对 $g (x)$ 使用一元的 N-L 公式
$$
g (x_{0}) = g (a) + \int_{a}^{x_{0}} g' (x) dx 
$$
所以
$$
f (x_{0}, y)  = f (a, y) + \int_{a}^{x_{0}} \frac{\partial f (x, y)}{\partial x} dx
$$

$$
\int_{c}^{d} f (x_{0}, y) dy = \int_{c}^{d} f(a, y) dy + \int_{c}^{d} dy \int_{a}^{x_{0}} \frac{\partial f (x, y)}{\partial x} dx
$$

由于偏导数 $\frac{\partial f}{\partial x}$ 连续，所以它可积。利用 Fubini 定理
$$
\int_{c}^{d} dy \int_{a}^{x_{0}} \frac{\partial f (x, y)}{\partial x} dx = \int_a^{x_0} dx \int_c^d \frac{\partial f(x, y)}{\partial x} dy
$$
所以
$$
\int_c^d f(x_0, y) dy = \int_c^d f(a, y) dy + \int_a^{x_0} dx \int_c^d \frac{\partial f(x, y)}{\partial x} dy
$$
(2) 对每个 $x \in [a, b]$，定义函数 $g(x) = \int_c^d f(x, y) dy$。证明: $g'(x) = \int_c^d \frac{\partial f(x, y)}{\partial x} dy$。

证明
$$
g' (x)  = \lim_{h \to 0} \frac{g (x + h) - g (x)}{h} = \lim_{h \to 0} \frac{1}{h} \left( \int_{c}^{d} f (x + h, y) dy - \int_{c}^{d} f (x, y) dy \right) \\ = 
\lim_{h \to 0} \int_{c}^{d} \frac{f (x + h, y) - f(x, y)}{h} dy
$$
现在证明积分和极限符号的可交换性

由微分中值定理，存在 $\theta \in [0, 1]$，使得 
$$
\frac{f (x + h, y) - f(x, y)}{h} = \frac{\partial}{\partial x} f (x + \theta h, y)
$$
由于偏导 $\frac{\partial f}{\partial x}$ 在闭区间上连续，所以原函数一定可积
$$
g' (x) = \lim_{h \to 0} \int_{c}^{d} \frac{\partial}{\partial x} f (x + \theta h, y) dy
$$
利用 $\frac{\partial f}{\partial x}$ 的连续性与（1）中的结论
$$
\lim_{h \to 0} \int_{c}^{d} \frac{\partial}{\partial x} f (x + \theta h, y) dy = \int_{c}^{d} \frac{\partial}{\partial x} f (x, y) dy + \lim_{h \to 0} \int_{x}^{x + \theta h} dx \int_{c}^{d} \frac{\partial f}{\partial x} (x, y) dy
$$
二最后一项显然为 $0$ 。所以
$$
g'(x) = \int_c^d \frac{\partial f(x, y)}{\partial x} dy
$$
6.设 $D$ 是 $Oxy$ 平面中的区域，其面积为 $S$。定义以 $D$ 为底面，$(0,0,1)$ 为顶点的锥体为
$$
V = \{(1-t)(u,v,0) + t(0,0,1)|(u,v,0) \in D, t \in [0,1]\}
$$
求 $V$ 的体积，要求答案用 $S$ 表示。
$$
V = \iiint_{V} dx dy dz
$$
现在作如下换元
$$
x = (1 - t) u \\
y = (1 - t) v \\
z = t
$$
且满足 $(u,v,0) \in D, t \in [0,1]$

利用换元公式
$$
V = \iiint_{\Phi^{-1} (V)} \det (J_{\Phi}) du dv dt \\ = 
\iiint_{\Phi^{-1} (V)} \begin{vmatrix} 1 - t & 0 & 0 \\ 0 & 1 - t & 0 \\ -u & -v & 1 \end{vmatrix} du dv dt \\ =
\iiint_{\Phi^{-1} (V)} (1 - t)^{2} du dv dt = \iint_{D} du dv \int_{0}^{1} (1 - t)^{2} dt = \frac{1}{3} S
$$
7.给定非负整数 $a,b,c$。令
$$
Q = \{(x,y,z) \in R^3 | x+y+z \leq 1, x \geq 0, y \geq 0, z \geq 0\}
$$
计算三重积分
$$
\iiint_Q x^ay^bz^c dxdydz
$$
利用 Fubini 定理的推论
$$
\iiint_{Q} x^{a} y^{b} z^{c} dx dy dz = \int_{0}^{1} z^{c} dz \iint_{D_{z}} x^{a} y^{b} dx dy \\ =
\int_{0}^{1} z^{c} dz \int_{0}^{1 - z} y^{b} dy \int_{0}^{1 - z - y} x^{a} dx \\ = 
\int_{0}^{1} z^{c} dz \int_{0}^{1 - z} \frac{1}{1 + a} y^{b} (1 - z -y)^{a + 1} dy \\ =
\frac{1}{a + 1} \int_{0}^{1} z^{c} dz \int_{0}^{1 - z} y^{b} \sum_{n = 0}^{a + 1} C_{a + 1}^{n} (1 - z)^{n} (- y)^{a + 1 - n} dy \\ = 
\frac{1}{a + 1} \int_{0}^{1} z^{c} dz \sum_{n = 0}^{a + 1} C_{a + 1}^{n} (1 - z)^{n} (-1)^{a + 1 - n}  \frac{1}{a + b + 2 - n} (1 - z)^{a + b + 2 - n} \\ =
\frac{1}{a + 1}  \sum_{n = 0}^{a + 1} C_{a + 1}^{n} \frac{(-1)^{a + 1 - n}}{a + b + 2 - n} \int_{0}^{1} z^{c} (1 - z)^{a + b + 2} dz
$$
因为
$$
\int_{0}^{1} z^{c} (1 - z)^{a + b + 2} = \left. \frac{1}{c + 1} z^{c + 1} (1 - z)^{a + b + 2} \right|_{z = 0}^{z = 1} + \frac{a + b + 2}{c + 1} \int_{0}^{1} z^{c + 1} (1 - z)^{a + b + 1} dz \\ = \frac{a + b + 2}{c + 1} \int_{0}^{1} z^{c + 1} (1 - z)^{a + b + 1} dz
$$
一直迭代下去
$$
\int_{0}^{1} z^{c} (1 - z)^{a + b + 2} = \frac{a + b + 2}{c + 1} \cdot \frac{a + b + 1}{c + 2} \cdots  \frac{1}{a + b + c + 2} \int_{0}^{1} z^{a + b + c + 2} dz = \frac{(a + b + 2)! c!}{(a + b + c + 3)!}
$$
所以原积分等于
$$
\iiint_{Q} x^{a} y^{b} z^{c} dx dy dz  \\ =
\sum_{n = 0}^{a + 1} \frac{1}{a + 1}  C_{a + 1}^{n} \frac{(-1)^{a + 1 - n}}{a + b + 2 - n} \frac{(a + b + 2)! c!}{(a + b + c + 3)!} \\ = 
\sum_{n = 0}^{a + 1} \frac{(a + 1)!}{n! (a + 1 - n)!} \frac{(a + b + 2)! c!}{(a + b + c + 3)!} \frac{(-1)^{a + 1 - n}}{(a + 1) (a + b + 2 - n)} \\ =
\frac{a! c! (a + b + 2)!}{(a + b + c + 3)!} \sum_{n = 0}^{a + 1} \frac{(-1)^{n}}{n! (a + 1 - n)! (b + 1 + n)} \\ = 
\frac{a! c!}{(a + b + c + 3)!} \sum_{n = 0}^{a + 1} \frac{(-1)^{n} (b + n)!}{n!} C_{a + b + 2}^{a + 1 - n} \\ = 
\frac{a! b! c!}{(a + b + c + 3)!} \sum_{n = 0}^{a + 1} (-1)^{n} C_{b + n}^{b} C_{a + b + 2}^{b + 1 + n}
$$
在计算最后的求和，注意到
$$
\sum_{k = 0}^{\infty} (-1)^{k} C_{b + k}^{b} x^{k} = \frac{1}{(1 + x)^{b + 1}}
$$

$$
\sum_{l = 0}^{a + b + 2} C_{a + b + 2}^{l} x^{l} = (1 + x)^{a + b + 2}
$$

所以
$$
\sum_{k = 0}^{\infty} \sum_{l = 0}^{a + b + 2} (-1)^{k} C_{b + k}^{b} C_{a + b + 2}^{l} x^{k + l} = \sum_{n = 0}^{\infty}  \sum_{k = \max \{0, n - (a + b + 2) \}}^{n} (-1)^{k} C_{b + k}^{b} C_{a + b + 2}^{n - k} x^{n} = (1 + x)^{a + 1} = \sum_{n = 0}^{a + 1} C_{a + 1}^{n} x^{n}
$$
所以令 $n= a + 1$，对比系数
$$
C_{a + 1}^{a + 1} = \sum_{k = 0}^{a + 1} (-1)^{k} C_{b + k}^{b} C_{a + b + 2}^{a + 1 - k} = 1
$$
所以最终结果为
$$
\iiint_{Q} x^{a} y^{b} z^{c} dx dy dz  = \frac{a! b! c!}{(a + b + c + 3)!}
$$
## 高等微积分（2） 第9次作业

Chasse_neige

#### 1 

##### (1)

设 $S$ 是椭球面 
$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1
$$
请用二重积分表示 $S$ 的面积（不必计算该积分）。

对椭球面做如下参数化
$$
x = a \sin \theta \cos \phi \\
y = b \sin \theta \sin \phi \\
z = c \cos \theta
$$
所以
$$
x_{\theta} = a \cos \theta \cos \phi, y_{\theta} = b \cos \theta \sin \phi, z_{\theta} = - c \sin \theta \\
x_{\phi} = - a \sin \theta \sin \phi, y_{\phi} = b \sin \theta \cos \phi, z_{\phi} = 0
$$

$$
S = \iint d S = \iint \begin{vmatrix}  \begin{pmatrix} a \cos \theta \cos \phi, b \cos \theta \sin \phi, - c \sin \theta \end{pmatrix} \times \begin{pmatrix} - a \sin \theta \sin \phi, b \sin \theta \cos \phi, 0 \end{pmatrix} \end{vmatrix} d \theta d \phi \\ =
\iint \sqrt{(bc \sin^{2} \theta \cos \phi)^{2} + (ac \sin^{2} \theta \sin \phi)^{2} + (ab \sin \theta \cos \theta)^{2}} d \theta d \phi \\ =
\iint \sqrt{b^{2} c^{2} \sin^{2} \theta \cos^{2} \phi + a^{2} c^{2} \sin^{2} \theta \sin^{2} \phi + a^{2} b^{2} \cos^{2} \theta} \sin \theta d \theta d \phi
$$

##### (2)
计算球面 $x^2 + y^2 + z^2 = R^2$ 的面积。

取 $a = b = c = R$
$$
S = R^{2} \iint  \sin \theta d \theta d \phi = 2 \pi R^{2} \int_{-1}^{1} dx = 4 \pi R^{2}
$$

#### 2
设 $\Sigma$ 为质量均匀的上半球面  
$$
\Sigma = \{(x, y, z) | x^2 + y^2 + z^2 = 1, z \geq 0\}
$$

求出 $\Sigma$ 的质心位置，即计算 
$$
\left( \frac{\iint_{\Sigma} x \, dS}{\iint_{\Sigma} dS}, \frac{\iint_{\Sigma} y \, dS}{\iint_{\Sigma} dS}, \frac{\iint_{\Sigma} z \, dS}{\iint_{\Sigma} dS} \right)
$$
由对称性，显然有
$$
\frac{\iint_{\Sigma} x \, dS}{\iint_{\Sigma} dS} = \frac{\iint_{\Sigma} y \, dS}{\iint_{\Sigma} dS} = 0
$$

$$
\frac{\iint_{\Sigma} z \, dS}{\iint_{\Sigma} dS} = \frac{1}{2 \pi} \iint \cos \theta \sin \theta d \theta d \phi = \int_{0}^{\frac{\pi}{2}} \cos \theta \sin \theta d \theta = \frac{1}{2}
$$

#### 3

给定 $a > b > 0$，定义曲面 $T$ 为  
$$
T = \{(x, y, z) \in \mathbb{R}^3 | (\sqrt{x^2 + y^2} - a)^2 + z^2 = b^2\}
$$
求 $T$ 的面积。

显然，$T$ 是双层曲面

做如下参数化
$$
x = (b \cos \theta + a) \sin \phi \\ 
y = (b \cos \theta + a) \cos \phi \\
z = b \sin \theta
$$
其中，参数取值范围 $\theta \in [0, \pi], \phi \in [0, 2 \pi)$所以
$$
x_{\theta} = - b \sin \theta \sin \phi, y_{\theta} = - b \sin \theta \cos \phi, z_{\theta} = b \cos \theta \\
x_{\phi} = (b \cos \theta + a) \cos \phi, y_{\phi} = - (b \cos \theta + a) \sin \phi, z_{\phi} = 0
$$
面积
$$
S = \iint |(-b \sin \theta \sin \phi, -b \sin \theta \cos \phi, b \cos \theta) \times ((b \cos \theta + a) \cos \phi, - (b \cos \theta + a) \sin \phi, 0)| d \theta d \phi \\ =
\iint \sqrt{(b^{2} \cos^{2} \theta + ab \cos \theta)^{2} \sin^{2} \phi + (b^{2} \cos^{2} \theta + ab \cos \theta)^{2} \cos^{2} \phi + (b^{2} \sin \theta \cos \theta + ab \sin \theta)^{2}} d \theta d \phi \\ =
\iint \sqrt{b^{4} \cos^{2} \theta + 2 ab^{3} \cos \theta + a^{2} b^{2}} d \theta d \phi \\ =
\iint b (b \cos \theta + a) d \theta d \phi = 2 \pi b \int_{0}^{\pi} (b \cos \theta + a) d \theta = 2 \pi^{2} ab 
$$


#### 4

令 $S$ 为单位球面 
$$
S = \{(x, y, z) | x^2 + y^2 + z^2 = 1\}
$$

设 $p : [0, 1] \to S$ 是 $C^1$ 光滑映射  
$$
p(t) = (x(t), y(t), z(t)), \quad \forall t \in [0, 1]
$$

假设 $p(0) = (0, 0, -1), \, p(1) = (0, 0, 1)$，且对任何 $0 < t < 1$ 有 $-1 < z(t) < 1$。

##### (1)
证明：对任何 $t \in [0, 1]$，有  
$$
x(t)x'(t) + y(t)y'(t) + z(t)z'(t) = 0
$$
证明
$$
x^{2} (t) + y^{2} (t) + z^{2} (t) = 1
$$

$$
\frac{d}{dt} (x^{2} (t) + y^{2} (t) + z^{2} (t)) = 0
$$

所以
$$
x(t)x'(t) + y(t)y'(t) + z(t)z'(t) = 0
$$

##### (2)

证明：对任何 $0 < t < 1$，有  
$$
x'(t)^2 + y'(t)^2 \geq \frac{z(t)^2}{x(t)^2 + y(t)^2} z'(t)^2
$$
证明

由 Cauchy 不等式
$$
(x^{2} + y^{2}) (x'^{2} + y'^{2}) \geq (x x' + y y')^{2} = (- z z')^{2}
$$
所以
$$
x'(t)^2 + y'(t)^2 \geq \frac{z(t)^2}{x(t)^2 + y(t)^2} z'(t)^2
$$

##### (3)
定义 $p$ 的弧长为 
$$
L = \int_0^1 \sqrt{x'(t)^2 + y'(t)^2 + z'(t)^2} \, dt
$$

证明：$L \geq \pi$

证明
$$
L = \int_0^1 \sqrt{x'(t)^2 + y'(t)^2 + z'(t)^2} \, dt \geq \int_{0}^{1} \sqrt{\frac{z(t)^2}{x(t)^2 + y(t)^2} z'(t)^2 + z'^{2} (t)} \, dt \\ =
\int_{0}^{1} \frac{|z' (t)|}{\sqrt{x^{2} (t) + y^{2} (t)}} dt = \int_{0}^{1} \sqrt{\frac{z'^{2} (t)}{1 - z^{2} (t)}} dt \\ \geq 
\int_{0}^{1} \frac{z' (t)}{\sqrt{1 - z^{2} (t)}} dt = \int_{-1}^{1} \frac{dz}{\sqrt{1 - z^{2}}} = \pi
$$

#### 5
给定正数 $c < \sqrt{2}$。设曲面 $S = \{(x, y, z) | x^2 + y^2 + z^2 = 1, x + y \geq c\}$。

##### (1)
计算第一型曲面积分 $\iint_S x \, dS$，其中 $dS$ 表示面积微元。

作换元
$$
\begin{pmatrix} u \\ v \\ w \end{pmatrix} = \begin{pmatrix} 
\frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} & 0 \\
- \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} & 0 \\
0 & 0 & 1
\end{pmatrix}
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$
由于变换矩阵是正交阵，所以面积元不变
$$
x = \frac{\sqrt{2}}{2} (u - v)
$$
再换到球坐标下
$$
u = \cos \theta \\
v = \sin \theta \sin \phi \\
w = \sin \theta \cos \phi
$$
所以积分范围为 $\theta \in [0, \arccos \frac{\sqrt{2}}{2} c], \phi \in [0, 2 \pi]$
$$
\iint_{S} x dS = \iint_{S} \frac{\sqrt{2}}{2} (\cos \theta - \sin \theta \sin \phi) \sin \theta d \theta d \phi \\ =
\frac{\sqrt{2}}{2} \cdot 2 \pi \int_{0}^{\arccos \frac{\sqrt{2}}{2} c} \cos \theta \sin \theta d \theta \\ = \sqrt{2} \pi \cdot \frac{1}{2} (1 - \frac{c^{2}}{2}) = \frac{\sqrt{2}}{2} \pi (1 - \frac{c^{2}}{2})
$$

##### (2)
计算第一型曲线积分 $\int_{\partial S} x \, dl$，其中 $\partial S$ 表示 $S$ 的边界，$dl$ 表示弧长微元

参数化边界，由于边界上 $u = \frac{\sqrt{2}}{2} c $
$$
l: (\frac{\sqrt{2}}{2} c, \sqrt{1 - \frac{c^{2}}{2}} \sin \phi, \sqrt{1 - \frac{c^{2}}{2}} \cos \phi)
$$
所以
$$
\int_{\partial S} x \, dl = \int_{0}^{2 \pi} \frac{\sqrt{2}}{2} (\frac{\sqrt{2}}{2} c - \sqrt{1 - \frac{c^{2}}{2}} \sin \phi) \sqrt{1 - \frac{c^{2}}{2}} d \phi = \pi c \sqrt{1 - \frac{c^{2}}{2}}
$$


#### 6
设 $C = \{(x, y) | x^2 + y^2 = 1\}$ 是平面上的单位圆周，取逆时针定向（方向）。

##### (1)
计算第二型曲线积分 
$$
B(u) = \oint_C \frac{-y \, dx + x \, dy}{(x^2 + y^2 + u^2)^{3/2}}
$$
参数化
$$
x = \cos \theta \\
y = \sin \theta
$$

$$
B(u) = \oint_C \frac{-y \, dx + x \, dy}{(x^2 + y^2 + u^2)^{3/2}} = \int_{0}^{2 \pi} \frac{ \sin^{2} \theta + \cos^{2} \theta}{(1 + u^{2})^{\frac{3}{2}}} d \theta = \frac{2 \pi}{(1 + u^{2})^{\frac{3}{2}}}
$$

##### (2)
计算极限 
$$
\lim_{A \to +\infty} \int_{-A}^A B(u) \, du
$$

$$
\lim_{A \to +\infty} \int_{-A}^A B(u) \, du = \lim_{A \to \infty} \int_{-A}^{A} \frac{2 \pi}{\cosh^{3} \theta} d (\sinh \theta) \\ =
\lim_{A \to \infty} \int_{- A}^{A} \frac{2 \pi}{\cosh^{2} \theta} d \theta = 4 \pi
$$

#### 7
计算 
$$
\oint_L xy \, dx + yz \, dy + zx \, dz
$$

其中 $L$ 为曲线  
$$
\begin{cases}  
x^2 + y^2 + z^2 = 1 \\  
x + y + z = 1  
\end{cases}
$$
积分方向从 $(1, 0, 0)$ 沿着劣弧指向 $(0, 1, 0)$

同样先做正交变换
$$
\begin{pmatrix} u \\ v \\ w \end{pmatrix} = \begin{pmatrix} 
\frac{\sqrt{3}}{3} & \frac{\sqrt{3}}{3} & \frac{\sqrt{3}}{3} \\
- \frac{\sqrt{2}}{2} & \frac{\sqrt{2}}{2} & 0 \\
\frac{\sqrt{6}}{6} & \frac{\sqrt{6}}{6} & - \frac{\sqrt{6}}{3}
\end{pmatrix}
\begin{pmatrix} x \\ y \\ z \end{pmatrix}
$$

$$
\begin{pmatrix} x \\ y \\ z \end{pmatrix} = \begin{pmatrix} 
\frac{\sqrt{3}}{3} & - \frac{\sqrt{2}}{2} & \frac{\sqrt{6}}{6} \\
\frac{\sqrt{3}}{3} & \frac{\sqrt{2}}{2} & \frac{\sqrt{6}}{6} \\
\frac{\sqrt{3}}{3} & 0 & - \frac{\sqrt{6}}{3}
\end{pmatrix}
\begin{pmatrix} u \\ v \\ w \end{pmatrix}
$$

所以利用 Stokes 公式
$$
\nabla \times (xy, yz, zx) = - (y, z, x)
$$

$$
\oint_L xy \, dx + yz \, dy + zx \, dz = \iint_{S} - (y, z, x) \cdot \frac{\sqrt{3}}{3} (1, 1, 1) dS \\ = - \frac{\sqrt{3}}{3} \iint_{S} d S = - \frac{2 \sqrt{3} \pi}{9}
$$

#### 8
设 $a, b, c$ 为给定的正数，$S$ 为椭球面 
$$
\frac{x^2}{a^2} + \frac{y^2}{b^2} + \frac{z^2}{c^2} = 1
$$

取指向外面的定向。对于正整数 $n$，计算第二型曲面积分 
$$
I_n = \iint_S (x^n \, dy \, dz + y^n \, dz \, dx + z^n \, dx \, dy)
$$
对椭球面做如下参数化
$$
x = a \sin \theta \cos \phi \\
y = b \sin \theta \sin \phi \\
z = c \cos \theta
$$
所以利用 Gauss 公式
$$
I_n = \iint_S (x^n \, dy \, dz + y^n \, dz \, dx + z^n \, dx \, dy) \\ = \iiint_{V} n (x^{n - 1} + y^{n - 1} + z^{n - 1}) dx dy dz \\ =
n abc \iiint_{V} (a^{n - 1} r^{n - 1} \sin^{n - 1} \theta \cos^{n - 1} \phi + b^{n - 1} r^{n - 1} \sin^{n - 1} \theta \sin^{n - 1} \phi + c^{n - 1}  r^{n - 1} \cos^{n - 1} \theta) r^{2} \sin \theta dr d \theta d \phi \\ =
\frac{2n \pi}{n + 2} abc \int_{0}^{\pi} \int_{0}^{2 \pi} (a^{n - 1} \sin^{n - 1} \theta \cos^{n - 1} \phi + b^{n - 1} \sin^{n - 1} \theta \sin^{n - 1} \phi + c^{n - 1}  \cos^{n - 1} \theta)  \sin \theta d \theta d \phi \\ =
\frac{2n \pi}{n + 2} abc  ((a^{n - 1} + b^{n - 1}) 2 \frac{(n - 2)!!}{n!!} + c^{n - 1} \frac{2}{n}) \\ = 
\frac{4 \pi}{n + 2} abc (a^{n - 1} + b^{n - 1} + c^{n + 1})
$$
## 高等微积分（2） 第10次作业  
Chasse_neige

#### 1  

定义曲面 $S$ 为 
$$
S = \{(x, y, z) \mid x^2 + y^2 \leq 1, x + y + z = 1\}
$$
取指向 $z$ 轴正方向的定向（或者用课本上的术语，选定了曲面的上侧）
(1) 计算第二型曲面积分  
$$
\iint_S x^2 \, dy \, dz + y^2 \, dz \, dx + z^2 \, dx \, dy
$$
利用 $x, y$ 对原曲面进行参数化，则第二型曲面积分简化为
$$
\iint_S x^2 \, dy \, dz + y^2 \, dz \, dx + z^2 \, dx \, dy = \iint_{D}  ((1 - x - y)^{2}, y^{2}, x^{2}) \cdot ((1, 0, -1) \times (0, 1, -1)) dx \, dy \\ = 
\iint_{D} ((1 - x - y)^{2}, y^{2}, x^{2}) \cdot (1, 1, 1) dx \, dy = \iint_{D} (1 + 2 x^{2} + 2 y^{2} - 2x - 2y + 2xy) dx \, dy \\ =
\pi + \pi - 0  = 2 \pi
$$
(2) 设 $S$ 的边界为 $\partial S$，赋予边界的正定向。计算第二型曲线积分  
$$
\int_{\partial S} z^2 \, dx + x^2 \, dy + y^2 \, dz
$$
同样使用参数化 $z = 1 - x - y, x = \cos \theta, y = \sin \theta$ ，则第二型曲面积分化为
$$
\int_{\partial S} z^2 \, dx + x^2 \, dy + y^2 \, dz = \int_{0}^{2 \pi} ((1 - x - y)^{2}, x^{2}, y^{2}) \cdot (- \sin \theta, \cos \theta, \sin \theta - \cos \theta) d \theta \\ = 
\int_{0}^{2 \pi} (- (1 - \cos \theta - \sin \theta)^{2} \sin \theta + \cos^{3} \theta + \sin^{3} \theta - \cos \theta \sin^{2} \theta) d \theta = 2 \pi
$$

#### 2  

设 $C \subset \mathbb{R}^2$ 是光滑的闭曲线，取逆时针方向（定向）。假设 $(0, 0) \notin C$，计算第二型曲线积分  
$$
\oint_C \frac{-(x^2 y + y^3) \, dx + (x^3 + x y^2) \, dy}{(x^2 + y^2)^2}
$$
由于$C \subset \mathbb{R}^2$ 是光滑的闭曲线，所以 $C$ 可以参数化。假设 
$$
x = x (t) \\
y = y (t)
$$
其中 $t \in [0,1]$ 是一个参数化

注意到
$$
\left(\arctan (\frac{y}{x}) \right)' = \frac{- yx' + xy'}{x^{2} + y^{2}} = \frac{-(x^2 y + y^3) x' + (x^3 + x y^2) y'}{(x^2 + y^2)^2}
$$
则第二型曲线积分化为
$$
\oint_C \frac{-(x^2 y + y^3) \, dx + (x^3 + x y^2) \, dy}{(x^2 + y^2)^2} = \int_{0}^{1} \frac{-(x^2 y + y^3) x' + (x^3 + x y^2) y'}{(x^2 + y^2)^2} dt = \int_{0}^{1} \left(\arctan (\frac{y}{x}) \right)' dt \\= 
\begin{cases} 
0  \qquad (\text{原点不在曲线内})\\
2 \pi \qquad (\text{原点在曲线内})
\end{cases}
$$
第3 题需要用到如下事实：设 $f$ 在矩形区域 $[a, b] \times [c, d]$ 上连续，且有连续的偏导函数 $\frac{\partial f}{\partial x}$。对每个 $x \in [a, b]$，定义函数 $g(x) = \int_c^d f(x, y) \, dy$，则有 $g'(x) = \int_c^d \frac{\partial f(x,y)}{\partial x} \, dy$。  

#### 3  
给定$(x_0, y_0) \in \mathbb{R}^2$。对于正数 $r$，令 $C(r) = \{(x, y) \mid (x - x_0)^2 + (y - y_0)^2 = r^2\}$。设$f$ 在区域 $D(R) = \{(x, y) \mid (x - x_0)^2 + (y - y_0)^2 \leq R^2\}$ 上是光滑函数，定义函数$g(r)$ 为如下的第一型曲线积分  
$$
g(r) = \frac{1}{2\pi r} \int_{C(r)} f(x, y) \, ds, \quad \forall 0 < r \leq R,
$$
其中 $ds$ 表示弧长微元。 
(1) 利用前述事实，证明：对任何 $0 < r \leq R$，有  
$$
g'(r) = \frac{1}{2\pi r} \int_{C(r)} -f_y(x,y) \, dx + f_x(x,y) \, dy
$$
其中 $C(r)$ 取逆时针定向。

证明

第一型曲线积分
$$
g(r) = \frac{1}{2\pi r} \int_{C(r)} f(x, y) \, ds = \frac{1}{2 \pi r} \int_{C (r)} f (x_{0} + r \cos \theta, y_{0} + r \sin \theta) r d \theta
$$

$$
g' (r) = \frac{1}{2 \pi} \int_{C (r)} \frac{\partial f}{\partial r} d \theta = \frac{1}{2 \pi} \int_{C (r)} f_{x} \cos \theta + f_{y} \sin \theta d \theta \\ = 
\frac{1}{2 \pi r} \int_{C (r)} f_{x} d (y_{0} + r \sin \theta) - f_{y} d (x_{0} + r \cos \theta) = \frac{1}{2\pi r} \int_{C(r)} -f_y(x,y) \, dx + f_x(x,y) \, dy
$$

(2) 设 $x_0^2 + y_0^2 > R^2$。计算 $\frac{1}{2\pi R} \int_{C(R)} \ln(x^2 + y^2) \, ds$。  
$$
g (r) = \frac{1}{2\pi r} \int_{C(r)} \ln(x^2 + y^2) \, ds
$$
利用2的结论，由于原点不在 $C (r)$ 内
$$
g' (r) = \frac{1}{2 \pi r} \int_{C (r)} - \frac{2 y }{x^{2} + y^{2}} dx + \frac{2x}{x^{2} + y^{2}} dy = 0
$$
所以
$$
g (R) = \lim_{r \to 0} \frac{1}{2\pi r} \int_{C(r)} \ln(x^2 + y^2) \, ds = \ln (x_{0}^{2} + y_{0}^{2})
$$

#### 4  

设 $S = \{(x, y, z) \in \mathbb{R}^3 \mid x^2 + y^2 + z^2 = 1\}$ 是单位球面，取指向外面的定向。对给定的非负整数 $k$，计算第二型曲面积分  
$$
\iint_S z^k (x \, dy \, dz + y \, dz \, dx + z \, dx \, dy) \quad \text{或等价的} \quad \iint_S z^k (x \, dy \wedge dz + y \, dz \wedge dx + z \, dx \wedge dy)
$$
选取球坐标作为参数化
$$
x = \sin \theta \cos \phi \\
y = \sin \theta \sin \phi \\
z = \cos \theta
$$
上半球
$$
\iint_S z^k (x \, dy \, dz + y \, dz \, dx + z \, dx \, dy) \\= 
\iint_{S} \cos^{k} \theta (\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta) \cdot \\((\cos \theta \cos \phi, \cos \theta \sin \phi, - \sin \theta) \times (- \sin \theta \sin \phi, \sin \theta \cos \phi, 0)) d \theta d \phi \\ = 
\iint_{S} \cos^{k} \theta (\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta) \cdot (\sin \theta \cos \phi, \sin \theta \sin \phi, \cos \theta) \sin \theta d \theta d \phi \\ = 
\iint_{S} \cos^{k} \theta \sin \theta d \theta d \phi = 2 \pi \int_{0}^{1} x^{k} dx = \frac{2 \pi}{k + 1}
$$

所以整个球面积分为
$$
\iint_S z^k (x \, dy \, dz + y \, dz \, dx + z \, dx \, dy) = \begin{cases}  0 \qquad (\text{n为偶数}) \\ \frac{4 \pi}{k + 1} \qquad (\text{n为奇数}) \end{cases}
$$


#### 5  

设 $S$ 为曲面  
$$
(x-1)^2 + y^2 + z^2 = 2,
$$
取指向外面的定向。计算第二型曲面积分  
$$
\iint_S \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(x^2 + y^2 + z^2)^{3/2}}
$$
$$
\iint_S \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(x^2 + y^2 + z^2)^{3/2}} = \iint_{S} \frac{\vec{r}}{r^{3}} \cdot d \vec{S}
$$

利用 Gauss 定理
$$
\iint_{S‘} \frac{\vec{r}}{r^{3}} \cdot d \vec{S} = \iiint_{V’} \nabla \cdot \frac{\vec{r}}{r^{3}} d v = 0 \qquad (0 \notin S')
$$
取 $S' = \{ (x - 1)^{2} + y^{2}+ z^{2} = 2, x^{2} + y^{2} + z^{2} = 0.1 \}$

所以
$$
\iint_S \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(x^2 + y^2 + z^2)^{3/2}} = \iint_{x^{2} + y^{2} + z^{2} = 0.1} \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(x^2 + y^2 + z^2)^{3/2}} = 4 \pi
$$

#### 6  

设 $S \subseteq \mathbb{R}^3$ 是 $C^1$ 光滑的闭曲面，取指向外面的定向（或用课本上的术语，$S$ 是它所围成区域的外侧面），$(0, 0, 0) \notin S$。计算第二型曲面积分  
$$
\iint_S \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(a^2 x^2 + b^2 y^2 + c^2 z^2)^{3/2}}
$$
其中 $a, b, c$ 是给定的正数。  

同样使用 Gauss 定理
$$
\nabla \cdot \frac{(x, y, z)}{(a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{3}{2}} = \frac{1}{(a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^{3}} ((a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{3}{2} - 3 (a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{1}{2} a x^{2} \\ + (a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{3}{2} - 3 (a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{1}{2} b y^{2} \\ + (a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{3}{2} - 3 (a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{1}{2} c z^{2}) = 0 \qquad (0 \notin S)
$$
所以
$$
\iint_S \frac{x \, dy \, dz + y \, dz \, dx + z \, dx \, dy}{(a^2 x^2 + b^2 y^2 + c^2 z^2)^{3/2}} = \iiint_{V} \nabla \cdot \frac{(x, y, z)}{(a^{2} x^{2} + b^{2}y^{2} + c^{2} z^{2})^\frac{3}{2}}d v = 0
$$

#### 7  
设 $S \subseteq \mathbb{R}^3$ 是封闭的光滑曲面，$V$ 是由 $S$ 围成的三维有界闭区域（称之为 $S$ 的内部）。设 $f(x, y, z), P(x, y, z), Q(x, y, z), R(x, y, z)$ 都是 $V$ 上的 $C^1$ 光滑函数，且 $P, Q, R$ 在 $S$ 上恒等于 0。证明：  
$$
\iiint_V \left( \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz = -\iiint_V \left( P \frac{\partial f}{\partial x} + Q \frac{\partial f}{\partial y} + R \frac{\partial f}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz
$$
证明

因为$P, Q, R$ 在 $S$ 上恒等于 0，所以积分
$$
\iint_{S} P e^{f (x, y, z)} dy dz + Q e^{f (x, y, z)} dz dx + R e^{f (x, y, z)} dx dy = 0
$$
利用 Gauss 定理
$$
\iint_{S} P e^{f (x, y, z)} dy dz + Q e^{f (x, y, z)} dz dx + R e^{f (x, y, z)} dx dy \\ =
\iiint_{V} \frac{\partial}{\partial x} (P e^{f (x, y, z)}) + \frac{\partial}{\partial y} ( Q e^{f (x, y, z)})  + \frac{\partial}{\partial z} ( R e^{f (x, y, z)}) dx dy dz \\ = 
\iiint_V \left( \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz + \iiint_V \left( P \frac{\partial f}{\partial x} + Q \frac{\partial f}{\partial y} + R \frac{\partial f}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz = 0
$$
所以
$$
\iiint_V \left( \frac{\partial P}{\partial x} + \frac{\partial Q}{\partial y} + \frac{\partial R}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz = -\iiint_V \left( P \frac{\partial f}{\partial x} + Q \frac{\partial f}{\partial y} + R \frac{\partial f}{\partial z} \right) e^{f(x, y, z)} \, dx \, dy \, dz
$$


#### 8  

对于函数 $f : \mathbb{R}^3 \to \mathbb{R}$，如果极限  
$$
\lim_{M \to \infty} \iiint_{x^2 + y^2 + z^2 \leq M^2} f(x, y, z) \, dx \, dy \, dz
$$
存在, 则把上述极限记作  
$$
\iiint_{\mathbb{R}^3} f(x,y,z) \, dx \, dy \, dz,
$$
称为 $f$ 在 $\mathbb{R}^3$ 上的无穷积分。 
(1) 设 $P, Q : \mathbb{R}^3 \to \mathbb{R}$ 是 $C^1$ 光滑函数。证明：对正数 $M$，有  
$$
\iint_{\partial B} P(x,y,z) e^{Q(x,y,z)} \, dy \wedge dz = \iiint_B \left( \frac{\partial P}{\partial x} + P \frac{\partial Q}{\partial x} \right) e^{Q(x,y,z)} \, dV
$$
其中 $B = \{(x,y,z) \mid x^2 + y^2 + z^2 \leq M^2\}$, $\partial B$ 是 $B$ 的边界，取指向外面的定向。

利用推导 Gauss 定理时 local model 的结果
$$
\iint_{\partial B} P(x,y,z) e^{Q(x,y,z)} \, dy \wedge dz = \iiint_{B} \frac{\partial}{\partial x} ( P(x,y,z) e^{Q(x,y,z)}) dx  \wedge dy \wedge dz \\ = 
\iiint_B \left( \frac{\partial P}{\partial x} + P \frac{\partial Q}{\partial x} \right) e^{Q(x,y,z)} \, dV
$$

 (2) 证明：对于三元多项式 $P(x,y,z)$，有  
$$
\iiint_{\mathbb{R}^3} \frac{\partial P}{\partial x} e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz = 2 \iiint_{\mathbb{R}^3} x P(x,y,z) e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz
$$
证明

取 $f (x, y, z) = - (x^{2} + y^{2} + z^{2})$，上一小问结果化为
$$
\iint_{\partial B} P(x,y,z) e^{- (x^{2} + y^{2} + z^{2})} \, dy \wedge dz = \iiint_{B} \frac{\partial P}{\partial x} e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz - 2 \iiint_{B} x P(x,y,z) e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz
$$
取 $B = \{(x, y, z)| x^{2} + y^{2} + z^{2} \leq R^{2} \}$ ，设 $k$ 次多项式 $P$ 在紧致集  $\partial B$ 上的最大值为 $M R^{k}$
$$
\forall \epsilon > 0, \exist R, s.t. \iint_{\partial B} P(x,y,z) e^{- (x^{2} + y^{2} + z^{2})} \, dy \wedge dz \leq 2 M R^{k} \pi R^{2} e^{- R^{2}} \leq \epsilon
$$
所以当 $R \to \infty$ ，即 $B \to \mathbb{R}^{3}$ 时
$$
\iiint_{B} \frac{\partial P}{\partial x} e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz - 2 \iiint_{B} x P(x,y,z) e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz \to 0
$$
所以
$$
\iiint_{\mathbb{R}^3} \frac{\partial P}{\partial x} e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz = 2 \iiint_{\mathbb{R}^3} x P(x,y,z) e^{-x^2 - y^2 - z^2} \, dx \, dy \, dz
$$
