---
參考資料:
---
# 問題
在《死亡擱淺》中，你主要扮演一個送貨員。你跟朋友有一天想要比較究竟是誰的送貨穩定度比較高，於是你們各自送了十趟貨，回來測量「包裹完整度」。以下是你們兩個十趟貨物的包裹完整度的資料。
$$
\begin{array}{l|ll}
趟次&你的包裹完整度（\%）&朋友的包裹完整度（\%）\\
\hline
1&93&95\\
2&88&92\\
3&91&94\\
4&90&89\\
5&92&96\\
6&87&90\\
7&95&93\\
8&89&91\\
9&90&92\\
10&94&97
\end{array}
$$
試求，在顯著水準$\alpha=0.05$下，兩位送貨員的穩定程度是否有顯著差異？
# 回答
題目問的是「穩定程度」，所以即使完整度很低，只要是資料越不離散，也就是變異數小，就可以說是穩定程度高。要比較兩個母體的變異數時，我們可以使用[[F檢定 - 雙變異數]]來進行檢定。
此虛無假設為：
$$
H_0\text{：}\sigma_1=\sigma_2\quad vs. \quad H_1\text{：}\sigma_1\neq\sigma_2
$$
而檢定統計量為
$$
F=\frac{S_1^2}{S_2^2}=\frac{6.766667}{6.766667}=1
$$
最後計算P值得出P值為1（畢竟兩個樣本變異數直接一樣了XD）
故我們不拒絕虛無假設，我們沒有足夠的證據證明你跟朋友的送貨穩定程度有顯著差異。