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
我們可以看到，$\hat{\beta}_0$中的兩個項，裡面都有$y_i$。在$\frac{\sum y_i}{n}$中，$y_i$的係數為$\frac1n$；-6
## (b) Show that $E(\hat{\beta}_1)=\beta_1$
## (c) Show that $E(\hat{\beta}_0)=\beta_0$
## (d) Show that $Cov(\bar{y},\hat{\beta}_1)=0$
## (e) Show that $Var(\hat{\beta}_1)=\frac{\alpha^2}{\sum(x_i-\bar{x})^2}$
## (f) Show that $Var(\hat{\beta}_0)=\sigma^2\left[\frac1n + \frac{\bar{x}^2}{\sum (x_i-\bar{x})^2}\right]$
