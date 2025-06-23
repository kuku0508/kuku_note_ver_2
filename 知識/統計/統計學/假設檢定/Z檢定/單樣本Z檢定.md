---
參考資料:
---
單樣本Z檢定（one-sample Z-test），是一種[[假設檢定]]，專門用於檢測一母體的母體[[平均數]]是否為給定的值。
- - -
# 前提
- 母體分配近似[[單變量常態分配|常態分配]]，或樣本數$n\geq 30$
- ==母體標準差$\sigma$已知==
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
在虛無假設為真的前提下，檢定統計量Z$\sim N(0,1)$：
$$
P=
\begin{cases}
2P(Z>|z|),&\text{when }H_1\text{：}\mu\neq \mu_0\\\\
P(Z>z),&\text{when }H_1\text{：}\mu> \mu_0\\\\
P(Z<z),&\text{when }H_1\text{：}\mu< \mu_0
\end{cases}
$$
- - -
parent::[[假設檢定]],[[平均數]],[[左尾檢定]],[[右尾檢定]],[[雙尾檢定]]
sibling::
child::