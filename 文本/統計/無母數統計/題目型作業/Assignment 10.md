![[NA Assignment 10.pdf]]
# 問題：
## Exercise 8.29
Table 8.40 shows the ages of samples of 10 men and 10 women who are employed by a state government. Can one conclude on the basis of these data that the age compositions of the two populations are different?Use a 0.05 level of significance.

**Table 8.40.  Age of 10 men and 10 women employed by a state government**
$$
\begin{array}{ccc}
\hline
\text{women}&21&37&35&54&31&33&42&27&47&26\\
\text{men}&56&25&43&42&54&33&34&35&47&39
\end{array}
$$
## Exercise 9.33
In an animal-behavior study, 15 domestic animals reared together were ranked according to their relative positions in the group's pecking order and also on the basis of their "friendliness" toward humans. The results are shown in Table 9.44.
1. Compute $r_s$ and determine whether one can conclude that animals higher in the pecking order tend to be friendlier toward humans.
2. compute $\hat{\tau}$ and determine whether the two variables are directly related. Do you reach the same conclusion? Explain.
**Table 9.44 15 domestic animals ranked on pecking order and "friedliness" toward humans**
$$
\begin{array}{ccc}
\hline
\text{Animal}&1&2&3&4&5&6&7&8&9&10&11&12&13&14&15\\
\text{Pecking order}&12&5&11&8&4&6&7&1&14&3&10&15&2&9&13\\
\text{Friendliness}&8&1&9&10&6&5&3&7&11&2&12&13&4&14&15
\end{array}
$$
# 回答：
## Exercise 8.29
表8.40 為受雇於州政府的10位男性與10位女性的年齡數據。根據這些數據，是否可以判斷兩個族群的年齡組成有所不同？使用顯著水準為0.05進行檢定。

**表8.40.  受雇於州政府的10位男性與10位女性之年齡數據**
$$
\begin{array}{ccc}
\hline
\text{女人}&21&37&35&54&31&33&42&27&47&26\\
\text{男人}&56&25&43&42&54&33&34&35&47&39
\end{array}
$$

首先我們判斷一下我們需要進行的處理是什麼。題目問我們說「我們是否可以判斷兩個族群的年齡組成有所不同」，什麼是年齡組成呢？其實就是在不同的年齡，大概有多少比例的元素。其實就是在問我們，受雇於州政府的男性與受雇於州政府的女性，是否來自於相同的機率分配。而當今天我們要檢驗兩組獨立樣本是否來自於同樣的母體分配時，我們就可以使用「Two-sample Kolmpgorov-Smirnov Test」來進行檢驗。
### 基礎假設：
- 此資料由兩組獨立樣本所建構－「受雇於州政府的10位男性年齡數據」以及「受雇於州政府的10位女性年齡數據」
- 受雇於州政府的男性及女性，其年齡的測量尺度為等比尺度（ratio），至少為有序尺度（ordinal）
### 虛無假設＆檢定統計量：
#### 虛無假設：
令
$F_1(x)$為受雇於州政府的男性年齡之機率分配
$F_2(x)$為受雇於州政府的女性年齡之機率分配
$S_1(x)$為受雇於州政府的男性年齡經驗分配函數（empirical distribution functions）
$S_2(x)$為受雇於州政府的女性年齡經驗分配函數（empirical distribution functions）

$$
H_0\text{：}F_1(x)=F_2(x) \quad,\forall\,x\quad versus \quad H_1\text{：}F_1(x)\neq F_2(x)\quad ,\exists \,x 
$$
#### 檢定統計量：
由於我們要進行的假設檢定$H_1\text{：}F_1(x)\neq F_2(x)$，所以我們的檢定統計量會是：
$$
D=max\mid S_1(x)-S_2(x)\mid
$$

## Exercise 9.33
在一樣動物行為研究中，15之一起飼養的家畜根據他們在群體「啄食順序」中的相對位置，以及他們對人類的「友好程度」進行排明。結果於表 9.44顯示。
1. 計算$r_s$值並判斷是否可以得出啄食順序排名較高的動物對人類更友好。
2. 計算$\hat{\tau}$值並判斷「啄食順序」以及「友好程度」是否直接相關。是否可以得出相同的結論，請解釋。

**表9.44 15隻家畜的「啄食順序」及對人類的「友好程度」之排名**
$$
\begin{array}{ccc}
\hline
\text{動物}&1&2&3&4&5&6&7&8&9&10&11&12&13&14&15\\
\text{啄食順序}&12&5&11&8&4&6&7&1&14&3&10&15&2&9&13\\
\text{友好程度}&8&1&9&10&6&5&3&7&11&2&12&13&4&14&15
\end{array}
$$
