# 問題：
![[Regression analysis Assignment 1.pdf]]
# 回答：
## (a) Show that $\hat{\beta}_0$ is a linear combination of $y_i$
由題目可以知道
$$
\hat{\beta}_0=\bar{y}-\hat{\beta}_1\bar{x}
$$
而我們把題目給的$\hat{\beta}_1=\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}$代入至上式中，可以得到：
$$
\begin{align}
\hat{\beta}_0&=\bar{y}-\hat{\beta}_1\bar{x}\\
&=\bar{y}-\left(\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}\right)\bar{x}\\
&=\frac{\sum y_i}{n}-\left(\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}\right)\bar{x}
\end{align}
$$
我們可以看到，$\hat{\beta}_0$中的兩個項，裡面都有$y_i$。在$\frac{\sum y_i}{n}$中，$y_i$的係數為$\frac1n$；而在$\left(\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}\right)\bar{x}$中，$y_i$的係數為$\left(\frac{\sum(x_i-\bar{x})}{\sum(x_i-\bar{x})^2}\right)\bar{x}$。因此我們可以說$\hat{\beta}_0$可以表示成一個包含所有$y_i$的線性加權和，因此我們可以說$\hat{\beta}_0$是$y_i$的線性組合。
## (b) Show that $E(\hat{\beta}_1)=\beta_1$
$$
\begin{align}
E(\hat{\beta}_1)&=E\left[\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}\right]\\
&=\frac{1}{\sum(x_i-\bar{x})^2}E\left[\sum(x_i-\bar{x})y_i\right]\\
&=\frac{1}{\sum(x_i-\bar{x})^2}E\left[\sum(x_i-\bar{x})(\beta_0+\beta_1x_i)\right]\\
&=\frac{1}{\sum(x_i-\bar{x})^2}E\left[\cancel{\sum(x_i-\bar{x})\beta_0}^{\,\,0}+\sum(x_i-\bar{x})\beta_1x_i\right]\\
&=\frac{1}{\sum(x_i-\bar{x})^2}\left[\sum(x_i-\bar{x})\beta_1x_i)\right]\\
&=\frac{1}{\sum(x_i-\bar{x})^2}\left[\beta_1\sum(x_i-\bar{x})x_i)\right]\\
&=\frac{1}{\cancel{\sum(x_i-\bar{x})^2}}\left[\beta_1\cancel{\sum(x_i-\bar{x})(x_i-\bar{x})}\right]\\\\
&=\beta_1
\end{align}
$$
## (c) Show that $E(\hat{\beta}_0)=\beta_0$
$$
\begin{align}
E(\hat{\beta}_0)&=E(\bar{y}-\hat{\beta}_1\bar{x})\\
&=E(\bar{y})-E(\beta_1\bar{x})\\
&=E(\frac{1}{n}\sum y_i)-E(\beta_1\bar{x})\\
&=E(\frac{\cancel n\beta_0+\beta_1\cancel{\sum(x_i)}^{\bar{x}}+\cancel{\bar{\epsilon}}}{\cancel{n}})-E(\beta_1\bar{x})\\
&=\beta_0+\beta_1\bar{x}-\beta_1\bar{x}\\
&=\beta_0
\end{align}
$$
## (d) Show that $Cov(\bar{y},\hat{\beta}_1)=0$
$$
\begin{align}
Cov(\bar{y},\hat{\beta}_1)&=E\left[(\bar{y}-\bar{\bar{y}})(\hat{\beta}_1-\bar{\hat{\beta}_1})\right]\\&=E\left\lbrace\left[\bar{y}-E(\bar{y})\right]\left[\hat{\beta}_1-E(\hat{\beta}_1)\right]\right\rbrace\\
&=E\left\lbrace\cancel{(\bar{y}-\bar{y})}^{\,0}\left[\hat{\beta}_1-E(\hat{\beta}_1)\right]\right\rbrace\\\\
&=0
\end{align}
$$
## (e) Show that $Var(\hat{\beta}_1)=\frac{\sigma^2}{\sum(x_i-\bar{x})^2}$
我們可以先整理$\hat{\beta}_1$，好讓我們後續比較好處理。
$$
\begin{align}
\hat{\beta}_1=\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}&=\frac{\sum(x_i-\bar{x})(\beta_0+\beta_1x_i+\epsilon_i)}{\sum(x_i-\bar{x})^2}\\
&=\frac{\cancel{\sum(x_i-\bar{x})\beta_0}^{\,0}+\sum(x_i-\bar{x})\beta_1x_i+\sum(x_i-\bar{x})\epsilon_i}{\sum(x_i-\bar{x})^2}\\
&=\beta_1+\frac{\sum(x_i-\bar{x})\epsilon_i}{\sum(x_i-\bar{x})^2}
\end{align}
$$
整理好了，接下來開始論證。
$$
\begin{align}
Var(\hat{\beta}_1)&=Var\left(\beta_1+\frac{\sum(x_i-\bar{x})\epsilon_i}{\sum(x_i-\bar{x})^2}\right)\\
&=Var\left(\frac{\sum(x_i-\bar{x})\epsilon_i}{\left[\sum(x_i-\bar{x})^2\right]^2}\right)\\\\
&=\frac{1}{\left[\sum(x_i-\bar{x})^2\right]^2}Var\left(\sum(x_i-\bar{x})\epsilon_i\right)\\
&=\frac{1}{\left[\sum(x_i-\bar{x})^2\right]^\cancel{2}}\times\cancel{\left[\sum(x_i-\bar{x})\right]^2}\times Var(\epsilon)\\
&=\frac{Var(\epsilon)}{\sum(x_i-\bar{x})^2}\\
&=\frac{\sigma^2}{\sum(x_i-\bar{x})^2}
\end{align}
$$
## (f) Show that $Var(\hat{\beta}_0)=\sigma^2\left[\frac1n + \frac{\bar{x}^2}{\sum (x_i-\bar{x})^2}\right]$
$$
\begin{align}
Var(\hat{\beta}_0)&=Var(\bar{y}-\hat{\beta}_1\bar{x})\\
&=Var(\bar{y})+\bar{x}^2Var(\hat{\beta}_1)-2\bar{x}Cov(\bar{y},\hat{\beta}_1)\\
\end{align}
$$
因為前面已經推導了$Cov(\bar{y},\hat{\beta}_1)=0$還有$Var(\hat{\beta}_1)=\frac{\sigma^2}{\sum(x_i-\bar{x})^2}$，最後再計算$Var(\bar{y})$即可直接帶入上式：
$$
\begin{align}
Var(\bar{y})&=Var(\frac1n\sum y_i)\\
&=\frac{1}{n^2}Var(\sum y_i)\\
&=\frac{1}{n^2}\sum Var(y_i)\\
&=\frac{1}{n^2}\sum \sigma^2\\
&=\frac{1}{n^2}\times n \times \sigma^2\\
&=\frac{\sigma^2}{n}
\end{align}$$
算完了，直接帶入吧：
$$
\begin{align}
Var(\hat{\beta}_0)&=Var(\bar{y})-\bar{x}^2Var(\hat{\beta}_1)-2\bar{x}Cov(\bar{y},\hat{\beta}_1)\\
&=\frac{\sigma^2}{n}-\bar{x}^2\left[\frac{\sigma^2}{\sum(x_i-\bar{x})^2}\right])-2\bar{x}\times0\\
&=\sigma^2\left[\frac1n+\frac{}{}\right]
\end{align}
$$
