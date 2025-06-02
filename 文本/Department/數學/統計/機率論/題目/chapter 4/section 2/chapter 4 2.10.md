# 問題：
The joint pdf of the r.v $X$ and $Y$ is given by:
$$
f_{X,Y}(x,y)=xe^{-(x+y)},\quad x>0,\quad y>0
$$
1. determine the marginal pdf $f_X$ and $f_Y$.
2. determine the conditional pdf $f_{Y\mid X}(\cdot\mid x)$
3. calculate the probability $P(X>\ln 4)$, whereas as always log stands for the natural logarithm.
# 回答：
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
&=e^{-y}\int^\infty_0xe^{-x}
\end{align}
$$
$$
f_X(x)=
\begin{cases}
xe^{-x},&x>0\\\\
0,&x\leq0
\end{cases}
$$
