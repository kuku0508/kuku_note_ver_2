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
&E(X\mid Y=y)=\sum^n_{x=1}x\cdot f_{X\mid Y}(X\mid Y=y)\\
&E(X\mid Y=1)=\sum^3_{x=0}x\cdot f_{X\mid Y}(X\mid Y=1)=0\cdot\frac14+1\cdot\frac18+2\cdot\frac38+3\cdot\frac14=\frac18+\frac68+\frac34=\frac{13}{8}\\
\\
&E(X\mid Y=2)=\sum^3_{x=0}x\cdot f_{X\mid Y}(X\mid Y=2)=0\cdot\frac18+1\cdot\frac18+2\cdot\frac14+3\cdot\frac12=\frac18+\frac24+\frac32=\frac{17}8
\end{align}
$$

接下來的就麻煩一點了，我們要求$E[E(X|Y)]$，我們先稍微理解一下這個是什麼意思。
$E(X|Y)$，就像前面講的，是指我們給定一個Y值的時候，X的期望值是多少。而E(X|Y)本質上來講他是一個隨機變數，他會根據Y的值的不同，而得到不同的期望值，在這個題目裡面，有$Y=1$的$\frac{13}{8}$，也有$Y=2$的$\frac{17}{8}$。而既然是隨機變數，那我們肯定可以去算出$Y=y$的機率是多少，其實就是Y的邊際機率。以這個題目來講Y不論等於1或2，他的機率都是$\frac12$。有了實際的值跟機率，我們就可以去算出他的期望值。也就是$E[E(X|Y)]$。
$$
\begin{align}
E[E(X\mid Y)]&=\sum^2_{y=1} E(X\mid Y=y)\cdot f_Y\\
&=\frac{13}8\cdot\frac12+\frac{17}8\cdot\frac12\\
&=\frac{13}{16}+\frac{17}{16}\\
&=\frac{30}{16}=\frac{15}8
\end{align}
$$
#### 第三小題
你可以注意到一件事情，$E[E(X\mid Y)]$的值跟$E(X)$是一模一樣的，並不是巧合，而是本來就會一樣，在$E[E(Y\mid X)]$的時候，他也會跟$E(Y)$一樣。

#### 第四小題
關於變異數的算法，我們可以透過以下的公式來算變異數：
$$
Var(X)=E(X^2)-E(X)^2
$$
$$
\begin{align}
Var(X)=E(X^2)-E(X)^2&=\left(
0^2\cdot\frac{3}{16}+1^2\cdot\frac{2}{16}+2^2\cdot\frac{5}{16}+3^2\cdot\frac{3}{8}\right)-\left(\frac{15}{8}\right)^2\\
&=\frac{2}{16}+\frac{5}{4}+\frac{27}{8}-\frac{225}{64}\\
&=\frac{79}{64}\approx1.234375
\end{align}
$$
$$
\begin{align}
Var(Y)=E(Y^2)-E(Y)^2&=\left(1^2\cdot\frac12+2^2\cdot\frac12\right)-\left(\frac32\right)^2\\
&=\left(\frac12+2\right)-\frac94\\
&=
\end{align}
$$