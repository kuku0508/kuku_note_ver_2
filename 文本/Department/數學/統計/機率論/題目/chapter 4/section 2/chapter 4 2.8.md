# 問題：
show that the marginal pdf of the r.v $X$ and $Y$ whose joint pdf is given by:
$$
f_{X,Y}(x,y)=\frac{6}{5}(x+y^2),\quad 0\leq x\leq 1,\quad 0\leq y \leq 1
$$
are as follows:
$$
f_X(x)=\frac25(3x+1),\quad0\leq x\leq 1,\quad f_Y(y)=\frac35(2y^2+1),\quad 0\leq y \leq 1
$$
# 回答：
題目要我們計算出$f_X$、$f_Y$，方法跟[[chapter 4 2.7]]的概念差不多，我就不多做贅述：
$$
\begin{align}
f_X(x)&=\int^1_0\frac65(x+y^2)\,dy\\
&=\frac65\left(\frac{y^3}{3}+xy\right)\bigg|^1_{y=0}\\
&=\frac65\cdot\frac{1}{3}\left(1+3x\right)\\
&=\frac25\left(1+3x\right)\\
&=\frac25\left(3x+1\right)
\end{align}
$$
$$
\begin{align}
f_Y(y)&=\int^1_0\frac65(x+y^2)\,dx\\
&=\frac65\left(\right)
\end{align}
$$