# 問題：
The joint pdf of the r.v $X$ and $Y$ is given by:
$$
f_{X,Y}(x,y)=\frac12ye^{-xy},\quad0<x<\infty,\quad0<y<2.
$$
1. determine the marginal pdf $f_X$ and $f_Y$.
2. determine the conditional pdf $f_{X\mid Y}(\cdot\mid y)$, and evaluate it at $y=1/2$
3. Compute the conditional expectation $E(X\mid Y=y)$, and evaluate it at $y=1/2$.
# 回答：
##### 第一小題
$$
\begin{align}
&f_X=\frac12\int^2_0ye^{-xy}\,dy\\\\
&v=y,\quad du=e^{-xy}\,dy\\
&dv=dy,\quad u=\int e^{-xy}\,dy=\frac{-1}{x}e^{-xy}
\end{align}
$$
$$
\begin{align}
f_X&=\frac12\int^2_0ye^{-xy}\,dy\\
&=\frac12\left(uv-\int^2_0u\,dv\right)\\
&=\frac12\left(\frac{-y}{x}e^{-xy}\bigg|^2_{y=0}-\int^2_0\frac{-1}{x}e^{-xy}\,dy\right)\\
&=\frac12\left(\frac{-2}{x}e^{-2x}-\left(\frac{1}{x^2}e^{-xy}\right)\bigg|^2_{y=0}\right)\\
&=\frac12\left(\frac{-2}{x}e^{-2x}-\frac{1}{x^2}e^{-2x}+\frac{1}{x^2}\right)
\end{align}
$$


$$
\begin{align}
f_Y&=\frac12y\int^\infty_0e^{-xy}\,dx\\
&=\frac12y\left(\frac{-1}{y}e^{-xy}\right)\bigg|^\infty_{x=0}\\
&=-\frac12y\cdot\left(\frac{-1}{y}\right)\\
&=\frac12
\end{align}
$$
##### 第二小題
$$
\begin{align}
f_{X\mid Y}(\cdot\mid Y)&=\frac{f_{X,Y}(x,y)}{f_Y(y)}\\
&=\frac{\frac12ye^{-xy}}{\frac{1}{2}}\\
&=ye^{-xy}\\\\
f_{X\mid Y}(\cdot\mid Y=\frac12)=\frac12e^{-\frac x2}
\end{align}
$$
##### 第三小題
在我們透過任何的積分方式來試著得到給定Y的條件機率的期望值前，我們可以觀察一下這個條件機率：
$$
f_{X\mid Y}(\cdot\mid Y)=ye^{-xy}
$$
我們可以回想一下，在我們常見的機率分配中，有一個叫做[[指數分配]]的機率分配，他的pdf就跟這個給定Y的條件機率一模一樣。指數分配的pdf是
$$
f(x)=\lambda e^{-\lambda x}
$$
只要$\lambda=y$，那我們就可以透過指數分配得到期望值$1/\lambda$。
所以條件機率的期望值會是$1/y$。
而在$y=1/2$的情況，期望值會是2。