今天如果我們要估計截斷的平均時間，要考慮時間會是連續的(Continuous)或是離散的(Discrete time)。
- - -
# 公式：
- **Continuous time：**
$$
\hat{E}(T)=\int^{y_n}_0\hat{S}(t)dt\,,\,where\,\,y_n=max\,(y_i)
$$
- **Discrete time：**
$$
\hat{E}(T)=\sum^k_{j=1}(t_j-t_{j-1})\hat{S}(t_{j-1})
$$
- - -
parent::[[Survival Time]],[[截斷]]