# 問題：
The r.v's $X$ and $Y$ have joint pdf of $f_{X,Y}$ given by the entries of the following table:
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3\\
\hline
1&1/8&1/16&3/16&1/8\\
\hline
2&1/16&1/16&1/8&1/4\\
\hline
\end{array}
$$
1. Determine the marginal pdf of $f_X$ and $f_Y$, and the conditional pdf $f_{X\mid Y}(\cdot\mid y),\,for\,\,y=1,2$.
2. Calculate: $E(X)$, $E(Y)$, $E(X\mid Y=y)$, $y=1,2$, and $E\left[E(X\mid Y)\right]$
3. Compare E(X) and $E\left[E(X\mid Y)\right]$.
4. Calculate: Var(X) and Var(Y)
# 回答：
#### 第一小題
##### 邊際機率密度函數
關於邊緣機率密度函數還有條件機率的算法，可以看[[chapter 4 2.4]]，這邊就不多做贅述。
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3&f_Y\\
\hline
1&1/8&1/16&3/16&1/8&1/2\\
\hline
2&1/16&1/16&1/8&1/4&1/2\\
\hline
f_X&3/16&2/16&5/16&3/8&1\\
\hline
\end{array}
$$
##### 條件機率
##### $f_{X\mid Y}(x,y)$
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3\\
\hline
1&\frac{1/8}{1/2}&\frac{1/16}{1/2}&\frac{3/16}{1/2}&\frac{1/8}{1/2}\\
\hline
2&\frac{1/16}{1/2}&\frac{1/16}{1/2}&\frac{1/8}{1/2}&\frac{1/4}{1/2}\\
\hline
\end{array}
\Rightarrow
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3&合計\\
\hline
1&1/4&1/8&3/8&1/4&1\\
\hline
2&1/8&1/8&1/4&1/2&1\\
\hline
\end{array}

$$
##### $f_{Y\mid X}(x,y)$
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3\\
\hline
1&\frac{1/8}{3/16}&\frac{1/16}{2/16}&\frac{3/16}{5/16}&\frac{1/8}{6/16}\\
\hline
2&\frac{1/16}{3/16}&\frac{1/16}{2/16}&\frac{1/8}{5/16}&\frac{1/4}{6/16}\\
\hline
\end{array}
\Rightarrow
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3\\
\hline
1&2/3&1/2&3/5&2/6\\
\hline
2&1/3&1/2&2/5&4/6\\
\hline
合計&1&1&1&1\\
\hline
\end{array}
$$
#### 第二小題
期望值的算法是：
$$
E(X)=\sum^n_{i=1}x\cdot f_{X,Y}
$$