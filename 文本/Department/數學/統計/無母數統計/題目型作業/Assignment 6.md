![[Pasted image 20241119233316.png]]
# 問題：
![[NA Assignment 6.pdf]]

## Exercise 6.20
A test designed to measure a person's level of mental health was administered to three groups of subjects. The results are shown in Table 6.28. can one conclude from these data that the status of mental health is different among these three groups? Use the extension of the median test.

**Score made on a level of mental health test by three groups of subjects**
$$
\begin{array}{lc}
\hline
\text{Unwed}&30&40&70&75&15&20&20&32&80&25&25&25\\
\text{pregnant}&75&30&90&30&60&85&100&90&75&70&90&15\\
\text{girls}&15\\
\\
\text{Married}&15&17&25&30&35&45&50&50&55&60&60&60\\
\text{pregnant}&100&95&80&75&70&65&60&80&30&30&25&50\\
\text{woman}&60&65&65&65&70&70&75&75&90&35&75&30\\
 &25&45&65&60&20&75&100&80&90&90\\
\\
\text{Unmarried}&20&15&60&45&15&35&55&20&70&65&30&100\\
\text{girl, not}&90&85&10&55&25&90&80&75&25&30&65&80\\
\text{pregnant}&55&100&15&100&50&90&30&40&15&40&50&65\\
 &70
\end{array}
$$
# 回答：
## Exercise 6.20（Extension of median test）
為了測量一個人的心理健康狀況，對三組受試者進行了測試，其結果如表 6.28 所示。根據這些資料，是否可以得出結論，這三組之間的心理健康狀況存在差異？請使用extension of median test 進行檢驗。

## 基本假設
- 心理狀況的評分是來自於三組獨立隨機樣本，分別是「未婚已懷孕的女性」、「已婚已懷孕的女性」、「未婚未懷孕的女性」，樣本數分別為25、46、37，母體中位數$M_1$、$M_2$、$M_3$未知。
- 心理狀況的評分至少是有序尺度的。
- 如果每一組的母體中位數皆相同，則觀察值大於或等於母體中位數的機率在每一組中應該也要是相同的。
## 虛無假設
令
$M_1$為未婚已懷孕的女性心理健康分數之中位數
$M_2$為已婚已懷孕的女性心理健康分數之中位數
$M_3$為未婚未懷孕的女性心理健康分數之中位數
$$
H_0\text{：}M_1=M_2=M_3\quad\text{versus}\quad H_1\text{： }至少有一個M_i\neq M_j \quad i=1,2,3\quad j=1,2,3
$$
## 檢定統計量
合併所有數據，並將他們排序，得到一個樣本中位數M。

建構一個2 x k的列聯表，依照原始資料進行分組，分為「未婚已懷孕的女性」、「已婚已懷孕的女性」、「未婚未懷孕的女性」，且將每一組的樣本以樣本中位數M為界線，分為大於樣本中位數M以及小於樣本中位數M。

計算這個列聯表的==卡方統計量$X^2$==。
- - -
將所有數據合併之後，得到的中位數為第54.5筆，也就是第54筆以及第55筆的平均。
第54筆及第55筆皆為60，故我們得出樣本中位數等於60。

接下來以60為界線，將各個組別劃分，建構出以下的列聯表：
$$
\begin{array}{|c|c|c|c|}
\hline
 &未婚已懷孕&已婚已懷孕&未婚未懷孕&總計\\
 \hline
 >60&11&22&15&48\\
 \hline
 \leq60&14&24&22&60\\
 \hline
 總計&25&46&37&108\\
 \hline
\end{array}
$$
而我們算出每一組的預期次數，以大於60分的未婚已懷孕女性為例：
$$
預期次數=\frac{48\times25}{108}
$$
得出每一格的預期次數為：
$$
\begin{array}{|c|c|c|c|}
\hline
 &未婚已懷孕&已婚已懷孕&未婚未懷孕\\
 \hline
 >60&11.11&20.44&16.44\\
 \hline
 \leq60&13.89&25.56&20.56\\
 \hline
\end{array}
$$
最後我們將只要算出卡方統計量$X^2$就可以判斷
$$
X^2=\sum^2_{i=1}\sum^3_{j=1}\frac{(O_{ij}-E_{ij})^2}{E_{ij}}=\frac{(11-11.11)^2}{11.11}+\frac{(22-20.44)^2}{20.44}\ldots+\frac{(22-20.56)^2}{20.56}\approx2.07
$$
查表，自由度為3-1=2的情況下，2.0695<$X^2_{\alpha=0.1}=4.605$，故我們不拒絕虛無假設。

## 程式輸出
從SAS的輸出結果我們也可以看到，在卡方檢定量的p-value為0.3553。我們也得出了不拒絕虛無假設的結論。

不管是從手算又或是程式的輸出，我們都沒有足夠的證據去證明，至少有一組的母體中位數於其他組不相同。即無法觀察到「未婚已懷孕的女性」、「已婚已懷孕的女性」以及「未婚未懷孕的女性」的心理健康狀況存在差異。
![[NA assignment 6 SAS_OUTPUT OF extension of median test.png]]

