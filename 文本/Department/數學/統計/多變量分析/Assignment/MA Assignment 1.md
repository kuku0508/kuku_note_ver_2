二維常態分配的圖 角度=二維常態分配的圖 角度=
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