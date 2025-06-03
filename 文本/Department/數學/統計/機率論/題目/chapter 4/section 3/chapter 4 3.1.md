# 問題：
Let $X$ and $Y$ be the r.v's denoting the number of sixes when two fair dice are rolled independently 15 times each.Determine the $E(X+Y)$.
# 回答：
我們有X跟Y兩個變數
X：第一顆骰子骰到「6」的次數
Y：第二顆骰子骰到「6」的次數
我們可以很簡單發現，X跟Y理應會服從[[二項分配]]
因為你只有骰到6跟沒有骰到6兩個可能。
所以我們可以寫成
$$
X,Y \sim B(15,\frac{1}{6})
$$
而二項分配的期望值是$np$，所以我們可以知道
$$
E(X)=E(Y)=15\ㄔㄟ
$$