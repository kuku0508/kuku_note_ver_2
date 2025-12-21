# 問題：
Suppose that $X_1,\ldots,X_n$ is a random sample from the following distribution.
$$
f(x;\theta)=\frac{\theta}{(1+x)^{\theta+1}},\quad0<x<\infty,\quad and \quad 0<\theta<\infty.
$$
1. Does this distribution belong to exponential family? State your reason.
2. Find a sufficient statistic for $\theta$.
# 回答：
#### 第一題
當我們要判斷一個分配是不是屬於exponential family的時候，我們需要進行以下的步驟：
	1. 寫出分配的pmf/pdf
	2. 把有包含參數的部分，改寫成exp的形式
	   $$
	   h(x)c(\theta)exp[T(x)Q(\theta)]
	   $$
	   其中：
	   $h(x)$：與$\theta$無關，可以為常數
	   $c(\theta)$：與$\theta$有關，不包含x
	   $T(x)$：與$\theta$無關，須包含x
	   $Q(\theta)$：與$\theta$有關，不可為常數

所以我們可以開始整理看看：
$$
\begin{align}
f(x;\theta)&=\frac{\theta}{(1+x)^{\theta+1}}\\
&=\theta\cdot(1+x)^{-(\theta+1)}\\
&=\underbrace{1}_{h(x)}\cdot\underbrace{\theta}_{c(\theta)}\cdot exp\lbrace\underbrace{\ln (1+x)}_{T(x)}\cdot\underbrace{[-(\theta+1)]}_{Q(\theta)}\rbrace
\end{align}
$$
故我們可以說$f(x;\theta)$為指數族。
#### 第二題
**Fisher-Neyman Factorization Theorem**
Let $X_1,\ldots,X_n$ be a random sample from $f(x;\theta)$ , $\theta\in \Omega$ , the statistic $T(\underline{X})$ is sufficient for $\theta$ if and only if the joint pdf of $X_1,\ldots,X_n$ factor as follows.
$$
f(\underline{X};\theta)=g(T(\underline{X}),\theta)h(\underline{X})
$$
where g depends on $X_1,\ldots,X_n$ only through T and h is independent of $\theta$

簡單來說，**我們只要把joint pdf整理成$g(T(\underline{X}),\theta)h(\underline{X})$**，就可以直接說by factorization Theorem，$T(\underline{X})$ is sufficient for $\theta$.
其中
$h(\underline{X})$：不含參數$\theta$的任何東西。
$g(T(\underline{X}),\theta)$：含$T(\underline{X})$，可以含$\theta$，可以是常數。

我們可以用factorization Theorem來做這題
我們只要把joint pdf整理成$g(T(\underline{X});\theta)h(x)$就好了。
$$
\begin{align}
f(\underline{X};\theta)&=\prod^n_{i=1}\frac{\theta}{(1+x_i)^{\theta+1}}\\
&=\prod^n_{i=1}\theta\cdot(1+x_i)^{-(\theta+1)}\\
&=\theta^n\prod^n_{i=1}(1+x_i)^{-\theta}\cdot(1+x_i)^{-1}\\
&=\prod^n_{i=1}(1+x_i)^{-1}\cdot\theta^n  \prod^n_{i=1} exp\left\lbrace-\theta\ln(1+x_i)\right\rbrace\\
&=\prod^n_{i=1}(1+x_i)^{-1}\cdot\theta^n exp\left\lbrace-\theta\sum^n_{i=1}\ln(1+x_i)\right\rbrace\\
&=\underbrace{\prod^n_{i=1}(1+x_i)^{-1}}_{h(x)}\cdot\underbrace{\theta^n exp\left\lbrace-\theta\underbrace{\sum^n_{i=1}\ln(1+x_i)}_{T(\underline{X})}\right\rbrace}_{g(T(\underline{X});\theta)}\\
\end{align}
$$
故我們可以說，by factorization theorem $\sum^n_{i=1}\ln(1+x_i)$ is sufficient for $\theta$.
