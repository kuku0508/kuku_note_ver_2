mean residual life(平均餘命)，又被稱為Expected Remaining Lifetime。是指在時間點t之後，個體沒有發生事件的條件下，剩餘存活期間的期望值。
- - -
# 公式：
$$
\begin{align}
mrl(t)
=&E\left[T-t\mid T>t \right]\\
=&\frac{\int^\infty_tS(u)du}{S(t)}
\end{align}
$$
- - -
# 應用：
- 用於預測病人在治療後的預期存活時間
- 用於預測機器或設備在運行一段時間後的預期剩餘壽命
- - -
![[mean residual life 圖例.png]]
- - -
parent::[[Survival Time]],[[Survival Function]],[[常用符號目錄]],[[平均數]]
child::[[mrl(t)的估計]]