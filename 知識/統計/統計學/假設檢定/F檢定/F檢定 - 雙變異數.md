---
參考資料:
---
F檢定（F-test），是一種[[假設檢定]]，可以來檢定兩母體的母體[[變異數]]之間的關係。
- - -
# 前提
- 母體分配為[[單變量常態分配|常態/近似常態]]
- 樣本抽樣相互獨立且來自同分配（[[獨立同分配|iid]]）
- 樣本數據為[[連續型隨機變數]]
- - -
# 虛無假設＆對立假設
### [[左尾檢定]]
$$
H_0\text{：}\sigma^2_1\geq \sigma^2_2\quad vs.\quad H_1\text{：}\sigma^2_1< \sigma^2_2
$$
### [[右尾檢定]]
$$
H_0\text{：}\sigma^2_1\leq \sigma^2_2\quad vs.\quad H_1\text{：}\sigma^2_1>\sigma^2_2
$$
### [[雙尾檢定]]
$$
H_0\text{：}\sigma^2_1=\sigma^2_2\quad vs.\quad H_1\text{：}\sigma^2_1\neq \sigma^2_2
$$
$\sigma^2_1$：來自母體1的母體變異數
$\sigma^2_2$：來自母體2的母體變異數
- - -
# 檢定統計量
$$
F=\frac{S^2_1}{S^2_2}
$$
$F$：F值（檢定統計量）
$S^2_1$：抽樣自母體1的樣本變異數
$S^2_2$：抽樣自母體2的樣本變異數
- - -
# P值
在虛無假設為真的前提下，檢定統計量會服從[[F分配]]：
$$
P=
\begin{cases}
2\cdot min(P(F\geq F_{obs}),P(F\leq F_{obs})) &\text{when }H_1\text{：}\sigma^2_1\neq \sigma^2_2\\\\

P(F\geq F_{obs}),&\text{when }H_1\text{：}\sigma^2_1> \sigma^2_2\\\\

P(F\leq F_{obs}),&\text{when }H_1\text{：}\sigma^2_1< \sigma^2_2
\end{cases}
$$
- - -
# 範例
- [[F檢定範例 - 精準抓量]]
- - -
parent::[[假設檢定]],[[單變量常態分配]],[[連續型隨機變數]],[[右尾檢定]],[[左尾檢定]],[[雙尾檢定]],[[F分配]]
sibling::
child::