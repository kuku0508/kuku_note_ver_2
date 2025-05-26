# 問題
The r.v.’s X and Y have the joint p.d.f. $f_{X,Y}$ given by:
$$
f_{X,Y}(x,y)=\frac67\left(x^2+\frac{xy}{2}\right),\quad0<x\leq1,\, 0<y\leq 2
$$
(i) Show that $f_{X,Y}$ is, indeed, a p.d.f.
(ii) Calculate the probability P(X > Y).
- - -
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
\frac67\left(x^2+\frac{xy}2\right),\quad0<x\leq1,\, 0<y\leq 2
$$
我們可以看到裡面的值有$x^2$跟$\frac{xy}2$。而我們知道$x^2$一定會是非負；$xy$也一定會是非負，因為x跟y的定義域都是正數，正數（$x$）乘以正數（$y$）也一定會是正數（$xy$）。正數（$xy$）除以2也會是正數（$\frac{xy}{2}$），所以$\frac{xy}{2}$也會是正數。而正數（$x^2$）加正數（$\frac{xy}2$）也一定會是正數。
故我們可以知道$f_{X,Y}$一定是非負。

##### 第二點&第三點
接下來我們可以一起證明第二點跟第三點，我們只要證明$f_{X,Y}$在定義域積分為1，我們就可以證明第二點跟第三點成立。但我們要透過積分"一起"證明第二點跟第三點成立，我們一定要先證明第一點。不然$f_{X,Y}$在定義域積分為1，就只能證明第二點，不能證明第三點。

原因是因為，儘管我們發現了$f_{X,Y}$在定義域積分為1這個結果，我們也不能保證$f_{X,Y}$會不會輸出負值，但輸出負值這件事情是不能被允許的，因為機率不可能是負的。
例如：
$$
f(x)=
\begin{cases}
3&,0<x\leq0.5\\
-1&,0.5<x\leq1
\end{cases}
$$
$$
\int^{0.5}_0 3\,dx+\int^1_{0.5}-1\,dx=\left.3x\right|^{0.5}_{x=0}+-x|^1_{x=0.5}=1.5+(-1+0.5)=1
$$
你可以看到，有機率是負數的，但我們得到的積分是1。證明了第二點，但絕對沒有證明第三點。

好，反正我們這邊證明了$f_{X,Y}$不會有負值，所以可以一起證明第二點跟第三點，進而證明$\frac67\left(x^2+\frac{xy}2\right)$是pdf。
那我們就來對他的定義域做積分：
$$
\begin{align}
\int^1_0\int^2_0\frac67\left(x^2+\frac{xy}2\right)\,dydx&=\frac67\int^1_0\int^2_0 x^2+\frac{xy}2\,dydx\\
&=\frac67\int^1_0x^2y+\frac{xy^2}4\bigg|^2_{y=0}\\
&=\frac67\int^1_0 2x^2+x\,dx\\
&=\frac67\left(\frac{2x^3}{3}+\frac{x^2}{2}\right)\bigg|^{1}_{x=0}\\
&=\frac67 \left(\frac23+\frac12\right)\\
&=\frac67\left(\frac{4+3}{6}\right)\\
&=\frac67\cdot\frac76\\
&=1
\end{align}
$$
因為他的積分結果為1，所以我們得證，$\frac67\left(x^2+\frac{xy}2\right)$是pdf。
#### (ii)
題目要我們計算$P(X>Y)$，那我們先回頭看一下X跟Y的定義域
$$
f_{X,Y}(x,y)=\frac67\left(x^2+\frac{xy}{2}\right),\quad0<x\leq1,\, 0<y\leq 2
$$
你可以看到，X最大就到1，而X要大於Y，所以定義域會被寫成：
$$
0<Y<X\leq1
$$
而我們根據這個定義域去做積分：
$$
\begin{align}
\int^1_0\int^x_0\frac{6}{7}\left(x^2+\frac{xy}2\right)\,dydx&=\int^1_0\frac67\cdot x\int^x_0\left(x+\frac y2\right)\,dydx\\
&=\int^1_0 \frac67x\left(xy+\frac{y^2}{4}\right)\bigg|^x_{y=0}\,dx\\
&=\int^1_0\frac67x\left(x^2+\frac{x^2}4\right)\,dx\\
&=\frac67\int^1_0 x^3+\frac{x^3}4\,dx\\
&=\frac67\left(\frac{x^4}4+\frac{x^4}{16}\right)|^1_{x=0}\\
&=\frac67\cdot\left(\frac{4}{16}+\frac{1}{16}\right)\\
&=\frac67\cdot\frac{5}{16}\\
&=\frac{15}{56}
\end{align}
$$
所以我們知道X>Y的機率是$\frac{15}{56}$。