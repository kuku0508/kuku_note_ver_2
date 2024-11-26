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
- 患者的肺活量


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
