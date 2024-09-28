# 問題：
![[Regression analysis Assignment 1.pdf]]
# 回答：
## (a) Show that $\hat{\beta}_0$ is a linear combination of $y_i$
由題目可以知道
$$
\hat{\beta}_0=\bar{y}-\hat{\beta}_1\bar{x}
$$
而我們把題目給的$\hat{\beta}_1=\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2}$代入至上式中，可以得到：
$$\begin{align}
\hat{\beta}_0=\bar{y}-\hat{\beta}_1\bar{x}&\\
&\bar{y}-(\frac{\sum(x_i-\bar{x})y_i}{\sum(x_i-\bar{x})^2})\bar{x}
\end{align}$$
## (b) Show that $E(\hat{\beta}_1)=\beta_1$
## (c) Show that $E(\hat{\beta}_0)=\beta_0$
## (d) Show that $Cov(\bar{y},\hat{\beta}_1)=0$
## (e) Show that $Var(\hat{\beta}_1)=\frac{\alpha^2}{\sum(x_i-\bar{x})^2}$
## (f) Show that $Var(\hat{\beta}_0)=\sigma^2\left[\frac1n + \frac{\bar{x}^2}{\sum (x_i-\bar{x})^2}\right]$
