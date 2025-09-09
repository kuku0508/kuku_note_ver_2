---
參考資料:
  - Survey Sampling, International Edition; Richard L. Scheaffer, William Mendenhall. III
tags:
---
尼曼分配（Neyman allocation）

- - -
當我們今天在每一層的成本的一樣的情況下，要將[[分層抽樣 - 樣本數（平均數）|樣本平均數]]跟[[分層抽樣 - 樣本數（總和）|總和]]估計的變異程度最小化，我們可以透過Neyman allocation來得到最適的[[配置率]]：
$$
n_i=n\cdot\frac{N_i\sigma_i}{\sum^L_{k=1}N_k\sigma_k}
$$
$$
n=\frac{\left(\sum^L_{i=1}N_i\sigma_i\right)^2}{N^2D+\sum^L_{i=1}N_i\sigma^2_i}
$$
$n$：總樣本數
$N_i$：第i層中的抽樣單位數
$\sigma^2$：第i層中的母體變異數

如果要估計平均數的話，$D=\frac{B^2}{4}$；估計總和的話，$D=\frac{B^2}{4N^2}$。
- - -
parent::[[配置率]],[[分層抽樣 - 樣本數（總和）]],[[分層抽樣 - 樣本數（平均數）]]
