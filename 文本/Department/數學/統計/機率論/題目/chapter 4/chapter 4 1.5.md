# 問題
The r.v.'s $X$ and $Y$ have the joint pdf
$f_{X,Y}(X,Y)=e^{-x-y},\,x>0,y>0$.
1. Calculate the probability$P(X\leq Y\leq c)$ for some $c>0$.
2. Find the numerical value in part 1 for $c=\log2$, where log is the natural logarithm.
# 答案
#### 1.
要計算$P(X\leq Y\leq c)$，我們一樣是用積分pdf的方式去計算機率。
而我們的定義域就是$0<x\leq y \leq c$，因為我們知道c、x跟y都必大於0，所以我們且$x\leq y \leq c$，故我們把定義域這樣設計。接下來透過這個定義域來積分：
$$
\begin{align}
\int^c_0\int^y_0 e^{-x-y}\,dxdy&=\int^c_0\int^y_0e^{-x}\cdot e^{-y}\,dxdy\\
&=\int^c_0 e^{-y}\int^y_0 e^{-x} dxdy\\
&=\int^c_0 e^{-y}\left(-e^{-x}\right)|^y_{x=0}\,dy\\
&=\int^c_0 e^{-y}\cdot \left(-e^{-y}\right)\,dy\\
&=-\int^c_0 e^{-2y}\,dy\\
&=-\left(-\frac{e^{-2y}}{2}\right)|^c_{y=0}\\
&=\frac{e^{-2c}}{2}
\end{align}
$$
#### 2.
第二題要我們找$P(X\leq Y \leq \log 2)$。

