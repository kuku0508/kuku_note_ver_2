# 問題：
In reference to Exercise 2.1 , calculate:
1. EX, EY, Var(X), and Var(Y)
2. Cov(X,Y) and $\rho(X,Y)$
3. Decide on the kind of correlation of the r.v $X$ and $Y$ 
![[table of chapter 4 1.1.png|400]]
# 回答：
#### 第一小題 
在2.1小題我們得到了$f_X$，我們就可以得到X的期望值：
$$
\begin{array}{|l|l|l|l|l|l|l|}
\hline
y\backslash x&0&1&2&3&4&5&f_Y\\
\hline
0&0.025&0.050&0.125&0.150&0.100&0.050&0.500\\
\hline
1&0.015&0.030&0.075&0.090&0.060&0.030&0.300\\
\hline
2&0.010&0.020&0.050&0.060&0.040&0.020&0.200\\
\hline
f_X&0.050&0.100&0.250&0.300&0.200&0.100&1.000\\
\hline
\end{array}
$$
$$
\begin{align}
EX&=\sum x \cdot f_X\\
&=0\cdot0.05+1\cdot0.1+2\cdot0.25+3\cdot0.3+4\cdot0.2+5\cdot0.1\\
&=0.1+0.5+0.9+0.8+0.5=2.8
\end{align}
$$

$$
\begin{align}
EY&=\sum y\cdot f_Y\\
&=0\cdot 0.5+1\cdot 0.3+2\cdot0.2\\
&=0.7
\end{align}
$$
$$
\begin{align}
Var(X)&=E(X^2)-E(X)^2\\
&=(0^2\cdot0.05+1^2\cdot0.1+2^2\cdot0.25+3^2\cdot0.3+4^2\cdot0.2+5^2\cdot0.1)-2.8^2\\
&=0.1+1+2.7+3.2+2.5-2.8^2=1.6
\end{align}
$$
$$
\begin{align}
Var(Y)&=E(Y^2)-E(Y)^2\\
&=0^2\cdot 0.5+1^2\cdot 0.3+2^2\cdot0.2-0.7^2\\
&=0.61
\end{align}
$$
#### 第二小題
$$
\begin{align}
\text{Cov}(x,y)&=E(XY)-E(X)E(Y)\\
&=\sum xy\cdot f_{X,Y}-E(X)E(Y)\\
&=(1\cdot1\cdot0.03+1\cdot2\cdot0.02+2\cdot1\cdot0.075+2\cdot2\cdot0.05+3\cdot1\cdot0.09+3\cdot2\cdot0.06\\&+4\cdot1\cdot0.06+4\cdot2\cdot0.04+5\cdot1\cdot0.03+5\cdot2\cdot0.02)-2.8\cdot0.7\\\\
&=(0.03+0.04+0.15+0.2+0.27+0.36+0.24+0.32+0.15+0.2)-2.8\cdot0.7\\
&=
\end{align}
$$

# 我去洗澡(5:39)