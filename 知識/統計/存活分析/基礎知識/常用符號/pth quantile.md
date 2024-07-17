pth quantile，就是指[[Survival Time|存活時間]]的[[百分位數]]，以$t_{p}$表示。
- - -
# 備註：
$t_{0.5}=median$
![[median in Survival function.png]]
- - -
# 公式：
$$
\begin{align}
t_p=inf\lbrace t:S(t)\leq 1-p \rbrace\\
\\
inf:最大下界
\end{align}
$$
BTW：{t：條件}，{}表集合，括號裡面是他的元素。
![[0.2th 0.5th example.png]]
上圖我們可以看到，紫線是p=0.2時，在紫線後的面積皆為$S(t_{0.8})$的存活機率。同理可證，綠線的p=0.5，則表在綠線之後的面積為$S(t_{0.5})$的存活機率。
## 連續型：當t為continuous的時候
$$
\begin{align}
&F(t_p)=P(T\leq t)=p\\
&= 1-S(t_p)
\end{align}
$$
![[example F(t)-t圖 in pth quantile.png]]
$$
\begin{align}
\Rightarrow S(t_p)=P(T>t_p)=1-p
\end{align}
$$![[example S(t)-t圖 in pth quantile.png]]

## 離散型：當t是discrete時
我們就需要去估計S(t)
![[discrete example in pth quantile.png]]
我們可以看到我們在估計[[Survival function]]的時候都是看他的斷面是多少的。
詳細請閱Kaplan-Meier估計法。
- - -
parent::[[Survival Time]],[[常用符號目錄]],[[百分位數]],[[Survival Function]]

