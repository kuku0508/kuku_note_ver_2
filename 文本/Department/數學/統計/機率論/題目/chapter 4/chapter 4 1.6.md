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
P(X\leq x)=\int^\infty_0 \int ^x_0 e^{-t-y}\,dtdy&=\int^\infty_0\int^x_0e^{-t}\cdot e^{-y}\,dtdy\\
&=\int^\infty_0e^{-y}\int^x_0e^{-t}\,dtdy\\
&=\int^\infty_0 e^{-y}\cdot\left(-e^{-t}\right)|^x_{t=0}\,dy\\
&=\int^\infty_0 e^{-y}\cdot\left[ \left(-e^{-x}\right)-(-1) \right]\,dy\\
&=\left(1-e^{-x}\right)\left(-e^{-y}\right)|^\infty_{y=0}\\
&=\left(1-e^{-x}\right)\cdot\left[-\left(-1\right)\right]\\
&=1-e^{-x}
\end{align}
$$
#### 2.
跟第一小題一樣，我們要求$P(Y\leq y)$，我們就必須要考慮所有$P(Y\leq y)$，包含$0<x<\infty$的範圍。那我們積分範圍就是：
$$
\begin{align}
P(Y\leq y)&=\int^{\infty}_{0} \int^{y}_{0}e^{-t-x} \,dtdx\\
&=\int^{\infty}_0e^{-x}\int^{y}_{0}e^{-t}\,dtdx\\
&=\int^{\infty}_0e^{-x}
\end{align}
$$