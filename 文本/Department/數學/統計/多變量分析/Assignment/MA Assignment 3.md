# 問題：
[[MA Assignment]]

1. Using R or SAS, find the determinant, trace, inverse, eigenvalues, and eigenvectors of the matrix A, where：
$$
A=
\begin{bmatrix}
13&-4&2\\
-4&13&-2\\
2&-2&10
\end{bmatrix}
$$
用R或SAS來找到矩陣A的「行列式」、「跡」、「反矩陣」、「特徵值」以及「特徵矩陣」。

2. In an effort to develop improved peanuts, crop scientists routinely compare varieties with respect to several variables. A two-factor experiment with two replications was considered. Three varieties were grown at two geographical locations, and the three variables representing yield, sound mature kernels（SMK, weight in grams）and seed size（weight in grams）were measured. The data are shown as follows. Test the effects at $\alpha=0.05$ and make your conclusion.

為了培育改良的花生，作物科學家經常會比較品種之間的不同變數。本研究考慮了重複兩次的二因子實驗。實驗中，三個不同品種的花生分別種植於兩個不同的地理位置。並且測量了三個變數，分別是產量（Yield）、成熟飽滿種子重量（SMK，單位為克）以及種子大小（單位為克）。資料如下所示，請在顯著水準$\alpha$為0.05之下檢驗各因素的影響，並做出結論。

$$
\begin{array}{ccccc}
\hline
\text{Factor 1 Location}&\text{Factor 2 Variety}&Y_1\text{ Yield}&Y_2\text{ SMK}&Y_3\text{ Size}\\
\hline
2.0	&	8.0	&	200.0	&	173.8	&	67.2	\\
2.0	&	5.0	&	180.4	&	121.1	&	44.4	\\
2.0	&	6.0	&	197.6	&	161.8	&	54.1	\\
1.0	&	8.0	&	187.0	&	165.1	&	58.6	\\
1.0	&	5.0	&	194.3	&	167.7	&	53.7	\\
1.0	&	6.0	&	195.9	&	166.0	&	45.8	\\
2.0	&	8.0	&	201.5	&	166.8	&	65.0	\\
2.0	&	5.0	&	189.7	&	139.5	&	55.5	\\
2.0	&	6.0	&	202.7	&	166.1	&	60.4	\\
1.0	&	8.0	&	193.5	&	164.5	&	57.8	\\
1.0	&	5.0	&	195.3	&	153.1	&	51.4	\\
1.0	&	6.0	&	203.0	&	156.8	&	49.8	\\
\end{array}
$$

# 回答：
## 第一大題：
因為R比較簡短且方便，故這邊使用R來做示範。
#### 輸入資料
首先我透過`matrix()`來建立題目給定的3x3矩陣，將每一個元素從左到右，從上到下輸入，行數及列數設定為3。即可完成輸入。
`matrix(data,nrow,ncol)`
`data`：資料向量（也可以是列表）
`nrow`：指定列數
`ncol`：指定行數
#### 行列式

`det()`可以計算給定的矩陣之行列式值。
`det(x)`
`x`：欲計算的矩陣

最後得到的行列式值是1458。
#### 跡
雖然R沒有可以直接計算跡的方法，但我們可以透過`diag()`來得到對角元素，然後再透過`sum()`來將對角元素加總，就可以得到跡。
`sum(diag())
`sum(x)`
`x`：欲加總的數值元素、矩陣、向量

`diag(x)`
`x`：矩陣

最後得到的跡是36
#### 反矩陣
`solve()`可以直接計算給定矩陣的反矩陣。
`solve(x)`
`x`：欲得到反矩陣的矩陣

$$$$

最後得到的反矩陣為
$$
A^{-1}=
\begin{bmatrix}
0.08649&0.02469&-0.01234\\
0.02469&0.08641&0.01234\\
-0.01234&0.01234&0.10493
\end{bmatrix}
$$
#### 特徵值＆特徵矩陣
透過`eigen()`他會透過list形式給你矩陣中的特徵值以及特徵向量。
可以利用`list名稱$value`跟`list名稱$vector`的方式分別叫出特徵值以及特徵向量。

```R
A <- matrix(c(13,-4,2,-4,13,-2,2,-2,10),nrow = 3,ncol = 3)

det_A <- det(A)

cat("determinant：", det_A)

trace_A <- sum(diag(A))
cat("trace：", trace_A)

inv_A <- solve(A)
cat("inverse：")
inv_A


# 特徵值（eigen可以直接幫你算特徵植跟特徵向量,list）
eig_A <- eigen(A)

eig_values <- eig_A$values
cat("eig_values：", eig_values)

# 特徵向量
eig_vectors <- eig_A$vectors
cat("eig_values：", eig_values)
```


