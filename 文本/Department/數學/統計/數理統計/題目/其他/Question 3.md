# 問題：
Let $X_1,X_2,\ldots,X_n$ be a random sample from Poisson distribution with parameter $\theta$.
1. What is the support of Poisson distribution?
2. What is the parameter space of Poisson distribution?
3. Show that the Poisson distribution is of the one-parameter exponential family.
4. Let $T=\sum^n_{i=1}X_i$ . Use the defintion to show that $T$ is a sufficient statistic for $\theta$.
5. Use the factorization theorem to show that T is a sufficient statistic for $\theta$.
6. Is $T$ a minimal sufficient statistic? Why?
# 回答： 
#### 第一題
可能要先翻譯一下，反正所謂support of Poisson distribution
就是指「隨機變數可能取到、且機率為正的所有值」
所以就是X的範圍，也就是：
$$
X=\lbrace0,1,2,\ldots\rbrace
$$
#### 第二題
簡單來說，他問的就是$\theta$的範圍，而我們知道卜瓦松分配參數的範圍，就是大於0就可以了，所以就寫：
$$
\theta=(0,\infty)
$$
#### 第三題
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
	   
所以在這題裡面，我們可以把卜瓦松分配的pmf：
$$
f(x;\theta)=\frac{e^{-\theta}\cdot\theta^x}{x!}
$$
裡面的
$$
\begin{align}
\theta^x&\xrightarrow{改寫成}e^{xln\theta}\\\\
&\Rightarrow \frac{e^{-\theta}\cdot e^{xln\theta}}{x!}\\
&=\frac{e^{-\theta+xln\theta}}{x!}\\
&=\frac{1}{x!}exp\left\lbrace xln\theta-\theta\right\rbrace\\
&=\frac{1}{x!}\cdot e^{-\theta}exp[x\cdot ln\theta]\\
&=h(x)\cdot c(\theta)exp[T(x)\cdot Q(\theta)]
\end{align}
$$
則得證，卜瓦松分配為指數族。

#### 第四題
sufficient statistic 充分統計量
A statistic $T(\underline{X})$ is a sufficient statistic for $\theta$ if the conditional distribution of the sample $\underline{X}$ given the value of $T(\underline{X})$ does not depend on $\theta$ that is $f_{\underline{X}\mid T}(\underline{x}\mid t)$ is independent of $\theta$ .

也就是當在給定$T(\underline{X})=t$ 的前提下，若條件分配
$$
f_{\underline{X}\mid T}(\underline{x}\mid t)
=\frac{P(\underline{X}=x,T(\underline{X})=T(x))}{P(T(\underline{X})=t)}
=\frac{P(X=x)}{P(T(\underline{X})=t)}
=\frac{f_{\underline{X}}(x;\theta)}{f_T(t;\theta)}
$$
若此條件分配不含參數$\theta$，則$T(\underline{X})$為充分統計量。
其中
$f_{\underline{X}}(x;\theta)$為joint pmf/pdf。
$f_T(t;\theta)$為T的pmf/pdf

那我們先算Poisson distribution 的 joint pmf 算出來：
$$
P(X=x)=\prod^n_{i=1}\frac{e^{-\theta}\theta^{x_i}}{x_i!}=\frac{e^{-n\theta}\theta^{\sum^n_{i=1}{x_i}}}{\prod^n_{i=1}x_i!}
$$
而因為sufficient statistic 充分統計量
A statistic $T(\underline{X})$ is a sufficient statistic for $\theta$ if the conditional distribution of the sample $\underline{X}$ given the value of $T(\underline{X})$ does not depend on $\theta$ that is $f_{\underline{X}\mid T}(\underline{x}\mid t)$ is independent of $\theta$ .

也就是當在給定$T(\underline{X})=t$ 的前提下，若條件分配
$$
F_{\underline{X}\mid T}(\underline{x}\mid t)
=\frac{f_{\underline{X}}(x;\theta)}{f_T(t;\theta)}
$$
若此條件分配不含參數$\theta$，則$T(\underline{X})$為充分統計量。
其中$P(X=x)$為joint pmf/pdf。

而因為$T=\sum^n_{i=1}x_i$，因為Poisson的加總還是Poisson，且其參數會變為$n\theta$，所以我們可以知道：
$$
T\sim Poisson(n\theta)
$$
我們就可以知道：
$$
P(T=t)=\frac{e^{-n\theta}(n\theta)^{t}}{t!}
$$
故我們可以得到：
$$
\begin{align}
f_{\underline{X}\mid T}(\underline{x}\mid t)
&=\frac{f_{\underline{X}}(x;\theta)}{f_T(t;\theta)}\\\\
&=\frac{\frac{\cancel{e^{-n\theta}}\theta^{\sum^n_{i=1}{x_i}}}{\prod^n_{i=1}x_i!}}{\frac{\cancel{e^{-n\theta}}(n\theta)^{t}}{t!}}\\\\
&=\frac{\frac{\cancel{\theta^{t}}}{\prod^n_{i=1}x_i!}}{\frac{n^{t}\cancel{\theta^{t}}}{t!}}\\\\
&=\frac{t!}{\prod^n_{i=1}x_i!\,n^{t}}
\end{align}
$$
我們可以發現條件機率$F_{\underline{X}\mid T}(\underline{x}\mid t)$中並不包含參數$\theta$，故T對於參數$\theta$來說是充分統計量。

但他後面的分數寫
$$
\frac{\frac{1}{\sqrt{2\pi\sigma^2}}exp[\frac{\sum(x_i-\mu)^2}{2\sigma^2}]}{\frac{1}{\sqrt{2\pi\sigma^2}}exp[\frac{\sum(y_i-\mu)^2}{2\sigma^2}}
$$