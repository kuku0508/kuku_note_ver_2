---
參考資料:
---
# 問題：
Consider a three-factor experiment where factor A is at a levels, factor B at b levels, and factor C at c levels. The experimemt is to run in a completely randomized manner with n observations for each treatment combination. Assuming that factor A is run at a random levels and both B and C at fixed levels, determine the EMS column and indicate what tests would be made after the analysis.
# 回答：
$$
\begin{array}{cccc}
&A(r,a)&B(f,b)&C(f,c)&EMS\\
\hline
A_a&1&b&c&bc\,\sigma^2_A+c\,\sigma^2_{AB}+b\,\sigma^2_{AC}+\sigma^2_\epsilon\\
B_b&a&0&c&\\
AB_{ab}&1&0&c\\
C_c&a&b&0\\
AC_{ac}&1&b&0\\
BC_{bc}&a&0&0\\
ABC_{abc}&1&0&0\\
error&1&1&1
\end{array}
$$