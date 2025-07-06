---
參考資料:
  - Statistics the exploration and analysis of data,7e; Roxy peck, Jay L. Devore.
---
單樣本Z檢定（one-sample Z-test），是一種[[假設檢定]]，可以用於檢測一母體的母體[[比例]]是否為給定的值。
- - -
# 前提
- 母體分配近似[[單變量常態分配|常態分配]]，或樣本數$n\geq 30$
- 樣本抽樣相互獨立且來自同分配（[[獨立同分配|iid]]）
- $np_0\geq 10$且$n(1-p_0)$
- 如果抽樣採不放回抽樣，樣本量不應大於母體規模的10%
- - -
# 虛無假設&對立假設
### [[左尾檢定]]
$$
H_0\text{：}\mu\geq \mu_0\quad vs.\quad H_1\text{：}\mu<\mu_0
$$
### [[右尾檢定]]
$$
H_0\text{：}\mu\leq \mu_0\quad vs.\quad H_1\text{：}\mu>\mu_0
$$
### [[雙尾檢定]]
$$
H_0\text{：}\mu= \mu_0\quad vs.\quad H_1\text{：}\mu\neq\mu_0
$$
$\mu$：母體平均數
$\mu_0$：給定值
- - -
# 檢定統計量
$$
Z=\frac{\bar{X}-\mu_0}{\sigma/\sqrt{n}}
$$
$Z$：Z值（檢定統計量）
$\bar{X}$：樣本平均數
$\mu_0$：給定值
$\sigma$：母體標準差
$n$：樣本數
- - -
# P值
在虛無假設為真的前提下，檢定統計量會服從[[Z分配]]：
$$
P=
\begin{cases}
2P(Z>|z|),&\text{when }H_1\text{：}\mu\neq \mu_0\\\\
P(Z>z),&\text{when }H_1\text{：}\mu> \mu_0\\\\
P(Z<z),&\text{when }H_1\text{：}\mu< \mu_0
\end{cases}
$$
- - -
# 範例
- [[Z檢定範例 - 客服等待時間]]
- - -
parent::[[假設檢定]],[[平均數]],[[左尾檢定]],[[右尾檢定]],[[雙尾檢定]],[[Z分配]]
sibling::
child::
- - -
parent::
sibling::
child::