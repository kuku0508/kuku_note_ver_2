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

## e
![[Assignment 3 2.10 e.png]]
**【圖一 體重與收縮壓之相關係數的信賴區間】**

從SAS輸出的結果我們可以看到，在95%的信心水準之下，相關係數的信賴區間為\[0.540462 , 0.890051\]，也就是說在95%的信心水準之下，相關係數的值落在\[0.540462 , 0.890051\]。

## 2.11

![[Assignment 3 2.11 regression.png]]
**【圖二 體重與收縮壓的迴歸模型 - 截距不為0】**

![[Assignment 3 2.11 no intercept.png]]
**【圖三 體重與收縮壓的迴歸模型 - 截距為0】**

我們使用了程式碼對體重以及收縮壓配適了有考慮截距的模型以及無截距模型的模型。
圖二為有考慮截距模型的資訊，而圖三為假設**無截距**模型之資訊。
我們可以看到考慮截距的模型，其$R^2$為0.5983，MSE為75.35719。
無截距的模型，其$R^2$為0.9929，MSE為158.70727。

雖然無截距的模型，其$R^2$遠高於有截距的模型，但是在比較有截距以及無截距的模型時，$R^2$並不會是一個特別有效的評估指標。特別是當今天將模型強制通過原點時，$R^2$時常被高估。

在吳傑

故我們這邊會使用MSE作為模型評估標準。
而在兩模型間，有截距的模型具有更小的MSE（75.35719），故我們這邊選擇有截距的模型。

# 附件
```SAS
DATA Systolic_Weight;
input Weight Systolic_BP;
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
PROC REG;
MODEL Systolic_BP = Weight;
RUN;

PROC REG;
 MODEL Systolic_BP = Weight / noint;
RUN;
```
