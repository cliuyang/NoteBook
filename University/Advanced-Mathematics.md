<head>
    <script src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML" type="text/javascript"></script>
    <script type="text/x-mathjax-config">
        MathJax.Hub.Config({
            tex2jax: {
            skipTags: ['script', 'noscript', 'style', 'textarea', 'pre'],
            inlineMath: [['$','$']]
            }
        });
    </script>
</head>

# 高等数学

## 第一章 函数与极限

### 第一节 映射与函数

#### 一、映射

##### 定义

设$X$、$Y$是两个非空集合，如果存在一个法则$f$，使得对$X$中每个元素$x$，按法则$f$，在$Y$中有唯一确定的非空元素$y$与之对应，那么称$f$为从$X$到$Y$的**映射**，记作

$$f:X\rightarrow Y$$

其中$y$称为元素$x$（在映射$f$下）的一个**像**，并记作$f(x)$，即

$$y = f(x)$$

而元素$x$称为元素$y$（在映射$f$下）的一个**原像**；集合$X$称为映射$f$的值域，记作$R_f$或$f(x)$，即

$$R_f = f(X) = \{f(x)\vert x \in X \}$$

#### 二、函数

##### 函数的概念

设数集$D \subset R$，则称映射$f:D \rightarrow R$为定义在$D$上的**函数**，通常简记为

$$y = f(x), x \in D$$

其中$x$称为**自变量**，$y$称为**因变量**，$D$称为**定义域**，记作$D_f$，即$D_f = D$。

##### 函数的特性

1. **函数的有界性** 如果存在整数$M$使得

   $$\left| f(x) \right| \leqslant M$$

   对任一$x \in X$都成立，那么称函数$f(x)$在$X$上**有界**。如果这样的$M$不存在，就称函数$f(x)$在$X$上**无界**；这就是说，如果对于任何整数$M$，总存在$x_1 \in X$，使$\left| f(x_1) \right| > M$，那么函数$f(x)$在$X$上无界。
2. **函数的单调性** 设函数$f(x)$的定义域为$D$，区间$I \subset D$。如果对于区间$I$上任意两点$x_1$及$x_2$，当$x_1 < x_2$时，恒有

    $$f(x_1) < f(x_2)$$

    那么称函数$f(x)$在区间$I$上是**单调增加**的；如果对于区间$I$上任意两点$x_1$及$x_2$，当$x_1 < x_2$时，恒有

    $$f(x_1) > f(x_2)$$

    那么称函数$f(x)$在区间$I$上是**单调减少**的。单调增加和单调减少的函数统称为**单调函数**。
3. **函数的奇偶性** 设函数$f(x)$的定义域$D$关于原点对称，如果对于任一$x \in D$，

    $$f(-x) = f(x)$$

    恒成立，那么称$f(x)$为**偶函数**。如果对于任一$x \in D$，

    $$f(-x) = -f(x)$$

    恒成立，那么称$f(x)$为**奇函数**。
4. **函数的周期性** 设函数$f(x)$的定义域为$D$，如果存在一个正数$l$，使得对于任一$x \in D$有$(x \pm l) \in D$，且

    $$f(x \pm l) = f(x)$$

    恒成立，那么称$f(x)$为**周期函数**，$l$称为$f(x)$的**周期**，通常我们说周期函数的周期是指**最小正周期**。
5. **反函数与复合函数** 设函数$f:D \rightarrow f(D)$是单射，则它存在逆映射$f^{-1}:f(D) \rightarrow D$，称此映射$f^{-1}$为函数$f$的**反函数**。

   相对于反函数$y = f{-1}(x)$来说，原来的函数$y = f(x)$称为**直接函数**。

   设函数$y = f(u)$的定义域为$D_f$，函数$u = g(x)$的定义域为$D_g$，且其值域$R_g \subset D_f$，则由下式确定的函数

    $$y = f[g(x)], x \in D_g$$

    称为由函数$u = g(x)$与函数$y = f(u)$构成的**复合函数**，它的定义域为$D_g$，变量$u$称为**中间变量**。

##### 函数的运算

设$f(x)$，$g(x)$的定义域依次为$D_f$，$D_g$，$D = D_f \cap D_g \neq \varnothing$，则我们可以定义这两个函数的下列运算：

* 和（差）$f \pm g$：$(f \pm g)(x) = f(x) \pm g(x), x \in D$；
* 积$f \cdot g$：$(f \cdot g)(x) = f(x) \cdot g(x), x \in D$；
* 商$\frac{f}{g}$：$(\frac{f}{g})(x) = \frac{f(x)}{g(x)}, x \in D \backslash \left\{ x \vert g(x) = 0, x \in D  \right\}$

##### 初等函数

* 幂函数：$y = x^{\mu}$（$\mu \in R$是常数）
* 指数函数：$y = a^x$（$a > 0$且$a \ne 1$）
* 对数函数：$y = \log_ax$（$a > 0$且$a \ne 1$，特别当$a = e$时，记为$y = \ln x$）
* 三角函数：如$y = \sin(x)$，$y = \cos(x)$，$y = \tan(x)$等
* 反三角函数：如$y = \arcsin(x)$，$y = \arccos(x)$，$y = \arctan(x)$等

以上这五类函数统称为**基本初等函数**。

由常数和基本初等函数经过有限次的四则运算和有限次的函数复合步骤所构成并可以用一个式子表示的函数，称为**初等函数**。例如

$$y = \sqrt{1 - x^2}, y = \sin^2x, y = \sqrt{\cot \frac{x}{2}}$$

