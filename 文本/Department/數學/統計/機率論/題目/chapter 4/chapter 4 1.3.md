# 問題
If the r.v.'s X and Y have the joint p.d.f. given by:
$f_{X,Y}(x,y)=x+y,\quad 0<x< 1,\quad 0<y< 1$
calculate the probability$P(X<Y)$
- - -
# 答案
我們有兩個做法，一個是算出來機率，另外一個是畫圖。
#### 計算
我們先確定變數之間的關係，因為Y一定要大於X，且他們本來就有0到1的限制，所以整個限制式可以改寫成：
$$
0<X<Y<1
$$
然後我們再依照這個範圍去積分他的pdf，就可以得到$P(X<Y)$。
$$
\begin{align}
P(X<Y)&=\int^1_0 \int_0^Y X+Y dx dy\\
&=\int^1_0 \left.\left(\frac12X^2+XY\right)\right|^Y_{X=0}\,dy\\
&=\int^1_0\left(\frac12Y^2+Y^2\right)\,dy\\
&=\int^1_0\frac32Y^2\,dy\\
&=\left.\frac12Y^3\right|^1_{Y=0}\\
&=\frac12
\end{align}
$$
