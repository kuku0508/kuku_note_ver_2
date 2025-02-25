# 問題：
![[Regression analysis Assignment 3.pdf]]
## Problem 2.10
The weight and systolic blood pressure of 26 randomly selected males in the age group 25-30 are shown below.Assume that weight and blood pressure（BP）are jointly normally distributed.
a. Find a regression line relating sytolic blood pressure to weight.
b. Estimate the corrlation coefficient.
c. Test the hypothesis that $\rho=0$
d. Test the hypothesis that $\rho=0.6$.
e. Find a 95% CI for $\rho$
$$
\begin{array}{lcc|ccc}
\hline
\text{Subject}&\text{Weight}&\text{Systolic BP}&\text{Subject}&\text{Weight}&\text{Systolic BP}\\
\hline
1& 165& 130& 14& 172& 153\\ 
2& 167& 133& 15& 159& 128\\ 
3& 180& 150& 16& 168& 132\\ 
4& 155& 128& 17& 174& 149\\ 
5& 212& 151& 18& 183& 158\\ 
6& 175& 146& 19& 215& 150\\ 
7& 190& 150& 20& 195& 163\\ 
8& 210& 140& 21& 180& 156\\ 
9& 200& 148& 22& 143& 124\\ 
10& 149& 125& 23& 240& 170\\ 
11& 158& 133& 24& 235& 165\\ 
12& 169& 135& 25& 192& 160\\ 
13& 170& 150& 26& 187& 159\\ 
\hline
\end{array}
$$
## Problem 2.11
Consider the weight and blood pressure data in Problem 2.10. Fit a no-interceot model to the data and compare it to the model obtained in Problem 2.10. Which model would you conclude is superior?
# 回答：
我們有一份資料是隨機選擇了26位25歲到30歲的男人，並記錄了她們的體重以及收縮壓
2.10.且我們假設體重以及血壓為聯合常態分配。
## a. 求體重對收縮壓關聯之迴歸線
我們使用SAS，用附件a的程式碼輸出如下：
![[Assignment 3 2.10 a.png]]
我們可以看到截距估計值為69.10437，斜率估計值為0.41942。且截距以及斜率的Pr > | t |皆小於0.0001，故我們有很強的證據證明，截距以及斜率皆不為0。故我們可以知道其簡單線性迴歸模型為
而我們也可以，當今天體重增加1磅的時候，收縮壓平均會增加0.41942毫米汞柱：
$$
\hat{y}=69.10437+0.41942\times x
$$
## b. 估計相關係數
我們對資料使用PROC CORR，得出其相關係數為0.77349
![[Pasted image 20241028221709.png]]
## c. 對資料做$\rho=0$的假設檢定
我們一樣是用上面那張圖，可以看到在$\rho=0$的虛無假設之下，其p-value小於0.0001。故這裡我們拒絕虛無假設$\rho=0$，我們有強烈的證據可以證明，收縮壓與體重之間的相關係數不等於0，也就是說收縮壓與體重之間，並不是完全沒有線性關係的。
![[Pasted image 20241028221935.png]]
## d.對資料做$\rho=0.6$的假設檢定
在這邊我們重新進行虛無假設，並輸出了新的結果。可以看到在$\rho=0.6$的虛無假設之下，其p-value為0.1204。故我們這邊不拒絕虛無假設$\rho=0.6$。也就是說，我們沒有強烈的證據去證明，收縮壓與體重之間的相關係數不等於0.6。
![[Pasted image 20241028222310.png]]

## e.求在95%信賴區間的相關係數為何
![[Assignment 3 2.10 e.png]]
**【圖一 體重與收縮壓之相關係數的信賴區間】**

從SAS輸出的結果我們可以看到，在95%的信心水準之下，相關係數的信賴區間為\[0.540462 , 0.890051\]，也就是說在95%的信心水準之下，相關係數的值落在\[0.540462 , 0.890051\]。

## 2.11 輸出一個無截距的模型並比較2.10的模型

![[Assignment 3 2.11 regression.png]]
**【圖二 體重與收縮壓的迴歸模型 - 截距不為0】**

![[Pasted image 20241028224714.png]]
**【圖三 體重與收縮壓的迴歸模型 - 截距為0】**

我們使用了程式碼對體重以及收縮壓配適了有考慮截距的模型以及無截距模型的模型。
圖二為有考慮截距模型的資訊，而圖三為假設**無截距**模型之資訊。
我們可以看到考慮截距的模型，其$R^2$為0.5983，MSE為75.35719。
無截距的模型，其$R^2$為0.9929，MSE為158.70727。

雖然無截距的模型，其$R^2$遠高於有截距的模型，但是在比較有截距以及無截距的模型時，$R^2$並不會是一個特別有效的評估指標。特別是當今天將模型強制通過原點時，$R^2$時常被高估。

一般有截距的模型，$R^2$的表示為下：
$$
R^2=\frac{\sum^n_{i=1}(\hat{y_i}-\bar{y})^2}{\sum^n_{i=1}(y_i-\bar{y})^2}=\frac{SSR}{SST}
$$

而在無截距的模型中，$R^2$會變成：
$$
R^2=\frac{\sum^n_{i=1}\hat{y_i}^2}{\sum^n_{i=1} y_i^2}
$$
我們可以發現，在有截距以及無截距的模型中，我們的$R^2$公式其實是不同的，導致$R^2$在比較有截距以及無截距的模型時，並不能算是一個非常有效的指標。
但在MSE裡面，並沒有類似$R^2$這樣的問題。故我們這邊在比較無截距以及有截距的模型時，應該使用MSE來作為我們的評估指標。

而在兩模型間，有截距的模型具有更小的MSE（75.35719），故我們這邊選擇有截距的模型。

# 附件
### a.
```SAS
DATA;
input weight bp;
cards;
165 130
167 133
180 150
155 128
212 151
175 146
190 150
210 140
200 148
149 125
158 133
169 135
170 150
172 153
159 128
168 132
174 149
183 158
215 150
195 163
180 156
143 124
240 170
235 165
192 160
187 159
;
proc reg;
model bp=weight;
run;

proc corr fisher (RHO0=0); 
var weight bp;
run;

proc corr fisher (RHO0=0.6);
var weight bp;
run;

proc reg;
model bp=weight/noint;
run;
```
