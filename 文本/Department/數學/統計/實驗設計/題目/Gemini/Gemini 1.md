---
參考資料:
---
# 問題：
$$
Y_{ijk}=\mu+A_i+B_{j(i)}+\epsilon_{k(ij)}
$$

畫EMS table
#### 1. 題目情境：裝填彈藥大作戰 (Example 7.1)

我們來看看這個實驗的結構 1：

- **因子 M (Method, 方法)**：有 2 種方法 ($i=1,2$)。 $\rightarrow$ **Fixed**
- **因子 G (Group, 群組)**：有 3 個群組 ($j=1,2,3$)。 $\rightarrow$ **Fixed**
- **因子 T (Team, 小隊)**：每個群組裡面有 3 個小隊 ($k=1,2,3$)。
    - 注意！小隊是屬於群組的，所以是 **巢狀於 G ($T_{k(j)}$)**。
    - 小隊是隨機抽取的。 $\rightarrow$ **Random**
- **重複 (Replicates)**：做 2 次 ($m=1,2$)。
模型長這樣 (超長！)：
$$Y_{ijkm} = \mu + M_i + G_j + MG_{ij} + T_{k(j)} + MT_{ik(j)} + \epsilon_{m(ijk)}$$
# 回答：
$$
\begin{array}{llll}
&i(f,a)&j(r,b)&k(r,n)&EMS\\
\hline
A_i&0&b&n&bn\,\phi_A+n\,\sigma^2_{B_{(A)}}+\sigma^2_\epsilon\\
B_{j(i)}&0&1&n&n\,\sigma^2_{B_{(A)}}+\sigma^2_\epsilon\\
error&1&1&1&\sigma^2_\epsilon\\
\end{array}
$$
- - -
$$
\begin{array}{llll}
&i(f,2)&j(f,3)&k(r,3)&m(r,2)&EMS\\
M_i&0&3&3&2\\
G_j&2&0&3&2\\
MG_{ij}&0&0&3&2\\
T_{k(j)}&2&0&1&2\\
TM_{ik(j)}&0&0&1&2\\
error&1&1&1&1
\end{array}
$$