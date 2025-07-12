---
參考資料:
  - Statistics the exploration and analysis of data,7e; Roxy peck, Jay L. Devore.
---
雙樣本Z檢定（two-sample Z-test），是一種[[假設檢定]]，可以用於檢測==兩[[獨立事件|獨立]]母體==的母體[[比例]]差是否為給定的值。
- - -
# 前提
- $n_1\hat{p_1}\geq10$，$n_1(1-\hat{p_1})\geq 10$；$n_2\hat{p_2}\geq10$，$n_2(1-\hat{p_2})\geq 10$
- 樣本抽樣相互獨立且來自同分配（[[獨立同分配|iid]]）
- - -
# 虛無假設&對立假設
### [[左尾檢定]]
$$
H_0\text{：}p_1-p_2\geq d_0\quad vs.\quad H_1\text{：}p_1-p_2<d_0
$$
### [[右尾檢定]]
$$
H_0\text{：}p_1-p_2\leq d_0\quad vs.\quad H_1\text{：}p_1-p_2>d_0
$$
### [[雙尾檢定]]
$$
H_0\text{：}p_1-p_2= d_0\quad vs.\quad H_1\text{：}p_1-p_2\neq d_0
$$
$p_1$：母體1比例
$p_2$：母體2比例
$d_0$：給定值
- - -
# 檢定統計量
$$
Z=\frac{(\bar{p_1}-\bar{p_2})-(p_1-p_2)}{\sqrt{\frac{1}{n_1}+\frac{1}{n_2}}}
$$
$Z$：Z值（檢定統計量）
$\bar{x_1}$：抽樣自母體1的樣本平均數
$\bar{x_2}$：抽樣自母體2的樣本平均數
$\mu_1$：母體1的母體平均數給定值
$\mu_2$：母體2的母體平均數給定值
$\sigma_1^2$：母體1的母體變異數
$\sigma_2^2$：母體2的母體變異數
$n_1$：抽樣自母體1的樣本數
$n_2$：抽樣自母體2的樣本數
- - -
# P值
在虛無假設為真的前提下，檢定統計量會服從[[Z分配]]：
$$
P=
\begin{cases}
2P(Z>|z|),&\text{when }H_1\text{：}\mu_1-\mu_2\neq d_0\\\\
P(Z>z),&\text{when }H_1\text{：}\mu_1-\mu_2> d_0\\\\
P(Z<z),&\text{when }H_1\text{：}\mu_1-\mu_2< d_0
\end{cases}
$$
- - -
parent::[[假設檢定]],[[比例]],[[左尾檢定]],[[右尾檢定]],[[雙尾檢定]],[[Z分配]],[[獨立事件]]
sibling::
child::