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
E(X)=\sum^n_{i=1}x\cdot f_X=0\cdot\frac{3}{16}+1\cdot\frac{2}{16}+2\cdot\frac{5}{16}+3\cdot\frac{3}{8}=\frac{15}{8}=1.875
$$
$$
E(Y)=\sum^n_{i=1}y\cdot f_Y=1\cdot\frac12+2\cdot\frac12=\frac32
$$

$$
\begin{align}
&E(X\mid Y=y)=\sum^n_{i=1}x\cdot f_{X\mid Y}(X\mid Y=y)\\
&E(X\mid Y=1)=\sum^n_{i=1}x\cdot f_{X\mid Y}(X\mid Y=1)=0\cdot\frac14+1\cdot\frac18+2\cdot\frac38+3\cdot\frac14=\frac18+\frac68+\frac34=\frac{13}{8}\\
\\
&E(X\mid Y=2)=\sum^n_{i=1}x\cdot f_{X\mid Y}(X\mid Y=2)=0\cdot\frac18+1\cdot\frac18+2\cdot\frac14+3\cdot\frac12=\frac18+\frac24+\frac32=\frac{17}8
\end{align}
$$
