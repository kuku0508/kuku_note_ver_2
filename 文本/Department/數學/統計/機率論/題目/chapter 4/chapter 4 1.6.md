# 問題：
If the r.v.'s $X$ and $Y$ have the joint pdf $f_{X,Y}(X,Y)=e^{-x-y}$, for $x>0$ and $y>0$, compute the following probabilities:
1. $P(X\leq x)$
2. $P(Y\leq y)$
3. $P(X<Y)$
4. $P(X+Y\leq 3)$
# 回答：
#### 1.
題目要我們求$P(X\leq x)$，所以我們就必須要考慮所有$P(X\leq x)$，包含$0<y<\infty$的範圍。
那我們的積分就會像這樣（因為我們要代入x，所以建議用非x的符號來取代x）。
$$
\begin{align}
\int^\infty_0 \int ^x_0 e^{-t-y}\,dtdy=\int
\end{align}$$
