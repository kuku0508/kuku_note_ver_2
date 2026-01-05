---
參考資料:
---
# 問題：
In an experiment on the efffects of three randomly selected operators and five fixed aluminizers on the aluminum thickness of a TV tube, two teadings rare made for each operator-aluminizer combination, The following ANOVA table is compiled.
$$
\begin{array}{lccc}
\hline
\text{Source}&\text{df}&\text{SS}&\text{MS}\\
\hline
\text{Operators}&2&107,540&53,770\\
\text{Aluminizers}&4&139,805&34,951\\
\text{O x A interaction}&8&84,785&10,598\\
\text{Error}&15&230,900&15,393\\
\hline
\text{Totals}&29&563,030\\
\hline
\end{array}
$$
Assuming complete randomization, determine the EMS column for this problem and make indicated significance tests.
# 回答：
因為這裡面有隨機因子，所以我們可以用EMS table來看他們彼此的EMS公式架構，來去決定 誰的MS 要跟 誰的MS 相除得到F。
$$
\begin{array}{ccc}
&i(3,r)&j(5,f)&k(2,r)&EMS\\
\hline
O_i&1&5&2&10\sigma^2_O+\sigma^2\\
A_j&3&0&2&6\phi_A+2\sigma^2_{OA}+\sigma^2\\
OA_{ij}&1&0&2&2\sigma^2_{OA}+\sigma^2\\
\epsilon_{ijk}&1&1&1&\sigma^2
\end{array}
$$
而要決定F值，我們就需要去看EMS的架構，你可以看到，我們要求的就是
$$
\begin{array}{ccc}
要檢定的&EMS架構\\
O&
\end{array}
$$