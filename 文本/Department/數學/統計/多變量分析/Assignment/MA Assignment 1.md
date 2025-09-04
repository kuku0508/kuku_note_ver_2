[[MA Assignment]]
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
### **銷售額（Sales）：**
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
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商銷售額排列過的觀測值跟理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的銷售額服從常態分配。

而銷售額排列過的觀測值跟標準常態百分位數的相關係數約為「0.9362」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.0000672」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商銷售額排列過的觀測值跟理論上的標準常態百分位數之間有顯著的線性關係。也就是各廠商的銷售額服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的銷售額是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}銷售額服從常態分配\quad  vs \quad  H_1\text{：}銷售額不服從常態分配
$$
根據R的輸出，其P-Value為「0.1018」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的銷售額不服從常態分配。

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
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商利潤排列過的觀測值跟理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的利潤服從常態分配。

而各廠商利潤排列過的觀測值跟理論上的標準常態百分位數的相關係數約為「0.9480」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.00003009」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商利潤排列過的觀測值跟理論上的標準常態百分位數之間有顯著的線性關係。也就是各廠商的利潤服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的利潤是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}利潤服從常態分配\quad  vs \quad  H_1\text{：}利潤不服從常態分配
$$
根據R的輸出，其P-Value為「0.2163」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的利潤不服從常態分配。 

透過Q-Q plot、皮爾森相關係數以及Shapiro-Wilk test，我們皆得到**各廠商的利潤服從常態分配**的結論。
### **資產（Assets）：**
#### Q-Q plot
![[MA Assignment1 QQ-plot Assets.png|500]]
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
我們可以看到Q-Q plot上各個點呈現出明顯的直線。也就是各廠商資產排列過的觀測值跟理論上的標準常態百分位數所構成的點，呈現直線。即各廠商的資產服從常態分配。

而各廠商資產排列過的觀測值跟理論上的標準常態百分位數的相關係數約為「0.9358」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.00006883」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商資產排列過的觀測值跟標準常態百分位數之間有顯著的線性關係。也就是各廠商的資產服從常態分配。

#### Shapiro-Wilk test
而在Shapiro-Wilk test中，我們直接檢測各廠商的資產是否服從常態分配。
而其虛無假設為：
$$
H_0\text{：}資產服從常態分配\quad  vs \quad  H_1\text{：}資產不服從常態分配
$$
根據R的輸出，其P-Value為「0.2163」，故我們不拒絕虛無假設，我們沒有足夠強烈的證據證明各廠商的資產不服從常態分配。 

透過Q-Q plot、皮爾森相關係數以及Shapiro-Wilk test，我們皆得到**各廠商的資產服從常態分配**的結論。

## 二維常態檢測
透過R來執行，我們可以知道各個變數的Chi-square plot的點是否呈現一條直線，若可以證明馬氏距離的平方與卡方分配百分位數呈現線性關係，則可以確定變數是否會服從常態分配。
### **銷售（Sales）&利潤（Profits）**
![[MA Assignment1 chi-square plot Sales Profits.png|500]]
$$
\begin{array}{}
&\text{Sales＆Profits}\\
\hline
\text{id}&\text{Squared Mahalanobis Distance}&\chi^2_2\,\text{Quantile}\\
\hline
1	&	0.59	&	0.1	\\
2	&	0.81	&	0.33	\\
3	&	0.83	&	0.58	\\
4	&	0.97	&	0.86	\\
5	&	1.01	&	1.2	\\
6	&	1.02	&	1.6	\\
7	&	1.2	&	2.1	\\
8	&	1.88	&	2.77	\\
9	&	4.34	&	3.79	\\
10	&	5.33	&	5.99	\\
\end{array}
$$
我們可以看到Chi-Square plot上各個點呈現出明顯的直線。也就是各廠商銷售額以及利潤的馬氏距離的平方與卡方分配百分位數所構成的點，呈現直線。即各廠商的銷售額以及利潤服從二維常態分配。

