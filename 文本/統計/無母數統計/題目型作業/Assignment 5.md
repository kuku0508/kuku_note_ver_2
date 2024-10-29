![[nonparametric statistic Assignment 5.pdf]]
# 問題：
## Exercise 3.10
Von Burg and Rustam (E15) reported values of the median nerve motor conduction velocity shown in Table 3.23. Experimental subjects admitted to a hospital had been diagnosed as having methylmercury poisoning and as having eaten contaminated bread. The controls were members of the hospital personnel who had presumably escaped exposure to the contaminated bread. Do these data provide suffcient evidence to indicate that the populations represented by the two samples have different distributions?Let $\alpha = 0.025$.

**Median nerve motor conduction velocity（meters per second）in two groups of subjects**
$$
\begin{array}{lcccccccccccc}
\hline
\text{Controls（X）}&68&67&58&62&55&60&67\\
\\\text{Experimental} \\\text{subjects（Y）}&60&59&72&73&56&53&43&50&65&56&56&56&57&36
\end{array}

$$

## Exercise 3.15
Gill and Murray（E19）conducted an experiment designed to test discrimination of song ability among blue-winged and golden-winged warblers（Vermivora pinus and
V . chrysopetra）of southeastern Michigan.Within the hearing range of territorial malesm te experimenters played tape recordings of songs of the listening bird and songs of the other species. Discminatory behavior of the birds was based on whether they reponded to the recordings. Table 3.33 shows 22 birds classified according to species and discriminatory behavior. Can we conclude on the basis of these data that the proportion on nondiscriminators is higher among golden-wings than amoong blue-wings ? Let $\alpha = 0.05$. Determine the P value. 

**Discriminatory behavior of territorial male Vermivora**
$$
\begin{array}{llll}
\hline
\text{Species}&\text{Discriminaotrs}&\text{Nondiscriminators}&\text{Total}\\
\hline
\text{Michigan blue-wings}&4&6&10 \\
\text{Michigan golden-wings}&3&9&12\\
\text{Total}&7&15&22
\end{array}
$$
## Exercise 4.3
Smite and Di Girolamo（E4）exanined the morphological changes in epididymal fat cells of mature,moderately obese rat during reduction of body weight and adipose tissue mass. Table4.5 shows part of their results. Do these data provide sufficient evidence at the 0.05 level of significance to indicate that reduction of body weight reduces the diameter of fat cells?

**Mean\* fat cell diameters, in micrometers, of mature, moderately obese rats before and after 20% reduction in body weight by underfeeding**
$$
\begin{array}{lcccccc}
\hline
\text{Rat}&1&2&3&4&5&6\\
\text{Before（X）}&84.4&86.0&84.9&93.9&95.2&96.6\\
\text{After（Y）}&62.9&75.4&78.2&83.6&57.6&58.0\\
\\\text{Rat}&7&8&9&10&11&12\\
\text{Before（X）}&97.5&101.4&103.8&115.2&116.4&134.5\\
\text{After（Y）}&69.6&76.5&73.9&88.0&73.8&94.1\\
\end{array}
$$
- - -
# 回答：

## Exercise 3.10
Von Burg 和 Rustam (E15) 報告了表 3.23 中顯示的正中神經傳導速度資料。實驗組的受試者是在醫院中被診斷為甲基汞中毒且吃了受污染的麵包。對照組則是醫院人員，據推測未接觸到受污染的麵包。這些資料是否提供了足夠的證據表明兩個樣本的母體服從不同的分配？令顯著水準為 $\alpha = 0.025$。

**兩組受試者的正中神經運動傳導速度（米/秒）**
$$
\begin{array}{lcccccccccccc}
\hline
\text{對照組（X）}&68&67&58&62&55&60&67\\
\\\text{實驗組（Y）}&60&59&72&73&56&53&43&50&65&56&56&56&57&36
\end{array}
$$

因為要檢驗兩組樣本是否服從不同的分配，我們這邊可以使用Wald-Wolfowitz Runs Test來達到我們的要求。以下逐步進行：
### 基本假設：
- 對照組（X）以及實驗組（Y）分別來自於不同母體，且皆為獨立觀測值。
- 正中神經運動傳導速度為連續型變數。
### 假設檢定
$H_0$：對照組之母體與實驗組之母體為相同分配。
$H_1$：對照組之母體與實驗組之母體為不同分配。

令合併兩組樣本之Runs的個數為$r$，對照組樣本數為$n_1=7$，實驗組樣本數為$n_2=14$

最多的Runs的情況為：
$$
\begin{array}{ccccc}
\hline
36&43&50&53&55&56&56&56&56&57&\\y&y&y&y&x&y&y&y&y&y\\58&59&60&60&62&65&67&67&68&72&73\\
x&y&x&y&x&y&x&x&x&y&y
\end{array}
$$
$r=11$

最少的Runs的情況為：
$$
\begin{array}{ccccc}
\hline
36&43&50&53&55&56&56&56&56&57&\\y&y&y&y&x&y&y&y&y&y\\58&59&60&60&62&65&67&67&68&72&73\\
x&y&y&x&x&y&x&x&x&y&y
\end{array}
$$
$r=9$

我們將最多以及最少的$r$取平均，得出$\frac{11+9}{2}=10$，後查表
![[Runs test Lower and Upper Table.png]]
當今天$r$落在$5$到$15$之間，我們就不拒絕虛無假設$H_0$。
而我們的$r=10$
故我們不拒絕虛無假設$H_0$
我們沒有足夠強烈的證據證明，兩組樣本之母體服從不同分配。

我們透過R的書出來進一步檢驗結果。R的輸出如下：

Wald-Wolfowitz Runs Test
data：x and y
$$
\begin{array}{ccccc}
\hline
\text{runs}=11&\text{m}=7&\text{n}=14&\text{p-value}=0.8155\\
\end{array}
$$
alternative hypothesis: true number of runs is not equal the expected number

其P-value=0.8155大於顯著水準，故我們不拒絕虛無假設$H_0$。與我們手算得出的結論一致。


## Exercise 3.15
Gill 和 Murray（E19）進行了一項實驗，旨在測試密西根州東南部藍翼和金翼林鶯（Vermivora pinus 和 V.chrysopetra）的歌曲辨別能力。在領地，雄性鳥的聽覺範圍內，實驗者播放了該鳥種和其他物種的歌曲錄音。鳥類的辨別行為基於牠們是否對錄音做出反應。表 3.33 顯示了 22 隻鳥，根據物種和辨別行為進行分類。基於這些數據，我們能否得出結論，金翼林鶯中的不辨別者比例高於藍翼林鶯？設$\alpha = 0.05$。請計算P值。 

$$
\begin{array}{lll|l}
\hline
\text{物種}&\text{辨別鳥}&\text{無辨別鳥}&\text{總計}\\
\hline
\text{密西根藍翼林鶯}&4&6&10 \\
\text{密西根金翼林鶯}&3&9&12\\
\hline
\text{總計}&7&15&22
\end{array}
$$
### 基本假設
- 密西根藍翼林鶯以及密西根金翼林鶯的數量顧ㄉㄧ