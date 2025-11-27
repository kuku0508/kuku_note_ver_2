---
參考資料:
  - "[[chapter 3 Single-Factor Experiments with No Restrictions on Randomization]]"
tags:
  - 實驗設計
  - ANOVA
---
# 母體
在母體中，完全隨機設計可以表示為：
$$
Y_{ij}=\mu+\tau_j+\epsilon_{ij}
$$
進而可以改寫為：
$$
\begin{align}
&Y_{ij}=\mu+(\mu_j-\mu)+(Y_{ij}-\mu_j)\\\\
&\Rightarrow Y_{ij}-\mu=(\mu_j-\mu)+(Y_{ij}-\mu_j)
\end{align}
$$
- - -
# 樣本
而在樣本中，可以表示為：
$$
Y_{ij}-\bar{Y}_{..}=(\bar{Y}_{.j}-\bar{Y}_{..})+(Y_{ij}-\bar{Y}_{.j})
$$
$$
\begin{align}
&\text{where}\\
&T=\sum^k_{j=1}\sum^{n_j}_{i=1}Y_{ij}=\sum^k_{j=1}T_{.j}\quad,\\
&N=\sum^k_{j=1}n_j\,\,,\,\bar{Y}_{.j}=T_{.j}/n_j\,\,and\,\,\bar{Y}_{..}=\sum^k_{j=1}n_j\bar{Y}_{.j}/N\\\\
&\sum\sum(Y_{ij}-\bar{Y}_{..})^2=\sum\sum (\bar{Y}_{.j}-\bar{Y}_{..})^2+\sum\sum(Y_{ij}-\bar{Y}_{.j})^2
\end{align}
$$

若處理效果$\tau_j=0 \quad\forall\,j$則：
$$
\begin{align}
&\sum\sum(Y_{ij}-\bar{Y}_{..})^2/(N-1)\underrightarrow{\quad\quad  U.E\quad \quad }\sigma^2_{\epsilon}\\
&\sum\sum(\bar{Y}_{.j}-\bar{Y}_{..})^2/(k-1)\underrightarrow{\quad\quad  U.E\quad \quad }\sigma^2_{\epsilon}\\
&\left(\sum\sum(Y_{.j}-\bar{Y}_{..})^2/(k-1)\underrightarrow{\quad\quad  U.E\quad \quad }\sigma^2_{\bar{Y_{.j}}}\,,\,\sigma^2_{\epsilon}=n_j\bar{Y_{.j}}\right)\\
&\sum\sum(Y_{ij}-\bar{Y}_{.j})^2/(N-k)\underrightarrow{\quad\quad  U.E\quad \quad }\sigma^2_{\epsilon}
\end{align}
$$
上面指的是，$Y_{ij}-\bar{Y}_{..}$（SST）、$(\bar{Y}_{.j}-\bar{Y}_{..})$（SSTR）、$(Y_{ij}-\bar{Y}_{.j})$（SSE）除以各自的自由度變成MST、MSTR、MSE之後會為變異數的無偏估計量。
- - -
parent::
sibling::
child::