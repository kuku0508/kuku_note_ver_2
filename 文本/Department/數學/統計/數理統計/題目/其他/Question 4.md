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
我們可以用factorization Theorem來做這題
我們只要把joint pdf整理成$g(T(\underline{X});\theta)h(x)$就好了。
$$
\begin{align}
f(\underline{X};\theta)&=\prod^n_{i=1}\frac{\theta}{(1+x_i)^{\theta+1}}\\
&=\prod^n_{i=1}\theta\cdot(1+x_i)^{-(\theta+1)}\\
&=\theta^n\prod^n_{i=1}(1+x_i)^{-\theta}\cdot(1+x_i)^{-1}\\
&=\prod^n_{i=1}(1+x_i)^{-1}\cdot\theta^nexp\left\lbrace-\theta\ln(1+)\right\rbrace
\end{align}
$$