### 第二节 数列的极限

#### 一、数列极限的定义

* 如果按照某一法则，对每个$n \in N_+$，对应着一个确定的实数$x_n$，这些实数$x_n$按照下标$n$从小到大排列得到的一个序列

    $$x_1, x_2, x_3, \ldots, x_n, \ldots$$

    就叫做**数列**，简记为$\left\{x_n\right\}$。

* 设$\left\{x_n\right\}$为一数列，如果存在常数$a$，对于任意给定的正数$\epsilon$（不论它多么小），总存在正整数$N$，使得当$n > N$时，不等式

    $$\left|x_n - a\right| < \epsilon$$

    都成立，那么就称常数$a$是**数列$\left\{X_n\right\}$的极限**，或者称数列$\left\{X_n\right\}$**收敛于**$a$，记为

    $$\lim_{n \rightarrow \infty}x_n = a$$

    或

    $$x_n \rightarrow a(n \rightarrow \infty)$$

    如果不存在这样的常数$a$，就说数列$\left\{x_n\right\}$没有极限，或者说数列$\left\{x_n\right\}$是**发散**的，习惯上也说$\lim\limits_{n \rightarrow \infty}x_n$不存在。

#### 二、收敛数列的性质

1. **极限的唯一性** 如果数列$\left\{x_n\right\}$收敛，那么它的极限唯一；
2. **收敛数列的有界性** 如果数列$\left\{x_n\right\}$收敛，那么数列$\left\{x_n\right\}$一定有界；
3. **收敛数列的保号性** 如果$\lim\limits_{n \rightarrow \infty}x_n = a$，且$a > 0$（或$a < 0$），那么存在正整数$N$，当$n > N$时，都有$x_n > 0$（或$x_n< 0$）；

    * 如果数列$\left\{x_n\right\}$从某项起有$x_n \geqslant 0$或（$x_n \leqslant 0$），且$\lim\limits_{n \rightarrow \infty}x_n = a$，那么$a \geqslant 0$（或$a \leqslant 0$）

4. **收敛数列与其子数列间的关系** 如果数列$\left\{x_n\right\}$收敛于$a$，那么它的任一子数列也收敛，且极限也是$a$。

### 第三节 函数的极限

#### 一、函数极限的定义

1. 设函数$f(x)$在点$x_0$的某一点去心邻域内有定义，如果存在常数$A$，对于任意给定的正整数$\varepsilon$（不论它多么小），总存在常数$\delta$，使得当$x$满足不等式$0 < \left|x - x_0\right| < \delta$时，对应的函数值$f(x)$都满足不等式

    $$\left|f(x) - A\right| < \delta$$

    那么常数A就叫做**函数$f(x)$当$x \rightarrow x_0$时的极限**，记作

    $$\lim\limits_{x \rightarrow x_0} = A或f(x) \rightarrow A（当x \rightarrow x_0）$$

2. 设函数$f(x)$当$\left|x\right|$大于某一正数时有定义。如果存在常数$A$，对于任一给定的正数$\varepsilon$（不论它多么小），总存在着正数$X$，使得当$x$满足不等式$\left|x\right| > X$时，对应的函数值$f(x)$满足不等式

    $$\left|f(x) - A\right| < \varepsilon$$

    那么常数$A$就叫做**函数$f(x)$当$x \rightarrow \infty$时的极限**，记作

    $$\lim\limits_{x \rightarrow \infty}f(x) = A或f(x) \rightarrow A（当x \rightarrow \infty）$$

#### 二、函数极限的性质

1. **（函数极限的唯一性）** 如果$\lim\limits_{x \rightarrow x_0}f(x)$存在，那么这极限唯一；
2. **（函数极限的局部有界性）** 如果$\lim\limits_{x \rightarrow x_0}f(x) = A$，那么存在常数$M > 0$和$\delta > 0$，使得当$0 < \left|x - x_0\right| < \delta$时，有$\left|f(x)\right| \leqslant M$；
3. **（函数极限的局部保号性）** 如果$\lim\limits_{x \rightarrow x_0}f(x) = A$，且$A > 0$（或$A < 0$），那么存在常数$\delta > 0$，使得当$0 < \left|x - x_0\right| < \delta$\时，有$f(x) > 0$（或$f(x) < 0$）；

   * 如果$\lim\limits_{x \rightarrow x_0}f(x) = A (A \neq 0)$，那么就存在着$x_0$的某一去心邻域$\bigcup\limits^{\circ}(x_0)$，当$x \in \bigcup\limits^{\circ}(x_0)$时，就有$\left|f(x)\right| > \frac{\left|A\right|}{2}$；
   * 如果在$x_0$的某去心邻域内$f(x) \geqslant 0$（或$f(x) \leqslant 0$），而且$\lim\limits_{x \rightarrow x_0}f(x) = A$，那么$A \geqslant 0$（或$A \leqslant 0$）。

4. **（函数极限与数列极限的关系）** 如果极限$\lim\limits_{x \rightarrow x_0}f(x)$存在，$\left\{x_n\right\}$为函数$f(x)$的定义域内任一收敛于$x_0$的数列，且满足：$x_n \neq x_0 (n \in N_+)$，那么相应的函数值数列$\left\{f(x_n)\right\}$必收敛，且$\lim\limits_{n \rightarrow \infty}f(x_n) = \lim\limits_{x \rightarrow x_0}f(x)$。

### 第四节 无穷大与无穷小

#### 无穷小

* 如果函数$f(x)$
