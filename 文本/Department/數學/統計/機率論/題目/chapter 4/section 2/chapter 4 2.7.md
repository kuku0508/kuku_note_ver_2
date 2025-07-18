# 問題：
In reference to [[chapter 4 1.3|Exercise 1.3]],calculate the marginal pdf $f_X$ and $f_Y$
# 回答：
題目要我們求以下pdf的邊際機率密度函數：
$$f_{X,Y}(x,y)=x+y,\quad 0<x< 1,\quad 0<y< 1$$
要求邊際機率密度函數其實就跟前面的表格求法一樣，只是我們有幾乎無限多的x跟y。
$$
\begin{array}{|l|l|l|l|l|l|}
\hline
y\backslash x&0&0.0\ldots1&\cdots&1\\
\hline
0&x+y&x+y&\cdots&x+y\\
\hline
0.0\ldots1&x+y&x+y&\cdots&x+y\\
\hline
\vdots&\vdots&\vdots&\ddots&\vdots\\
\hline
1&x+y&x+y&\cdots&x+y\\
\hline
\end{array}
$$
要求$f_X$，我們只要把同一行（一樣的x）所有的機率加起來，就可以得到個別的邊際機率。
而我們可以通過積分的方式來快速得到我們想要的值。
求$f_X$要把所有同一行的值全部相加，其實就等於對y做積分。所以：
$$
\begin{align}
f_X(x)&=\int^1_0 x+y\,dy\\
&=\left(\frac{y^2}2+xy\right)\bigg|^1_{y=0}\\
&=x+\frac{1}{2}
\end{align}
$$
同理，$f_Y$就是對x做積分：
$$
\begin{align}
f_Y(y)&=\int^1_0x+y\,dx\\
&=\left(\frac{x^2}2+xy\right)\bigg|^1_{x=0}\\
&=y+\frac12
\end{align}
$$
