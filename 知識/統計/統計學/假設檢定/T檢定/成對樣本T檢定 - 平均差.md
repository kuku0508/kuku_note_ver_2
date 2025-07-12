---
參考資料:
---
成對T檢定（paired-sample T-test），是一種[[假設檢定]]，用來檢定成對樣本的平均差是否為給定值。

例如：吃完血壓藥之前後的舒張壓數值之差、在用藥之後的握力差等。
- - -
# 前提
- ==樣本為配對。==
- 樣本差異的母體分配為常態/近似常態，或樣本數大於30。
- 樣本抽樣相互獨立且來自同分配（[[獨立同分配|iid]]）。
- - -
# 虛無假設＆對立假設
假設$X$與$Y$分別為兩個常態母體的特性，且X與Y不獨立。而$X_d=X_i-Y_i$。
### [[左尾檢定]]
$$
H_0\text{：}\bar{d}\geq d_0\quad vs.\quad H_1\text{：}\bar{d}<d_0
$$
### [[右尾檢定]]
$$
H_0\text{：}\bar{d}\leq d_0\quad vs.\quad H_1\text{：}\bar{d}>d_0
$$
### [[雙尾檢定]]
$$
H_0\text{：}\bar{d}= d_0\quad vs.\quad H_1\text{：}\bar{d}\neq d_0
$$
$\bar{d}$：$X_d$的平均數
$d_0$：給定值
- - -
# 檢定統計量
$$
T=\frac{\bar{d}-d_0}{\frac{S_d}{\sqrt{n}}}\sim T(n-1)
$$
$T$：T值（檢定統計量）
$\bar{d}$：樣本差異的平均數
$d_0$：給定值
$S_d$：樣本差異的標準差
$n$：樣本差異的個數
- - -
# P值
在虛無假設為真的前提下，檢定統計量會服從[[T分配]]：
$$
P=
\begin{cases}
2P(T>|t|),&\text{when }H_1\text{：}\bar{d}\neq d_0\\\\
P(T>t),&\text{when }H_1\text{：}\bar{d}> d_0\\\\
P(T<t),&\text{when }H_1\text{：}\bar{d}< d_0
\end{cases}
$$
- - -
# 範例
[[成對T檢定範例 - ]]
- - -
parent::[[假設檢定]],[[平均數]],[[左尾檢定]],[[右尾檢定]],[[雙尾檢定]]
sibling::
child::