而各廠商銷售額以及利潤的馬氏距離的平方與卡方分配百分位數的相關係數約為「0.9584」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.00001248」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商銷售額以及利潤的馬氏距離的平方與卡方分配百分位數之間有顯著的線性關係。也就是各廠商銷售額以及利潤服從二維常態分配。

透過Chi-Square plot、皮爾森相關係數，我們皆得到**各廠商銷售額以及利潤服從二維常態分配**的結論。
### **銷售（Sales）&資產（Assets）**
![[MA Assignment1 chi-square plot Sales Assets.png|500]]
$$
\begin{array}{}
&\text{Sales＆Assets}\\
\hline
\text{id}&\text{Squared Mahalanobis Distance}&\chi^2_2\,\text{Quantile}\\
\hline
1	&	0.04	&	0.1	\\
2	&	0.62	&	0.33	\\
3	&	0.78	&	0.58	\\
4	&	0.81	&	0.86	\\
5	&	1.03	&	1.2	\\
6	&	1.05	&	1.6	\\
7	&	2.27	&	2.1	\\
8	&	2.33	&	2.77	\\
9	&	4.23	&	3.79	\\
10	&	4.84	&	5.99	\\
\end{array}
$$
我們可以看到Chi-Square plot上各個點呈現出明顯的直線。也就是各廠商銷售額以及資產的馬氏距離的平方與卡方分配百分位數所構成的點，呈現直線。即各廠商銷售額以及資產服從二維常態分配。

而各廠商銷售額以及資產的馬氏距離的平方與卡方分配百分位數的相關係數約為「0.9584」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.00001248」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商銷售額以及資產的馬氏距離的平方與卡方分配百分位數之間有顯著的線性關係。也就是各廠商銷售額以及資產服從二維常態分配。

透過Chi-Square plot、皮爾森相關係數，我們皆得到**各廠商銷售額以及資產服從二維常態分配**的結論。
### **利潤（Profits）&資產（Assets）**
![[MA Assignment1 chi-square plot Profits Assets.png|500]]

$$
\begin{array}{}
&\text{Profits＆Assets}\\
\hline
\text{id}&\text{Squared Mahalanobis Distance}&\chi^2_2\,\text{Quantile}\\
\hline
1	&	0.42	&	0.1	\\
2	&	0.82	&	0.33	\\
3	&	0.86	&	0.58	\\
4	&	0.9	&	0.86	\\
5	&	1.07	&	1.2	\\
6	&	1.19	&	1.6	\\
7	&	1.23	&	2.1	\\
8	&	2.26	&	2.77	\\
9	&	2.86	&	3.79	\\
10	&	6.37	&	5.99	\\
\end{array}
$$
我們可以看到Chi-Square plot上各個點呈現出明顯的直線。也就是各廠商利潤以及資產的馬氏距離的平方與卡方分配百分位數所構成的點，呈現直線。即各廠商利潤以及資產的服從二維常態分配。

而各廠商利潤以及資產的馬氏距離的平方與卡方分配百分位數的相關係數約為「0.9583」
且以獨立性檢定檢測皮爾森相關係數是否為0（是否有線性關係）。其虛無假設為：
$$
H_0\text{：}\rho =0\quad  vs \quad  H_1\text{：}\rho\neq0
$$
根據R的輸出，其P-Value為「0.00001248」，故我們拒絕虛無假設，我們有足夠強烈的證據證明各廠商利潤以及資產的馬氏距離的平方與卡方分配百分位數之間有顯著的線性關係。也就是各廠商利潤以及資產服從二維常態分配。

透過Chi-Square plot、皮爾森相關係數，我們皆得到**各廠商利潤以及資產服從二維常態分配**的結論。

**Extra Question**：creating a plot of a bivariate normal distribution with 
$\mu_1=\mu_2=2$，$\sigma_1=\sigma_2=1$ and $\rho=0.5$ using R.

