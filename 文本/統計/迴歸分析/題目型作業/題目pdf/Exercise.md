![[Exercise.pdf]]
## a
$$
y=
\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}
\quad
X=
\begin{bmatrix}
1&1\\
1&2\\
1&3\\
1&4\\
1&5\\
\end{bmatrix}
\quad
\beta=
\begin{bmatrix}
\beta_0\\
\beta_1
\end{bmatrix}
\quad

\epsilon=
\begin{bmatrix}
\epsilon_1\\
\epsilon_2\\
\epsilon_3\\
\epsilon_4\\
\epsilon_5
\end{bmatrix}

$$
可以把簡單線性迴歸的公式以下列形式表達 $$
y=X\beta+\epsilon
$$
## b
$$
\hat{\beta}=(X'X)^{-1}X'y
$$
$X'$是轉置矩陣
那個-1，反矩陣
$$
\begin{align}
\hat{\beta}&=
\left(\begin{bmatrix}
1&1&1&1&1\\
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1&1\\
1&2\\
1&3\\
1&4\\
1&5
\end{bmatrix}\right)^{-1}

\begin{bmatrix}
1&1&1&1&1\\
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}
\\
&=

\left(
\begin{bmatrix}
1+1+1+1+1&1+2+3+4+5\\
1+2+3+4+5&1+4+9+16+25
\end{bmatrix}
\right)^{-1}

\begin{bmatrix}
1&1&1&1&1\\
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}

\\
&=

\left(
\begin{bmatrix}
55&-15\\
-15&5
\end{bmatrix}
\right)^{-1}

\begin{bmatrix}
1&1&1&1&1\\
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}
\\
&=
\begin{bmatrix}
\frac{11}{10}&-\frac{3}{10}\\
-\frac{3}{10}&\frac{1}{10}
\end{bmatrix}


\begin{bmatrix}
1&1&1&1&1\\
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}

\\
&=
\begin{bmatrix}
\frac{8}{10}&\frac{5}{10}&\frac{2}{10}&-\frac{1}{10}&-\frac{4}{10}\\
-\frac{2}{10}&-\frac{1}{10}&\frac{0}{10}&\frac{1}{10}&\frac{2}{10}
\end{bmatrix}

\begin{bmatrix}
1\\
1\\
2\\
2\\
4
\end{bmatrix}
\\
&=
\begin{bmatrix}
\frac{8+5+4-2-16}{10}\\
\frac{-2-1-0+2+8}{10}
\end{bmatrix}

\\
&=
\begin{bmatrix}
\frac{-1}{10}\\
\frac{7}{10}
\end{bmatrix}

\end{align}
$$
## c
$$
\begin{align}
H&=X(X'X)^{-1}X'\\
&=
\begin{bmatrix}
1\\2\\3\\4\\5
\end{bmatrix}

\left(
\begin{bmatrix}
1&2&3&4&5
\end{bmatrix}

\begin{bmatrix}
1\\2\\3\\4\\5
\end{bmatrix}

\right)^{-1}
\begin{bmatrix}
1&2&3&4&5
\end{bmatrix}
\\
&=
\begin{bmatrix}
1\\2\\3\\4\\5
\end{bmatrix}
55
\end{align}
$$