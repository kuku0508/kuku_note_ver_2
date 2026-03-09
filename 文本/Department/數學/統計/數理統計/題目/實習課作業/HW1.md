##### (1)$X_1,X_2,\cdots,X_n\overset{i.i.d}{\sim}U(0,\theta),\theta\in\Omega=(0,\infty).$ Let $Y_n$ be the largest order statistic of $X_i$'s.

##### (a) Find $f_{Y_n}(y_n)$ 

Find $F_{Y_n}(y_n)$ first
$$
\begin{align}
F_{Y_n}(y)&=P(Y_n\leq y)\\&
=P(X_1\leq y,\ldots,X_n\leq y)\\\\
&=\prod^n_{i=1}P(X_i\leq y)\\\\
P(X_i\leq y)&=
\begin{cases}
0,&y\leq 0\\
\frac{y}{\theta},&0<y<\theta\\
1,&y\geq\theta
\end{cases}
\end{align}
$$
$$
\begin{align}
\because P(Y_n\leq y)&=P(X_1\leq y,\ldots,X_n\leq y) \& X_i \text{ is i.i.d}\\
\Rightarrow F_{Y_n}(y)&=P(Y_n\leq y )=(P(X_1\leq y))^n=\left(\frac{y}{\theta}\right)^n\\
&\Rightarrow 
F_{Y_n}(y)=
\begin{cases}
0,&y\leq 0\\
(\frac{y}{\theta})^n,&0<y<\theta\\
1,&y\geq\theta
\end{cases}
\end{align}
$$
$$
\begin{align}
f_{Y_n}(y_n)&=\frac{d}{dy}F_{Y_n}(y)\\
&=\frac{d}{dy}\,\frac{y^n}{\theta^n}\\
&=\frac{n}{\theta^n} \cdot y^{(n-1)}\\
&\Rightarrow f_{Y_n}(y_n)
=\begin{cases}
\frac{n}{\theta^n} \cdot y^{(n-1)},&0<y<\theta\\
0,&o.w.
\end{cases}
\end{align}
$$
##### (b) Find the unbiased estimate of $\theta$ based on $Y_n$ 
$$
\begin{align}
E(Y_n)&=\int^\theta_0 y\cdot \frac{n}{\theta^n}y^{n-1}dy\\
&=\frac{n}{\theta^n}\int^\theta_0 y^n dy\\
&= \frac{n}{\theta^n}\left[\frac{y^{n+1}}{n+1}\right]^\theta_0\\
&=\frac{n}{\theta^n}\cdot\frac{\theta^{n+1}}{n+1}=\frac{n}{n+1}\theta
\end{align}
$$
let $\hat{\theta}=cY_n$ ，
$\because unbiased$
$\rightarrow E(\hat{\theta})=E(cY_n)=cE(Y_n)=\theta$
$\Rightarrow c\cdot \frac{n}{n+1}\theta=\theta$
$\Rightarrow c=\frac{n+1}{n}$
故
$\Rightarrow \hat{\theta}=\frac{n+1}{n}Y_n$

(2)$X_1,X_2,\ldots,X_n$ be independent r.v's, $f(x;\theta)=\frac{1}{\theta}e^{\frac{-x}{\theta}},x>0,\theta\in\Omega=(0,\infty)$
(a) Find sufficient statistics.
$$
\begin{align}
f(\underline{X};\theta)&=\prod^n_{i=1}\frac{1}{\theta}e^{-x_i/\theta}\\
&=\underbrace{\frac{1}{\theta^n}exp\left(-\frac{1}{\theta}\sum^n_{i=1}x_i\right)}_{g(T(\underline{X}),\theta)}\cdot \underbrace{1}_{h(\underline{X})}
\end{align}
$$
By Factorization theorem
$\sum^n_{i=1}X_i$ is sufficient statistic for $\theta$.