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
### **銷售（Sales）：**
#### Q-Q plot
![[MA Assignment1 QQ-plot Sales.png|500]]
$$
\begin{array}{cccc}
&\text{Sales}\\
\hline
\text{Ordered observations}&\text{Probability levels}&\text{Standard normal quantiles}\\
\hline
32416&0.05&-1.64\\
32416&0.05&-1.64\\									
35209&0.15&-1.04\\									
36156&0.25&-0.67\\									
39069&0.35&-0.39\\									
50976&0.45&-0.13\\									
55264&0.55&0.13\\									
63438&0.65&0.39\\									
86656&0.75&0.67\\									
96933&0.85&1.04\\									
126974&0.95&1.64\\
\end{array}
$$
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商銷售額的百分位數與理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的利潤服從常態分配。

而排列過的觀測值跟標準常態百分位數的相關係數約為「0.9362」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
由R得到其P-Value為「0.0000672」，故我們拒絕虛無假設，我們有足夠強烈的證據證明排列過的觀測值跟標準常態百分位數之間有顯著的線性關係。也就是各廠商的銷售額服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的銷售額是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}銷售額服從常態分配\quad  vs \quad  H_1\text{：}銷售額不服從常態分配
$$
由R得到其P-Value為「0.1018」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的銷售額不服從常態分配。

透過Q-Q plot、皮爾森相關係數以及Shapiro-Wilk test，我們皆得到**各廠商的銷售額服從常態分配**的結論。
### **利潤（Profits）：**
#### Q-Q plot
![[MA Assignment1 QQ-plot Profits.png|500]]
$$
\begin{array}{cccc}
&\text{Profits}\\
\hline
\text{Ordered observations}&\text{Probability levels}&\text{Standard normal quantiles}\\
\hline
359	&	0.05	&	-1.64	\\
1809	&	0.15	&	-1.04	\\
2413	&	0.25	&	-0.67	\\
2480	&	0.35	&	-0.39	\\
2946	&	0.45	&	-0.13	\\
3510	&	0.55	&	0.13	\\
3758	&	0.65	&	0.39	\\
3835	&	0.75	&	0.67	\\
3939	&	0.85	&	1.04	\\
4224	&	0.95	&	1.64	\\
\end{array}
$$
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商的利潤之百分位數與理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的利潤服從常態分配。

而排列過的觀測值跟標準常態百分位數的相關係數約為「0.9480」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
由R得到其P-Value為「0.00003009」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商利潤的排列過的觀測值跟標準常態百分位數之間有顯著的線性關係。也就是各廠商的利潤服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的利潤是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}利潤服從常態分配\quad  vs \quad  H_1\text{：}利潤不服從常態分配
$$
由R得到其P-Value為「0.2163」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的利潤不服從常態分配。 

透過Q-Q plot、皮爾森相關係數以及Shapiro-Wilk test，我們皆得到**各廠商的利潤服從常態分配**的結論。
### **資產（Assets）：**
#### Q-Q plot
![[MA Assignment1 QQ-plot Assets.png]]
$$
\begin{array}{cccc}
&\text{Assets}\\
\hline
\text{Ordered observations}&\text{Probability levels}&\text{Standard normal quantiles}\\
\hline
25636	&	0.05	&	-1.64	\\
34715	&	0.15	&	-1.04	\\
38528	&	0.25	&	-0.67	\\
39080	&	0.35	&	-0.39	\\
51038	&	0.45	&	-0.13	\\
77734	&	0.55	&	0.13	\\
83219	&	0.65	&	0.39	\\
128344	&	0.75	&	0.67	\\
160893	&	0.85	&	1.04	\\
173297	&	0.95	&	1.64	\\
\end{array}
$$
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商的利潤之百分位數與理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的利潤服從常態分配。

而Ordered observations跟Standard normal quantiles的相關係數約為「0.9358」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
由R得到其P-Value為「0.00006883」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商資產排列過的觀測值跟標準常態百分位數之間有顯著的線性關係。也就是各廠商的銷售額服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的銷售額是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}銷售額服從常態分配\quad  vs \quad  H_1\text{：}銷售額不服從常態分配
$$
由R得到其P-Value為「0.2163」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的銷售額不服從常態分配。 

透過Q-Q plot、皮爾森相關係數以及Shapiro-Wilk test，我們皆得到**各廠商的銷售額服從常態分配**的結論。

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