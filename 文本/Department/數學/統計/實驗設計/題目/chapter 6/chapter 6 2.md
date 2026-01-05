---
參考資料:
---
# 問題：
Consider a three-factor experiment where factor A is at a levels, factor B at b levels, and factor C at c levels. The experimemt is to run in a completely randomized manner with n observations for each treatment combination. Assuming that factor A is run at a random levels and both B and C at fixed levels, determine the EMS column and indicate what tests would be made after the analysis.
# 回答：
$$
\begin{array}{cccc}
&A(r,a)&B(f,b)&C(f,c)&l(r,n)&EMS\\
\hline
A_a&1&b&c&n&bcn\,\sigma^2_A+\sigma^2_\epsilon\\
B_b&a&0&c&n&acn\,\phi^2_B+cn\,\sigma^2_{AB}+\sigma^2_\epsilon\\
AB_{ab}&1&0&c&n&cn\,\sigma^2_{AB}+\sigma^2_\epsilon\\
C_c&a&b&0&n&abn\,\phi^2_{C}+bn\,\sigma^2_{AC}+\sigma^2_\epsilon\\
AC_{ac}&1&b&0&n&bn\,\sigma^2_{AC}+\sigma^2_\epsilon\\
BC_{bc}&a&0&0&n&an\,\phi_{bc}+n\,\sigma^2_{ABC}+\sigma^2_\epsilon\\
ABC_{abc}&1&0&0&n&n\,\sigma^2_{ABC}+\sigma^2_\epsilon\\
error&1&1&1&1&\sigma^2_\epsilon
\end{array}
$$
3
4
2
5

2
3
1
