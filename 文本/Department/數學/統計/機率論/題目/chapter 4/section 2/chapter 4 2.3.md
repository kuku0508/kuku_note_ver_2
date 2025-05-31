# 問題：
If the joint pdf of the r.v's $X$ and $Y$ is given by the following table, determine the marginal pdf of $f_X$ and $f_Y$.
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&-4&-2&2&4\\
\hline
-2&0&0.25&0&0\\
\hline
-1&0&0&0&0.25\\
\hline
1&0.25&0&0&0\\
\hline
2&0&0&0.25&0\\
\hline
\end{array}
$$
# 回答：
就跟[[chapter 4 2.1]]還有[[chapter 4 2.2]]一樣，我們只要把$X=x$的機率全部加總，就可以得到$f_X(X=x)$的邊際機率密度。不多說，開始加總：
$$
\begin{array}{|l|l|l|l|l|}
\hline
y\backslash x&-4&-2&2&4&f_Y\\
\hline
-2&0&0.25&0&0&0.25\\
\hline
-1&0&0&0&0.25&0.25\\
\hline
1&0.25&0&0&0&0.25\\
\hline
2&0&0&0.25&0&0.25\\
\hline
f_X&0.25&0.25&0.25&0.25&1\\
\hline
\end{array}
$$
done.