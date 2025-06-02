# 問題：
The joint pdf of the r.v $X$ and $Y$ is given by:
$$
f_{X,Y}(x,y)=\frac12ye^{-xy},\quad0<x<\infty,\quad0<y<2.
$$
1. determine the marginal pdf $f_X$ and $f_Y$.
2. determine the conditional pdf f_{X\mid Y}(\cdot\mid y), and evaluate it at $y=1/2$
3. Compute the conditional expectation $E(X\mid Y=y)$, and evaluate it at $y=1/2$.
# 回答：
##### 第一小題
$$
\begin{align}
&v=y,\quad du=e^{-xy}\,dy\\
&dv=dy,\quad u=\int e^{-xy}\,dy=\frac{-1}{x}e^{-xy}
\end{align}
$$
$$
\begin{align}
f_X&=\frac12\int^2_0ye^{-xy}\,dy\\
&=uv-\int^2_0u\,dv\\
&=\frac{-y}{x}e^{-xy}\bigg|^2_{y=0}-\int^2_0\frac{-1}{x}e^{-xy}\,dy\\
&=\frac{-2}{x}e^{-2x}-\left(\frac{1}{x^2}e^{-xy}\right)\bigg|^2_{y=0}\\
&=\frac{-2}{x}e^{-2x}-
\end{align}
$$