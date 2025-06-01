# 問題：
Let the r.v X and Y have the joint pdf:
$$
f_{X,Y}(x,y)=\frac{2}{n(n+1)},\quad y=1,2\ldots ,x;\,x=1,2\ldots,n
$$
Then compute:
1. The marginal pdf $f_X$ and $f_Y$.
2. The conditional pdf's $f_{X\mid Y}(x,y)$ and $f_{Y\mid X}(x,y)$.
3. The conditional expectations $E(X\mid Y=y)$ and $E(Y\mid X=x)$.
# 回答：
我們看一下我們可以知道有機率的部分，在$1\leq y \leq x \leq n$。
我們用表格的方式呈現這個題目會變成：
##### $f_{X,Y}(x,y)$
$$
\begin{array}{|l|l|l|l|l|l|}
\hline
y\backslash x&1&2&\cdots&n\\
\hline
1&\frac{2}{n(n+1)}&\frac{2}{n(n+1)}&\cdots&\frac{2}{n(n+1)}\\
\hline
2&0&\frac{2}{n(n+1)}&\cdots&\frac{2}{n(n+1)}\\
\hline
\vdots&\vdots&\vdots&\ddots&\vdots\\
\hline
x&0&0&\cdots&\frac{2}{n(n+1)}\\
\hline
\end{array}
$$
#### 第一小題
我們知道$f_X$就是把所有$X=x$的機率加總：
$$
f_X=\sum^x_{y=1}\frac{2}{n(n+1)}=x\cdot\frac{2}{n(n+1)}=\frac{2x}{n(n+1)}
$$

$$
f_X=
\begin{cases}
\frac{2x}{n(n+1)},&x=1,2,\ldots,n\\\\
0,&\text{otherwise}
\end{cases}
$$
而$f_Y$我們需要加的是將$Y=y$中符合條件的範圍中的機率，也就是$y\leq x$的機率
$$
f_Y=\sum_{x=y}^n\frac{2}{n(n+1)}=(n-y+1)\cdot\frac{2}{n(n+1)}=\frac{2(n-y+1)}{}
$$