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
T=\sum^k_{j=1}\sum^{n_j}_{i=1}Y_{ij}=\sum^k_{j=1}T_{.j}
\end{align}
$$

- - -
parent::
sibling::
child::