我們現在有平均數、變異數跟相關係數，要把二維常態分配的圖畫出來，我們還需要兩個變數的共變異數。而我們可以由相關係數得到彼此的共變異數，方法如下：
$$
\begin{align}
&\rho=\frac{Cov(X_1,X_2)}{\sigma_1 \sigma_2}\\\\
\Rightarrow &Cov(X_1,X_2)=\rho \times\sigma_1\times\sigma_2\\
&=0.5\times1\times1\\
&=0.5
\end{align}
$$
所以共變異數矩陣就會變成：
$$
\begin{bmatrix}
1&0.5\\
0.5&1
\end{bmatrix}
$$
得到了共變異數之後我們就可以開始畫圖。
![[二維常態分配的圖 角度=0.png]]
![[二維常態分配的圖 角度=45.png]]
![[二維常態分配的圖 角度=90.png]]
![[二維常態分配的圖 角度=135.png]]
```R
#一維檢定

Sales <- c(126974,96933,86656,63438,55264,50976,39069,36156,35209,32416)
Profits <- c(4224,3835,3510,3758,3939,1809,2946,359,2480,2413)
Assets <- c(173297,160893,83219,77734,128344,39080,38528,51038,34715,25636)

#sort()拿來從小到大排列資料
data_list_qqplot <- list(Sales = sort(Sales), Profits = sort(Profits), Assets = sort(Assets))

#用迴圈，不想讓程式太長
for(name in names(data_list_qqplot)){
  x <- data_list_qqplot[[name]]
  #建立編號向量從1到樣本數，用seq_along可以防止空的資料導致錯誤
  id <- seq_along(x)
  level <- (id - 0.5) / length(x)
  q <- qnorm(level)
  cat("=== ", name, " ===\n")
  data_f <-data.frame(x, level, round(q,2))
  names(data_f)[1] <- "Ordered observations"
  names(data_f)[2] <- "Probability levels"
  names(data_f)[3] <- "Standard normal quantiles"
  print(data_f)
  #相關係數&檢定
  print(cor.test(x,q,alternative = "two.sided",method="pearson"))
  #畫qq plot
  qqnorm(x, main = paste("QQ Plot for", name))
  qqline(x)
  #常態假設
  print(shapiro.test(x))
}

#二維檢定
library(heplots)

X_2 <-data.frame(Sales,Profits,Assets)
#給迴圈用的，每個變數的組合(1,2),(2,3),(1,3)
# 1=Sales 2=Profits 3=Assets
pair <- combn(1:3, 2, simplify = FALSE)
j <- c(1:nrow(X_2))

for(pair in pairs) {
  cat("兩變數為:", pair, "\n")
  paired_variable <- X_2[, pair]
  d_2 <- sort(Mahalanobis(paired_variable))
  j <- c(1:nrow(X_2))
  q_2 <- qchisq((j - 0.5) / nrow(X_2),2)
  data_f_2 <- data.frame("Ordered Observations" = round(d_2, 2),"Chi-square Quantiles" = round(q_2, 2))
  print(data_f_2)
  cqplot(paired_variable)
  print(cor_res)
}

#加分題
library(mvtnorm)

# 參數
mu <- c(2, 2)
Sigma <- matrix(c(1, 0.5, 0.5, 1), nrow = 2)

#設定網格的密度，數字越大，越多網格（網格越小）
x <- seq(0, 4, length.out = 50)
y <- seq(0, 4, length.out = 50)

# 建立網格
grid <- expand.grid(x = x, y = y)

# 計算密度
z <- matrix(dmvnorm(as.matrix(grid), mean = mu, sigma = Sigma), 
            nrow = length(x), byrow = TRUE)

# 畫圖
for(i in c(0,45,90,135,180,180+45,270,270+45,360)){
persp(x, y, z, 
      theta = i,      # 旋轉角度（水平面上的角度）
      phi = 20,        # 俯視角度
      col = "lightpink", #我喜歡粉紅色
      xlab = "X1", 
      ylab = "X2", 
      zlab = "Density",
      main = paste("二維常態分配的圖，角度=",i))
}
```

