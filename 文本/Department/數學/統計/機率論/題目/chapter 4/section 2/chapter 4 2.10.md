# 問題：
The joint pdf of the r.v $X$ and $Y$ is given by:
$$
f_{X,Y}(x,y)=xe^{-(x+y)},\quad x>0,\quad y>0
$$
1. determine the marginal pdf $f_X$ and $f_Y$.
2. determine the conditional pdf $f_{Y\mid X}(\cdot\mid x)$
3. calculate the probability $P(X>\ln 4)$, whereas as always log stands for the natural logarithm.
# 回答：
##### 第一小題
$$
\begin{align}
f_X(x)&=\int^\infty_0xe^{-(x+y)}\,dy\\
&=xe^{-x}\int^{\infty}_0 e^{-y}\\
&=xe^{-x}\left(-e^{-y}\right)\bigg|^{\infty}_{y=0}\\
&=xe^{-x}
\end{align}
$$
$$
f_X(x)=
\begin{cases}
xe^{-x},&x>0\\\\
0,&x\leq0
\end{cases}
$$

$$
\begin{align}
f_Y(y)&=\int^\infty_0xe^{-(x+y)}\,dx\\
&=e^{-y}\int^\infty_0xe^{-x}\,dx\\
&=e^{-y}\cdot1!\,(Gamma函數)\\
&=e^{-y}
\end{align}
$$
關於Gamma函數的積分，可以看一下[[chapter 4 1.11]]
$$
f_X(x)=
\begin{cases}
e^{-y},&y>0\\\\
0,&y\leq0
\end{cases}
$$
##### 第二小題
$$
\begin{align}
f_{Y\mid X}(\cdot\mid x)&=\frac{f_{X,Y}(x,y)}{f_X}\\
&=\frac{xe^{-(x+y)}}{xe^{-x}}\\
&=\frac{xe^{-x}e^{-y}}{xe^{-x}}\\
&=e^{-y}
\end{align}
$$
$$
f_{Y\mid X}(\cdot\mid x)=
\begin{cases}
e^{-y},&x>0\,;\,y>0\\\\
0,&x\leq0\,\text{or}\,y\leq0
\end{cases}
$$
##### 第三小題
要求$P(X>\ln4)$，我們可以直接積分X的邊際機率密度函數來得到答案，積分範圍是$\ln4<x<\infty$：
$$
P(X>\ln4)=\int^\infty_{\ln4} xe^{-x}\,dx\\
$$
我們可以發現，積分範圍是$(\infty,\ln4)$，而不是$(\infty,0)$，所以我們這邊不能用Gamma函數積分，我們需要用部分積分的方法來積分：
$$
\begin{align}
&u=x\quad dv=e^{-x}dx\\
&du=dx\quad v=\int e^{-x}dx=-e^{-x}
\end{align}
$$
$$
\begin{align}
P(X>\ln4)&=\int^\infty_{\ln4} xe^{-x}\,dx\\
&=\int u\,dv=
\end{align}
$$