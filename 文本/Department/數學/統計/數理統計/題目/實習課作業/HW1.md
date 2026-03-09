(1)$X_1,X_2,\cdots,X_n\overset{i.i.d}{\sim}U(0,\theta),\theta\in\Omega=(0,\infty).$ Let $Y_n$ be the largest order statistic of $X_i$'s.

(a) Find $f_{Y_n}(y_n)$ 

Find $F_{Y_n}(y_n)$ first
$$
\begin{align}
F_{Y_n}(y_n)&=P(Y_n\leq y)\\&
=P(X_1\leq y,\ldots,X_n\leq y)\\\\
&=P(X_i\leq y)=
\begin{cases}
0,&y\leq 0\\
\frac{y}{\theta},&0<y<\theta\\
1,&y\geq\theta
\end{cases}
\end{align}
$$
