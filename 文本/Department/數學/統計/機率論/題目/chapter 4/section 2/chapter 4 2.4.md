# 問題：
The r.v $X$ and $Y$ take on the values 1, 2 and 3, as indicated in the following table:
$$
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3\\
\hline
1&2/36&2/36&3/36\\
\hline
2&1/36&10/36&3/36\\
\hline
3&4/36&5/36&6/36\\
\hline
\end{array}
$$
1. Determine the marginal pdf of $f_X$ and $f_Y$.
2. Determine the conditional pdf of $f_{X\mid Y}(\cdot\mid y)$ and $f_{Y\mid X}(\cdot\mid x)$.
# 回答：
第一小題，詳細的我就不說了，請參照[[chapter 4 2.1]]、[[chapter 4 2.2]]。反正就加總就好。
$$
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3&f_Y\\
\hline
1&2/36&2/36&3/36&7/36\\
\hline
2&1/36&10/36&3/36&14/36\\
\hline
3&4/36&5/36&6/36&15/36\\
\hline
f_X&7/36&17/36&12/36&1\\
\hline
\end{array}
$$
第二小題，我們得到條件機率的方法就是：
$$
f_{(X\mid Y)}(x,y)=\frac{f_{X,Y}(x,y)}{f_Y(y)}\quad;\quad f_{(Y\mid X)}(x,y)=\frac{f_{X,Y}(x,y)}{f_X(x)}
$$
#### $f_{(X\mid Y)}(x,y)$
$$
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3\\
\hline
1&\frac{2/36}{7/36}&\frac{2/36}{7/36}&\frac{3/36}{7/36}\\
\hline
2&\frac{1/36}{14/36}&\frac{10/36}{14/36}&\frac{3/36}{14/36}\\
\hline
3&\frac{4/36}{15/36}&\frac{5/36}{15/36}&\frac{6/36}{15/36}\\
\hline
\end{array}
\Rightarrow
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3&合計\\
\hline
1&2/7&2/7&3/7&1\\
\hline
2&1/14&5/7&3/14&1\\
\hline
3&4/15&1/3&2/5&1\\
\hline
\end{array}
$$
#### $f_{(Y\mid X)}(x,y)$
$$
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3\\
\hline
1&\frac{2/36}{7/36}&\frac{2/36}{17/36}&\frac{3/36}{12/36}\\
\hline
2&\frac{1/36}{7/36}&\frac{10/36}{17/36}&\frac{3/36}{12/36}\\
\hline
3&\frac{4/36}{7/36}&\frac{5/36}{17/36}&\frac{6/36}{12/36}\\
\hline
\end{array}
\Rightarrow
\begin{array}{|l|l|l|l|}
\hline
y\backslash x&1&2&3\\
\hline
1&2/7&2/17&3/12\\
\hline
2&1/7&10/17&3/12\\
\hline
3&4/7&5/17&6/12\\
\hline
合計&1&1&1\\
\hline
\end{array}
$$