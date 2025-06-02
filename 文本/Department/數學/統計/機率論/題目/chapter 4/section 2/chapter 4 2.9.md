# 問題：
let $X$ and $Y$ be two r.v with joint pdf given by:
$$
f_{X,Y}(x,y)=ye^{-x},\quad 0<y\leq x <\infty
$$
1. determine the marginal pdf of $f_X$ and $f_Y$, and specify the range of the arguments involved.
2. determine the comditional pdf of $f_{X\mid Y} (\cdot\mid y)$ and $f_{Y\mid X}(\cdot\mid x)$, and specify the range of the arguments involved.
3. calculate the (conditional) probability $P(X>2\log2\mid Y=\log2)$, wjere always log stands for the natural logarithm.
# 回答：
##### 第一小題
$$
\begin{align}
f_X(x)&=\int^x_0ye^{-x}\,dy\\
&=e^{-x}\left(\frac{y^2}2\right)\bigg|^x_0\\
&=\frac{x^2}{2}e^{-x}
\end{align}
$$
$$
f_X(x)
\begin{cases}
\frac{x^2}{2}e^{-x},&0<x\\\\
0,&x\leq 0
\end{cases}
$$

$$
\begin{align}
f_Y(y)&=\int^\infty_yye^{-x}\,dx\\
&=y(-e^{-x})\bigg|^\infty_{x=y}\\
&=-ye^{-y}
\end{align}
$$
##### 第二小題
f^{X\mid Y}(\cdot\mid y)