# 問題：
![[NA Assignment 7.pdf]]
## Exercise 6.10
Wohl et al.(E13) studied the physiological properties of the lungs in patuents who received therapeutic bilateral pulmonary irradiation in early childhood. Their subjects consisted of three groups of children. Group 1 was composed of six childhood. Their subjects consisted of course of bilateral pulmonary irradiation. Group 2 contained six children who had received additional pulmonary radiotherapy or thoracic surgery or both. Group 3 consisted of eight children who received no irradiation directed primarily to the lung. Vital capacity values,expressed as percentages of predicted values vbased on standing height, for subjects in the three groups are shown in Table 6.17. Test the null hypothesis of no difference among the three populations represented against the order：$\text{group 2}\leq\text{group 1}\leq\text{group 3}$. Determine the P-value.


**Vital capacity values,expressed as percentage of predicted values based on standing height, in three groups of subjects**
- - -
##### Group 1：Bilateral pulmonary irradiation
$$
\begin{array}{c}
\hline
&71&57&85&67&66&79
\end{array}
$$
##### Group 2：Additional pulmonary irradiation or thoracic surgery
$$
\begin{array}{c}
\hline
76&94&61&36&42&49
\end{array}
$$
##### Group 3：No pulmonary irradiation
$$
\begin{array}{c}
\hline
80&104&81&90&93&85&101&83
\end{array}
$$

## Exercise 7.2
Perry et al.(E2)determined plasma epinephrine concentrations during isoflurane, halothane, and cyclopropane anesthesia in 10 dogs. The results are shown in Table 7.9. Do these data suggest a difference in treatment effects? Find the P-value.

**Convertrations, nanograms per milliliter, of free catecholamines in arterial plasma in response to isoflurane, halothane and cyclopropane**
- - -
$$
\begin{array}{rr}
\hline
\text{Dog}&1&2&3&4&5&6&7&8&9&10\\
\hline
\text{Isoflurane}&0.28&0.51&1.00&0.39&0.29&0.36&0.32&0.69&0.17&0.33\\
\text{Halothane}&0.30&0.39&0.63&0.38&0.21&0.88&0.39&0.51&0.32&0.42\\
\text{Cyclopropane}&1.07&1.35&0.69&0.28&1.24&1.53&0.49&0.56&1.02&0.30
\end{array}
$$

# 回答：
## Exercise 6.10
Wohl等人研究了兒童在早期接受雙側肺部放射治療患者的肺部生理特性。受試者分為三組，分別是：

第一組：接受過雙側肺部放射治療的兒童，樣本數為6。
第二組：接受過雙側肺部放射治療或胸部手術，又或是兩種治療皆有接受的兒童，樣本數為6。
第三組：未接受肺部放射治療的兒童，樣本數為8，

以下數據為每組受試者的肺活量值（按站立身高預測百分比表示），如下表所示。檢驗虛無假設：「三組代表的母體之間無顯著差異」，針對以下有序假設：
$$
\text{第二組}\leq\text{第一組}\leq\text{第三組}
$$
並決定其p值。


**根據身高預測值百分比計算的三組受試者肺活量數據**
- - -
##### 第1組：雙側肺部照射
$$
\begin{array}{c}
\hline
&71&57&85&67&66&79
\end{array}
$$
##### 第2組：額外肺部照射或胸腔手術
$$
\begin{array}{c}
\hline
76&94&61&36&42&49
\end{array}
$$
##### 第3組：未進行肺部照射
$$
\begin{array}{c}
\hline
80&104&81&90&93&85&101&83
\end{array}
$$

因為要檢定樣本所代表的母體是否存在顯著差異，且他的假設為「$\text{第二組}\leq\text{第一組}\leq\text{第三組}$」，故我們這邊使用Jonckheere-Terpstra Test來檢驗其假設是否正確。而我們需要先檢驗此資料是否符合Jonckheere-Terpstra Test所要求的假設：
## 基礎假設：
- 患者的肺活量值是連續型的變數。
- 患者的肺活量值的測量尺度至少是有序尺度。
- 患者的肺活量值由三組獨立隨機樣本建構，其樣本數分別是6、6以及8，來自相同母體分配除了具有相異位置函數且中位數未知。
## 虛無假設
令
$M_1$為接受雙側肺部照射的兒童其肺活量值之中位數
$M_2$為接受額外肺部照射或胸腔手術的兒童其肺活量值之中位數
$M_3$為未進行肺部照射的兒童其肺活量值之中位數
$$
H_0\text{：}M_1=M_2=M_3\quad\text{versus}\quad H_1\text{：}M_2\leq M_1\leq M_3 其中至少有一個嚴格不等式
$$
# 檢定統計量
我們需要比較三組的大小，將每一組的樣本i，與其他組的樣本 j 進行比較，若樣本 i 小於 樣本j，則將其記錄1，若數值一致，其記錄值表示為$U_{ij}$，則記錄其為0.5，並將所有樣本都進行比較。
最後加總所有紀錄值，得到Jonckheere-Terpstra test統計量$J=\sum_{i<j}U_{ij}$。
最後進行查表。
$$
\begin{array}{|c|c|}
\hline
編號&第一組&第二組&第三組&U_{21}&U_{13}&U_{23}\\
\hline
1&71&76&80&2&8&8\\
2&57&94&104&0&8&2\\
3&85&61&81&5&4.5&8\\
4&67&36&90&6&8&8\\
5&66&42&93&6&8&8\\
6&79&49&85&6&8&8\\
7& & &101&0&0&0\\
8& & & 83&0&0&0\\
\hline
總和& & & &25&44.5&42\\
\hline
\end{array}
$$

