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
&=\int^{\infty}_0e^{-x}(-e^{-t})|^{y}_{t=0}\,dx\\
&=\int^{\infty}_0e^{-x}(-e^{-y}+1)\,dx\\
&=(-e^{-y}+1)\int^{\infty}_0e^{-x}\,dx\\
&=(-e^{-y}+1)(-e^{-x})|^\infty_{x=0}\\
&=(-e^{-y}+1)(1)\\
&=1-e^{-y}
\end{align}
$$

#### 3.
而第三小題其實就跟前兩題一樣，就是定義域問題，我們可以知道，我們今天要符合原題目的$X>0$、$Y>0$，也要符合第三小題要求的$X<Y$。所以定義域就會長這樣$0<X<Y<\infty$。最後積分範圍就會長這樣：
$$
\begin{align}
P(X<Y)&=\int^\infty_0 \int^y_0 e^{-x-y} \,dx dy\\
&=\int^\infty_0e^{-y}\int^{y}_0e^{-x}\,dxdy\\
&=\int^\infty_0e^{-y}(-e^{-x})|^{y}_{x=0}\,dy\\
&=\int^\infty_0e^{-y}(-e^{-y}+1)\,dy\\
&=\int^\infty_0e^{-2y}+e^{-y}\,dy\\
&=\frac12e^{-2y}-e^{-y}|^{\infty}_{y=0}\\
&=1-\frac12\\
&=\frac12
\end{align}
$$
#### 4.
第四小題看起來有點麻煩，我們要先理解定義域。
在原本的pdf中，定義域$X$的定義域是$X>0$，$Y$的定義域為$Y>0$。
而我們有另外一個限制，就是$X+Y\leq 3$。
我們可以先看一下這個限制，我們可以透過移位，來得到
- $X\leq 3-Y$
或是
- $Y\leq 3-X$

我們先看$X$，因為有$X>0$跟$X\leq3-Y$這兩個限制，所以我們就會得到這樣的定義域：
$$0<X\leq 3-Y$$
而因為有$X+Y\leq 3$這個限制存在，所以我們給$Y$的定義域也會被這個限制影響。但因為我們在前面處理完$X$跟$Y$在$X+Y\leq 3$這個限制式上，所以我們現在只要考慮$Y$要如何不違背$X+Y\leq 3$這個限制式。
我們能讓$Y$
