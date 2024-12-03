處理事件：[[Cox-Stuart test]]
使用的Procedure：[[UNIVARIATE]]

# 範例
隨著汙染增加，蟲族的進攻不斷，現在堡壘裡面的人們正在討論是否需要增強牆邊武器威力，一派人馬認為不需要增強，蟲族看似並沒有增加的趨勢。另外一派人馬認為，蟲族進攻越發強烈，需要增強武器威力。以下我們收集了最近50波的蟲族攻擊的蟲族數量。
$$
\begin{array}{|c|c|c|c|}
\hline
\text{波數}&\text{蟲族數量}&\text{波數}&\text{蟲族數量}\\
\hline
1&37&26&52\\
2&34&27&53\\
3&33&28&57\\
4&37&29&54\\
5&39&30&61\\
6&35&31&52\\
7&41&32&53\\
8&38&33&62\\
9&42&34&53\\
10&39&35&59\\
11&44&36&61\\
12&39&37&69\\
13&34&38&60\\
14&43&39&72\\
15&45&40&64\\
16&43&41&18\\
17&46&42&53\\
18&39&43&71\\
19&47&44&75\\
20&46&45&72\\
21&49&46&74\\
22&51&47&81\\
23&46&48&80\\
24&48&49&10\\
25&50&50&1\\
\hline
\end{array}
$$
# 輸入
``` SAS
/*建立資料集*/
data worm;
/*辨識變數*/
input worm1 worm2;
/*定義配對變數*/
DIFF=worm2-worm1;
/*輸出資料*/
cards;
37 52
34 53
33 57
37 54
39 61
35 52
41 53
38 62
42 53
39 59
44 61
39 69
36 60
43 72
45 65
43 18
46 53
39 71
47 75
46 72
49 74
51 81
46 80
48 10
50 1
;
/*使用Procedure UNIVARIATE*/
PROC UNIVARIATE;
/*指定處理變數DIFF*/
	VAR DIFF;
/*執行程式碼*/
RUN;
```
- `worm1`、`worm2`：我們這邊將50波的蟲族數量劃分成了兩個變數，`worm1`主要是前25波的蟲族數量，`worm2`是第26波到第50波的蟲族數量。會這樣劃分的原因是因為，在[[Cox-Stuart test]]裡面，我們也會把資料分半成兩組，將其相減，以進行[[Cox-Stuart test]]。
- `DIFF`：你可以看到我們把前25波的蟲族數量減去了後25波的蟲族數量，就如前面所說在[[Cox-Stuart test]]，我們會將資料前半後半進行相減，檢視相減後的正負號數。所以這個變數你可以把他想成[[Cox-Stuart test]]裡面的配對結果。
`PROC UNIVARIATE`：指定使用Procedure [[UNIVARIATE]]。
- `VAR DIFF`：定義處理的變數為`DIFF`。
- `RUN`：執行程式碼。

# 輸出
![[Cox-stuart test in SAS output.png|500]]
你可以看到，因為Cox-stuart test的p-value計算方式跟Sign test一樣，所以我們這邊可以看跟Sign test一樣的部分，你可以看到他的雙尾的p-value為0.0002，而這時候你可以看到他的檢定統計量是顯示正號，代表正數的數量大於負數。故我們這邊將p-value直接除以2就會等於是否有上升趨勢的假設檢定的檢定統計量。

# 備註
你可能注意到了，在SAS的檢定統計量裡面，跟我筆記裡面的Cox-stuart test的檢定統計量的表示是不一樣的，當你看到有小數點的時候就可能感受到了不對勁。這個是因為SAS在計算Sign test的檢定統計量的時候，他的計算方式不是看正號有多少個或是負號有多少個，在SAS裡面是這樣敘述的：
>Sign test
>PROC UNIVARIATE calculates the sign test statistic as
>$$M=\frac{n^+-n^-}{2}$$
>where $n^+$ is the number of values that are greater than $\mu_0$ , and $n^-$ is the number of values that are less than $\mu_0$ . Values equal to $\mu_0$ are discarded. Under the null hypothesis that the population median is equal to $\mu_0$ , the p-value for the observed statistic $M_{obs}$ is 
>$$ Pr(\mid M_{obs}\mid\geq\mid M\mid)=0.5^{(n_t-1)}\sum^{min(n^+,\,n^-)}_{J=0}\binom{n_t}{i}$$
>where $n_t=n^++n^-$ is the number of $x_i$ values not equal to $\mu_0$
>**Note**：If $n^+$ and $n^-$ are equal, the p-value is equal to one.

這段大致是在講，在SAS裡面，對於[[單樣本符號檢定|Sign test]]的檢定統計量的計算方式是採取，正負號相減後除以2的方法，而p-value一樣是透過二項分配的方式來計算他的雙尾p-value。
但你一定也注意到了，在p-value的計算中，並不會直接使用到檢定統計量$M$，因為檢定統計量這邊只是讓我們知道式正號比較多，還是負號比較多。當今天檢定統計量是正號的時候，你就可以知道在資料中是正號多於負號；相反，當今天檢定統計量是負號的時候，你就可以知道在資料中是負號多於正