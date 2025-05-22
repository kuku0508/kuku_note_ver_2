# 問題
The r.v.’s X and Y have the joint p.d.f. $f_{X,Y}$ given by:
$$
f_{X,Y}(x,y)=\frac67\left(x^2+\frac{xy}{2}\right),\quad1<x\leq1,\, 0<y\leq 2
$$
(i) Show that $f_{X,Y}$ is, indeed, a p.d.f.
(ii) Calculate the probability P(X > Y).
# 答案

#### (i)
第一題要我們證明$f_{X,Y}$真的是pdf，如果$f_{X,Y}$真的是pdf的話她應該要符合下面三點。
1. $f_{X,Y}\geq 0,\,\forall(x,y)\in R^2$（所有值都是非負）
2. $\int^{\infty}_{-\infty}\int^{\infty}_{-\infty}f_{X,Y}\,dxdy=1$（對pdf的定義域上下界積分會等於1）
3. $$P((X,Y)\in B)=\iint_\limits_D f_{X,Y}\,dxdy$$