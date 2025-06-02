# 問題：
let $X$ and $Y$ be two r.v with joint pdf given by:
$$
f_{X,Y}(x,y)=ye^{-x},\quad 0<y\leq x <\infty
$$
1. determine the marginal pdf of $f_X$ and $f_Y$, and specify the range of the arguments involved.
2. determine the comditional pdf of $f_{X\mid Y} (\cdot\mid y)$ and $f_{Y\mid X}(\cdot\mid x)$, and specify the range of the arguments involved.
3. calculate the (conditional) probability $P(X>2\log2\mid Y=\log2)$, wjere always log stands for the natural logarithm.
# 回答：
$$
\begin{align}
f_X(x)&=\int^\infty_yye^{-x}\\
&=y\left(-e^{-x}\right)\bigg|^\infty_{x=y}\\
&=ye^{-y}
\end{align}
$$
$$
\begin{align}
f_Y(y)&=\int^x_0ye^{-x}\\

\end{align}
$$