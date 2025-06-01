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
我會用表格的方式去想這道題，會比較簡單一點：
##### $f_{X,Y}(x,y)$
$$
\begin{array}{|l|l|l|l|l|l|}
\hline
y\backslash x&1&2&\cdots&n\\
\hline
1&\frac{2}{n(n+1)}&\frac{2}{n(n+1)}&\cdots&\frac{2}{n(n+1)}\\
\hline
2&\frac{2}{n(n+1)}&\frac{2}{n(n+1)}&\cdots&\frac{2}{n(n+1)}\\
\hline
\vdots&\vdots&\vdots&\ddots&\vdots\\
\hline
x&\frac{2}{n(n+1)}&\frac{2}{n(n+1)}&\cdots&\frac{2}{n(n+1)}\\
\hline
\end{array}
$$
#### 第一小題
我們知道$X$的邊際機率密度函數就是把所有x的機率加總，例如