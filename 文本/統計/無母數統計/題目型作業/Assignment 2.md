![[nonparametric statistic Assignment 2.pdf]]
# 問題：
## 2.14：
Chin et al.(E20) did indirect fluorescent antibody tests on pretreatment sera against falciparum malaria in 57 successfully treated subjects.They found 38 positives.If this sample  satisfies the assumptions of the binomial test, can we conclude from these data that the proportion of positives in the population is greater than 0.50? Let $\alpha=0.05$ 
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

\*Each sample contains five lamps

 - - -
# 回答：
## 2.14
在本次的實驗中，對於57名惡性瘧疾的成功治療的病患，進行了間接螢光抗體測試，其中有38名病患結果為陽性。題目試問，母體的陽性比例是否大於50%？

我們可以使用二項檢定（binomial test）來檢定母體的比例。以下逐步進行：
- - -
## 基本假設：
- 此樣本由57次相互獨立的伯努利試驗建立，其中成功事件次數為38次。而題目也提到此樣本滿足二項檢定的基本假設。
- - -
### 假設檢定：
令$\rho$為成功治療惡性瘧疾之患者，產生抗體的比例
$$
H_0：\rho\leq0.5\quad H_1：\rho>0.5
$$
而在該假設的情況下，p-value為：$P(S\geq s\mid n,\rho_0)$
然後由題目可以知道，$n=57$、$s=38$，$\rho_0=0.5$。

$$
\begin{align}
P(S\geq38\mid 57,0.5)&=\left(C^{57}_{38}+ C^{57}_{39}+ C^{57}_{40}\ldots + C^{57}_{57}\right)\times0.5^{57}\\
&\approx0.0082
\end{align}
$$
我們可以看到最後的p-value等於0.0082，遠小於顯著水準$\alpha$的0.05，故我們可以說，我們有強烈的證據去拒絕虛無假設，並說明在在感染瘧疾後成功康復的患者，有超過50%的人產生了抗體。

我們透過SAS來進一步驗證，程式碼如下：
data non_parametric_assignment_2;
input result $ count;
cards;
Positive 38
Negative 19
;
PROC FREQ order=data;
WEIGHT count;
TABLE result/BINOMIAL(P=0.5);
EXACT BINOMIAL;
RUN;

![[Assignment 2 2.14 SAS.png]]
我們可以看到在Exact test的單邊P-value的值跟我們試算的結果一樣是0.0082。

# 2.21：
題目這邊直接問下面的資料集呈現的資料，建立兩個分類，分別是大於及小於1435，並檢視該模式是否呈現隨機性。我們可以使用One-sample runs test來檢定其是否具有隨機性。
- - -
## 基本假設：
- 本樣本由控制前白熾燈的壽命（以小時為單位）組成，且將其分為了大於1435以及小於1435這種類型的資料。
- - - 
於是我們先將其原始資料減去1435，並進行One-sample runs test：
$$H_0\text{: Data are randomly distributed.}\quad\text{v.s.}\quad
H_1\text{: Data are not randomly distributed.}
$$
$$
\begin{array}{|ccr|ccr|}
\hline
\text{Sample*}&\text{Median}&\text{Reduced}&\text{Sample*}&\text{Median}&\text{Reduced}\\
 \hline
1&1100&-335&17&1210&-225\\
2&1280&-155&18&1620&185\\
3&1360&-75&19&1560&125\\
4&1350&-85&20&730&-705\\
5&1060&-375&21&1260&-175\\
6&1250&-185&22&1560&125\\
7&1440&5&23&1770&335\\
8&1230&-205&24&1160&-275\\
9&1630&195&25&1300&-135\\
10&2100&665&26&1500&65\\
11&1210&-225&27&1270&-165\\
12&1760&325&28&1560&125\\
13&2410&975&29&1150&-285\\
14&2080&645&30&1940&505\\
15&1500&65&31&840&-595\\
16&1550&115&32&1140&-295\\
\hline
\end{array}
$$
現在我們跟ㄐ
然後我們來算一下這邊有幾個runs，
1. \[1-6\]
2. \[7\]
3. \[8\]
4. \[9-10\]
5. \[11\]
6. \[12-16\]
7. \[17\]
8. \[18-19\]
9. \[20-21\]
10. \[22-23\]
11. \[24-25\]
12. \[26\]
13. \[27\]
14. \[28\]
15. \[29\]
16. \[30\]
17. \[31-32\]
我們有17個runs，$n_1=15$(正數數量)，$n_2=17$(負數數量)。
我們根據上面的值查表：
![[Runs test Lower and Upper Table.png]]
在$n_1=15$、$n_2=17$的情況下，我們可以知道只要$11<\text{runs的數量}<23$，我們就不拒絕虛無假設，反之則拒絕。
而我們剛剛得出，我們有17個runs，故我們這邊不拒絕虛無假設。我們沒有足夠強烈的證據去證明，這些樣本的白熾燈的燈泡壽命之中位數，呈現顯著的非隨機性模式。

我們這邊用程式碼再驗證一下，程式碼如下：
``` R
install.packages("randtests")
library(randtests)

# 原始資料(key的好累)
raw_data=c(1100,1280,1360,1350,1060,1250,1440,1230,1630,2100,1210,1760,2410,2080,1500,1550,1210,1620,1560,730,1260,1560,1770,1160,1300,1500,1270,1560,1150,1940,840,1140)

# 將原始資料減1435
reduced_data=c(raw_data-1435)

runs.test(reduced_data,threshold = 0)
```

![[Assignment 2 runs test output.png]]
我們可以看到p-value為0.982，故我們沒有足夠強烈的證據去證明，這些樣本的白熾燈的壽命之中位數，呈現顯著的非隨機性模式。