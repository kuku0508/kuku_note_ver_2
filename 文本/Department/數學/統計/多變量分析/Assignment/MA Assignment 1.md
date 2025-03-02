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


我們已知如果$X$服從常態分配，則$(X-\mu)'\Sigma^{-1}(X-\mu)$會服從自由度為$X$變數數量的卡方分配。而$(\bar{X}-\mu)'\Sigma^{-1}(\bar{X}-\mu)$，我們由a小題已知，$\bar{X}$服從平均為$\mu$，共變異數為$\Sigma$的三維常態分配。故我們可知：
$$
(\bar{X}-\mu)'\Sigma^{-1}(\bar{X}-\mu)\sim\chi^2_3
$$

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
要檢驗三個變數是否符合常態假設，我們可以先檢視Q-Q Plot，看各個變數是否各自服從常態假設。當確定所有變數皆符合常態假設，我們便可以透過chi-square plot再檢視兩個變數之間是否服從二維常態。

## 一維常態檢測
透過R來執行，我們可以知道各個變數的Q-Q plot的點是否呈現一條直線，且變數是否會通過Shapiro-Wilk test，以確定變數是否會服從常態分配。
#### 銷售：




**Extra Question**：creating a plot of a bivariate normal distribution with 
$\mu_1=\mu_2=2$，$\sigma_1=\sigma_2=1$ and $\rho=0.5$ using SAS or R.


```R
Sales <- c(126974,96933,86656,63438,55264,50976,39069,36156,35209,32416)
Profits <- c(4224,3835,3510,3758,3939,1809,2946,359,2480,2413)
Assets <- c(173297,160893,83219,77734,128344,39080,38528,51038,34715,25636)

data_list <- list(Sales = Sales, Profits = Profits, Assets = Assets)

for(name in names(data_list)){
  x <- data_list[[name]]
  id <- seq_along(x)
  level <- (id - 0.5) / length(x)
  q <- qnorm(level)
  cat("=== ", name, " ===\n")
  print(data.frame(x, level, round(q, 2)))
  qqnorm(x, main = paste("QQ Plot for", name))
  qqline(x)
  print(shapiro.test(x))
}
```