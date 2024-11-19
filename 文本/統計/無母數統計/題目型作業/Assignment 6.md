# 問題：
![[nonparametric statistic Assignment 6.pdf]]

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
為了測量一個人的心理健康狀況，對三組受試者進行了測試，其結果如表 6.28 所示。根據這些資料，是否可以得出結論，這三組之間的心理健康狀況存在差異？請使用extension of median test 進行檢驗。

## 基本假設
- 心理狀況的評分是來自於三組獨立隨機樣本，分別是「未婚已懷孕的女性」、「已婚已懷孕的女性」、「未婚未懷孕的女性」，樣本數分別為25、46、37，母體中位數$M_1$、$M_2$、$M_3$未知。
- 心理狀況的評分至少都是有序尺度的。
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

計算這個列聯表的卡方統計量。
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
 &未婚已懷孕&已婚已懷孕&未婚未懷孕&總計\\
 \hline
 >60&11.11&20.44&16.44&48\\
 \hline
 \leq60&13.89&25.5&22&60\\
 \hline
 總計&25&46&37&108\\
 \hline
\end{array}
$$