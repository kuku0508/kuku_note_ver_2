# 問題：
let $X$ and $Y$ be two r.v with joint pdf given by:
$$
f_{X,Y}(x,y)=ye^{-x},\quad 0<y\leq x <\infty
$$
1. determine the marginal pdf of $f_X$ and $f_Y$, and specify the range of the arguments involved.
2. determine the comditional pdf of $f_{X\mid Y} (\cdot\mid y)$ and $f_{Y\mid X}(\cdot\mid x)$, and specify the range of the arguments involved.
3. calculate the (conditional) probability $P(X>2\log2\mid Y=\log2)$, where always log stands for the natural logarithm.
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
\frac{x^2}{2}e^{-x},&0<x<\infty\\\\
0,&x\leq 0
\end{cases}
$$

$$
\begin{align}
f_Y(y)&=\int^\infty_yye^{-x}\,dx\\
&=y(-e^{-x})\bigg|^\infty_{x=y}\\
&=ye^{-y}
\end{align}
$$
$$
f_Y(y)
\begin{cases}
ye^{-y},&0<y<\infty\\\\
0,&y\leq 0
\end{cases}
$$
##### 第二小題
$$
\begin{align}
f_{X\mid Y}(\cdot\mid y)&=\frac{f_{X,Y}(x,y)}{f_Y(y)}\\
&=\frac{ye^{-x}}{ye^{-y}}\\
&=e^{-x}\cdot e^y\\
&=e^{-x+y}
\end{align}
$$
$$
f_{X\mid Y}(\cdot\mid y)
\begin{cases}
e^{-x+y},&y\leq x \leq \infty\,;\,\text{given}\,0<y<\infty \\\\
0,&x<y
\end{cases}
$$

$$
\begin{align}
f_{Y\mid X}(\cdot\mid x)&=\frac{f_{X,Y}(x,y)}{f_X(x)}\\
&=\frac{ye^{-x}}{\frac{x^2}{2}e^{-x}}\\
&=\frac{2y}{x^2}
\end{align}
$$
$$
f_{Y\mid X}(\cdot\mid x)
\begin{cases}
\frac{2y}{x^2},&0<y\leq x,\,\text{given}\,y\leq x<\infty\\\\
0,&x<y ,\,y<0
\end{cases}
$$
##### 第三小題
 題目要求$P(X>2\ln2\mid Y=\ln2)$，我們就把Y代入$\ln2$然後對X積分，積分範圍會是$2\ln 2<X<\infty$：
 $$
 \begin{align}
 P(X>2\ln 2\mid Y=\ln 2)&=\int^\infty_{2\ln2}e^{-x+\ln2}\,dx\\
 &=e^{\ln2}\cdot\int^\infty_{2\ln2}e^{-x}\,dx\\
 &=e^{\ln2}\cdot\left(-e^{-x}\right)\bigg|^\infty_{x=2\ln2}\\
 &=2\cdot-\left\frac{}{}
 \end{align}
 $$
 