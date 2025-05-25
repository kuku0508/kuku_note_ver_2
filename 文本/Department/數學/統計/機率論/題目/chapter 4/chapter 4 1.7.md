# 問題：
Let $X$ and $Y$ be r.v.'s jointly distributed with pdf $f_{X,Y}=2/c^2$, for $0<x\leq y < c$.
Determine the constant c .
# 回答：
這種題目反正我們知道pdf是$2/c^2$，我們只要對她積分，然後積分結果必須要是1，我們就可以透過
$$
\begin{align}
\int^{c}_{0} \int^{y}_{0} \frac{2}{c^2} \,dxdy&=\int^c_0\frac2{c^2}\int^y_01\,dxdy\\
&=\int^c_0\frac2{c^2}y\,dy\\
&=\frac2{c^2}\int^c_0y\,dy\\
\end{align}
$$