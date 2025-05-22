# 問題
The r.v.’s X and Y have the joint p.d.f. $f_{X,Y}$ given by:
$$
f_{X,Y}(x,y)=\frac67\left(x^2+\frac{xy}{2}\right),\quad0<x\leq1,\, 0<y\leq 2
$$
(i) Show that $f_{X,Y}$ is, indeed, a p.d.f.
(ii) Calculate the probability P(X > Y).
# 答案

#### (i)
第一題要我們證明$f_{X,Y}$真的是pdf，如果$f_{X,Y}$真的是pdf的話她應該要符合下面三點。
1. $f_{X,Y}\geq 0,\,\forall(x,y)\in R^2$（所有值都是非負）
2. $\int^{\infty}_{-\infty}\int^{\infty}_{-\infty}f_{X,Y}\,dxdy=1$（對pdf的定義域上下界積分會等於1）
3. $P((X,Y)\in B)=\iint\limits_D f_{X,Y}\,dxdy$（機率等於對pdf的相對範圍做積分）
為了證明這三點，我們可以先證明所有值一定非負。
##### 第一點
我們來證明第一點
我們可以看到，pdf是
$$
\frac67\left(x^2+\frac{xy}2\right)
$$
我們可以看到裡面的值有$x^2$跟$\frac{xy}2$。而我們知道$x^2$一定會是非負；$xy$也一定會是非負，因為x跟y的定義域都是正數，正數（$x$）乘以正數（$y$）也一定會是正數（$xy$）。正數（$xy$）除以2也會是正數（$\frac{xy}{2}$），所以$\frac{xy}{2}$也會是正數。而正數（$x^2$）加正數（$\frac{xy}2$）也一定會是正數。
故我們可以知道$f_{X,Y}$一定是非負。

##### 第二點&第三點
接下來我們可以一起證明第二點跟第三點，我們只要證明$f_{X,Y}$在定義域積分為1，我們就可以證明第二點跟第三點成立。但我們要透過積分"一起"證明第二點跟第三點成立，我們一定要ㄒ證明