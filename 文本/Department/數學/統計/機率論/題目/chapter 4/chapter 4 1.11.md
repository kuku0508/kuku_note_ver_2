# 問題：
The r.v.'s $X$ and $Y$ have joint pdf $f_{X,Y}$ given by:
$$
f_{X,Y}(x,y)=c(y^2-x^2)e^{-y},\quad -y<x<y,\quad0<y<\infty.$$
Determine the constant c.
**Hint**. We have that $\int^\infty_0 ye^{-y}\,dy=1$, and the remaining integrals are computed recursively.
# 回答：
$$
\begin{align}
\int^\infty_0\int^y_{-y} c(y^2-x^2)e^{-y}\,dxdy&=\int^\infty_0ce^{-y}\int^y_{-y}y^2-x^2\,dxdy\\
&=\int^\infty_0ce^{-y}\left(y^2x-\frac{x^3}{3}\right)\bigg|^{y}_{x=-y}\,dy\\
&=\int^\infty_0ce^{-y}\left[\left(y^3-\frac{y^3}{3}\right)-\left(-y^3-\frac{-y^3}{3}\right)\right]\,dy\\
&=\int^\infty_0ce^{-y}\left(2y^3-\frac{2y^3}{3}\right)\,dy\\
&=c\int^\infty_0\frac{4}{6}y^3e^{-y}\,dy\quad(使用\text{Gamma}函數)\\
&=\frac{4c}{6}\cdot3!\\
&=8c\\
&\Rightarrow8c=1\\
&\Rightarrow c=\frac{1}{8}
\end{align}
$$
$$
\Gamma(s)=\int^\infty_0 y^{(s-1)}e^{-y}\,dy=(s-1)!
$$