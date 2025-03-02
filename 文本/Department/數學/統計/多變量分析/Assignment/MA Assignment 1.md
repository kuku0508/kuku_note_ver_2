![[MA Assignment 1.pdf]]
## 1.
Let $X_1,\ldots,X_{36}$ be a random sample of size 36 from a three-variate normal distribution having mean $\mu$ and covariance $\Sigma$. Specify each of the following completely.
 (a) The distribution of $\bar{X}$.
 (b) The distribution of $n(\bar{X}-\mu)'\Sigma^{-1}(\bar{X}-\mu)$.


(a)
由於題目說樣本為random sample，
可以知道$X_1、X_2\ldots、X_{36}$相互獨立且來自相同分布$N_3(\mu,\Sigma)$
故：
$$
X\sim N_3(\mu,\Sigma)
$$
而我們要求$\bar{X}$的分配，也就是
$$
\bar{X}=\frac{1}{36}\sum^{36}_{i=1}X_i
$$
我們已知如果$X$服從常態分配，則$X$的線性組合也會服從常態分配。
而$\frac{1}{36}\sum^{36}_{i=1}X_i$為$X_i$的線性組合，且$X_i$服從三維常態分配。
故$\bar{X}$也服從三維常態分配。

而其期望值為：
$$
E(\bar{X})=\mu
$$
變異數為：
$$
Cov(\bar{X})=\frac{1}{n}\Sigma=\frac{1}{36}\Sigma
$$
(b)


我們已知如果$X$服從常態分配，則$(X-\mu)'\Sigma^{-1}(X-\mu)$會服從自由度為$X$變數數量的卡方分配。而$(\bar{X}-\mu)'\Sigma^{-1}(\bar{X}-\mu)$，我們已知

## 2.
Check whether the following data satisfy the normality assumption.
$$
\begin{array}{lrrr}
\hline
\text{Company}&X_1-\text{Sales}&X_2-\text{Profits}&X_3-\text{Assets}\\
\hline
\text{General Motors}&126974&4224&173297\\
\text{Ford}&96933&3835&160893\\
\text{Exxon}&86656&3510&83219\\
\text{IBM}&63438&3758&77734\\
\text{General Electric}&55264&3939&128344\\
\text{Mobil}&50976&1809&39080\\
\text{Philip Morris}&39069&2946&38528\\
\text{Chrysler}&36156&359&51038\\
\text{Du Pont}&35209&2480&34715\\
\text{Texaco}&32416&2413&25636
\end{array}
$$
**Extra Question**：creating a plot of a bivariate normal distribution with 
$\mu_1=\mu_2=2$，$\sigma_1=\sigma_2=1$ and $\rho=0.5$ using SAS or R.

