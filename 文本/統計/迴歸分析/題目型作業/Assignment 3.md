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
我們可以看到截距估計值為69.10437，斜率估計值為0.41942。且截距以及斜率的Pr > | t |皆小於0.0001，故我們有很強的證據證明，截距以及斜率皆不為0。故我們可以知道其簡單線性迴歸模型為：
$$
\hat{y}=69.10437+0.41942\times x
$$
## b. 估計相關係數
我們對資料使用PROC CORR，得出其相關係數為0.77349
![[Pasted image 20241028221709.png]]
## c. 對資料做$\rho=0$的假設檢定
我們一樣是用上面那張圖，可以看到在$\rho=0$的虛無假設之下，其p-value為0.0001
![[Pasted image 20241028221935.png]]

# 附件
### a.
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

PROC CORR fisher;
 VAR Weight Systolic_BP;
RUN;
```