$$
J=\sum_{i<j}U_{ij}=25+44.5+42=111.5
$$
![[Jonckheere terpstra查表 6 6 8.png]]
我們可以看到Jonckheere-Terpstra test統計量J=111的p-value小於0.005，故我們拒絕虛無假設，我們有強烈的證據證明三組之間的肺活量值具有明顯差異，且「接受額外肺部照射或胸腔手術的兒童之肺活量值」小於「接受雙側肺部照射的兒童之肺活量值」小於「未進行肺部照射的兒童之肺活量值」。
## SAS
![[Pasted image 20241126223333.png]]
我們可以看到，在SAS的輸出中，JT檢定的P-value為0.0142，故我們拒絕虛無假設，與手算結果相同。
## Exercise 7.2
Perry等人測定了10隻狗在異氟醚（isoflurane）、氟烷（halothane）、環丙烷（cyclopropane）麻醉期間的血漿腎上腺素濃度。下表顯示了10隻狗在接受三種麻醉劑後反應時間的變化。結果如下表所示。這些數據是否顯示三種麻醉劑的治療效果存在差異。

**異氟醚、氟烷和環丙烷反應後，動脈血漿中游離兒茶酚胺濃度（單位：毫微克/毫升）**
- - -
$$
\begin{array}{rr}
\hline
\text{狗}&1&2&3&4&5&6&7&8&9&10\\
\hline
\text{異氟醚}&0.28&0.51&1.00&0.39&0.29&0.36&0.32&0.69&0.17&0.33\\
\text{氟烷}&0.30&0.39&0.63&0.38&0.21&0.88&0.39&0.51&0.32&0.42\\
\text{環丙烷}&1.07&1.35&0.69&0.28&1.24&1.53&0.49&0.56&1.02&0.30
\end{array}
$$
為資料每一隻狗在獨立注射三種不同的麻醉劑後，血漿中的游離兒茶酚胺濃度，三種麻醉劑分別為異氟醚（Isoflurane）、氟烷（Halothane）、環丙烷（Cyclopropane），故我們這邊可以使用Friedman Test。
## 基礎假設
- 此資料由10組獨立的樣本建構，且每組樣本中皆有3種不同的麻醉藥效。
- 注射麻醉劑的狗狗其動脈血漿中游離兒茶酚胺濃度為連續型變數。
- 麻醉劑種類與每支注射麻醉劑的狗狗之間無交互作用。
- 在注射不同的麻醉劑後，狗狗動脈血漿內的游離兒茶酚胺的濃度可以進行排序。
## 虛無假設

令
$M_1$為注射異服醚後狗狗動脈血漿中的游離兒茶酚胺濃度的中位數。
$M_2$為注射氟烷後狗狗動脈血漿中的游離兒茶酚胺濃度的中位數。
$M_1$為注射環丙烷後狗狗動脈血漿中的游離兒茶酚胺濃度的中位數。
$R_1$為注射異氟醚後每一隻狗狗動脈血漿中的游離兒茶酚胺濃度與其他麻醉劑比較之排名總和。
$R_2$為注射氟烷後每一隻狗狗動脈血漿中的游離兒茶酚胺濃度與其他麻醉劑比較之排名總和。
$R_3$為注射環丙烷後每一隻狗狗動脈血漿中的游離兒茶酚胺濃度與其他麻醉劑比較之排名總和。
$$
H_0\text{：}M_1=M_2=M_3\quad\text{versus}\quad H_1\text{：}至少有一個M_i\neq M_j \quad i=1,2,3\quad j=1,2,3
$$
## 檢定統計量

$$
\text{Friedman test statistic}= \frac{12}{bk(k+1)}\sum^k_{j=1}\left[R_j-\frac{b(k+1)}{2}\right]^2
$$
b為樣本數
k為麻醉劑種類數

以下是每一隻狗狗在注射異服醚、氟烷、環丙烷後動脈血漿中游離兒茶酚胺的濃度，單位為毫微克/毫升。
$$
\begin{array}{rr}
\hline
\text{狗}&1&2&3&4&5&6&7&8&9&10\\
\hline
\text{異氟醚}&0.28&0.51&1.00&0.39&0.29&0.36&0.32&0.69&0.17&0.33\\
\text{氟烷}&0.30&0.39&0.63&0.38&0.21&0.88&0.39&0.51&0.32&0.42\\
\text{環丙烷}&1.07&1.35&0.69&0.28&1.24&1.53&0.49&0.56&1.02&0.30
\end{array}
$$
我們將以下的表格以不同的麻醉劑，同一隻狗狗做由小到大標記其排名：
$$
\begin{array}{rr}
\hline
\text{狗}&1&2&3&4&5&6&7&8&9&10\\
\hline
\text{異氟醚}&1&2&3&3&2&1&1&3&1&2&R_1=19\\
\text{氟烷}&2&1&1&2&1&2&2&1&2&3&R_2=17\\
\text{環丙烷}&3&3&2&1&3&3&3&2&3&1&R_3=23
\end{array}
$$
我們將值帶入：
$$
\frac{12}{10\times3\times(3+1)}\left[19-\frac{}{}\right]^2
$$
