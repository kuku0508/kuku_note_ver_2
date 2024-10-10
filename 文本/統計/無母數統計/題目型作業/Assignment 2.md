# 問題：
![[nonparametric statistic Assignment 2.pdf]]
## 2.14：
Chin et al.(E20) did indirect fluorescent antibody tests on pretreatment sera against falciparum malaria in 57 successfully treated subjects.They found 38 positives.If this samplesatisfies the assumptions of the binomial test, can we conclude from these data that the proportion of positives in the population is greater than 0.50? Let $\alpha=0.05$ 
## 2.21：
In an article on quality control, Purcell(E30) gives the set of typical data shown in Table 2.21. Categorize each observation according to whether it falls above or below 1435, and test the pattern for randomness.

Typical data for life of incandescent lamps in hours, before establishment of control
$$
\begin{array}{|cc|cc|}
\hline
\text{Sample*}&\text{Median}&\text{Sample*}&\text{Median}\\
 \hline
1&1100&17&1210\\
2&1280&18&1620\\
3&1360&19&1560\\
4&1350&20&730\\
5&1060&21&1260\\
6&1250&22&1560\\
7&1440&23&1770\\
8&1230&24&1160\\
9&1630&25&1300\\
10&2100&26&1500\\
11&1210&27&1270\\
12&1760&28&1560\\
13&2410&29&1150\\
14&2080&30&1940\\
15&1500&31&840\\
16&1550&32&1140\\
\hline
\end{array}
$$
 - - -
 # 回答：
## 2.14
題目試問，母體的陽性比例是否大於50%，所以我們這邊可以使用二項檢定（binomial test），而題目又表示這個樣本符合二項檢定的假設，故我們這邊可以使用二項檢定來檢測母體比例是否大於50%。
從上面的題目，我們可以知道他的虛無假設為：
$$
H_0：\rho\leq0.5\quad H_1：\rho>0.5
$$
而在該假設的情況下，p-value為：$P(S\geq s\mid n,\rho_0)$