- - -
## Exercise 6.20（Kruskal-Wallis test）
## 基本假設
- 心理狀況的評分是來自於三組獨立隨機樣本，分別是「未婚已懷孕的女性」、「已婚已懷孕的女性」、「未婚未懷孕的女性」，樣本數分別為25、46、37，母體除了位置參數可能出現差異外，其餘分佈皆相同。
- 心理狀況的評分為連續型變數。
- 心理狀況的評分的至少是有序尺度的。
## 假設檢定
令
$M_1$為未婚已懷孕的女性心理健康分數之中位數
$M_2$為已婚已懷孕的女性心理健康分數之中位數
$M_3$為未婚未懷孕的女性心理健康分數之中位數
$$
H_0\text{：}M_1=M_2=M_3\quad\text{versus}\quad H_1\text{： }至少有一個M_i\neq M_j \quad i=1,2,3\quad j=1,2,3
$$
## 檢定統計量
合併三組樣本，並將所有觀察值由小到大進行排名的標記。

加總各個組別的排名，並將每一組的排名加總計為$R_i$

計算Kruskal-Wallis檢定量
$$
H=\frac{12}{N(N+1)}\sum^k_{i=1}\frac{R_i^2}{n_i}-3(N+1)
$$
N：全部觀察值的數量
$n_i$：每組的觀察值數量


我們將每一組的數值都賦予標記並且計算每一組的名次加總，結果如下
$$
\begin{array}{lc}
\hline
\text{Unwed}&5.5&5.5&5.5&13&13&19.5&19.5&19.5&28.5&28.5\\
\text{pregnant}&28.5&34&39&56.5&72&72&80&80&80&87.5\\
\text{girls}&91.5&97&97&97&105.5\\
&R_1=1275.5\\
\\
\text{Married}&5.5&10&13&19.5&19.5&19.5&28.5&28.5&28.5&28.5\\
\text{pregnant}&36&36&42&42&46&46&46&50.5&56.5&56.5\\
\text{woman}&56.5&56.5&56.5&56.5&64.5&64.5&64.5&64.5&64.5&72\\
 &72&72&80&80&80&80&80&87.5&87.5&87.5\\
 &97&97&97&102&105.5&105.5\\
 &R_2=2689.5\\
\\
\text{Unmarried}&1&5.5&5.5&5.5&5.5&13&13&19.5&19.5&28.5\\
\text{girl, not}&28.5&28.5&36&39&39&42&46&46&50.5&50.5\\
\text{pregnant}&50.5&56.5&64.5&64.5&64.5&72&72&80&87.5&87.5\\
 &91.5&97&97&97&105.5&105.5&105.5\\
 &R_3=1921
\end{array}
$$



$R_1$為未婚已懷孕的女性的心理狀況分數之名次加總
$R_2$為已婚已懷孕的女性的心理狀況分數之名次加總
$R_3$為未婚未懷孕的女性的心理狀況分數之名次加總

接下來計算Kruskal-Wallis檢定量
$$\begin{align}
H&=\frac{12}{108(108+1)}\sum^3_{i=1}\frac{R_i^2}{n_i}-3(108+1)\\\\
&=\frac{12}{108\times109}\left(\frac{(1275.5)^2}{25}+\frac{(2689.5)^2}{46}+\frac{(1921)^2}{37}\right)-3\times109\\\\
&\approx1.29796
\end{align}$$
但由於有ties，所以我們必須要帶入Kruskal-Wallis檢定量的修正
$$\begin{align}
H_c&=\frac{H}{1-\frac{\sum(t_i^3-t_i)}{N^3-N}}\\
&=\frac{-0.0632}{1-\frac{(12^3-12)+(25^3-25)+(20^3-20)}{108^3-108}}\\
&\approx -0.0645
\end{align}$$
哈哈，負的，殺了我吧。手算不行，交給程式。

## 程式輸出
我們可以看到在SAS的輸出，他的卡方檢定值為1.3037，P-value為0.5211，故我們不拒絕虛無假設的結論。

我們都沒有足夠的證據去證明，至少有一組的母體中位數於其他組不相同。即無法觀察到「未婚已懷孕的女性」、「已婚已懷孕的女性」以及「未婚未懷孕的女性」的心理健康狀況存在差異。
![[NA Assignment 6 Kruskal-Wallis test SAS output.png]]

## 附件 程式碼
``` SAS
data mental_health;
input Group$ Score @@;
cards;
NY 30 NY 40 NY 70 NY 75 NY 15 NY 20 NY 20 NY 32 NY 80 NY 25 NY 25 NY 25 NY 75 NY 30 NY 90 NY 30 NY 60 NY 85 NY 100 NY 90 NY 75 NY 70 NY 90 NY 15 NY 15
YY 15 YY 17 YY 25 YY 30 YY 35 YY 45 YY 50 YY 50 YY 55 YY 60 YY 60 YY 60 YY 100 YY 95 YY 80 YY 75 YY 70 YY 65 YY 60 YY 80 YY 30 YY 30 YY 25 YY 50 YY 60 YY 65 YY 65 YY 65 YY 70 YY 70 YY 75 YY 75 YY 90 YY 35 YY 75 YY 30 YY 25 YY 45 YY 65 YY 60 YY 20 YY 75 YY 100 YY 80 YY 90 YY 90
NN 20 NN 15 NN 60 NN 45 NN 15 NN 35 NN 55 NN 20 NN 70 NN 65 NN 30 NN 100 NN 90 NN 85 NN 10 NN 55 NN 25 NN 90 NN 80 NN 75 NN 25 NN 30 NN 65 NN 80 NN 55 NN 100 NN 15 NN 100 NN 50 NN 90 NN 30 NN 40 NN 15 NN 40 NN 50 NN 65 NN 70
;
PROC NPAR1WAY MEDIAN;
CLASS Group;
VAR Score; 
RUN;
PROC NPAR1WAY WILCOXON;
CLASS Group;
VAR Score;
RUN;
```
