![[Regression analysis Assignment 2.pdf]] 
# 問題：
## Problem 2.4
Table B.3 presents data on the gasoline mileage performance of 32 different automoblies.

a. Fit a simple linear regression model relating gasoline mileage y(miles per gallon) to engine displacement $x_1$ (cubic inches).

b. Construct the analysis-of-variance table and test for significance of regression.

c. What percent of the total variability in gasoline mileage is accounted for by the linear relationship with engine displacement?

d. Find a 95% CI on the mean gasoline mileage if the engine displacement is 275 in$.^3$

e. Suppose that we wish to predict the gasoline mileage obtained from a car with a 275-in$.^3$ engine.Give a point estimate of mileage.Find a 95% prediction interval on the mileage.

f. Compare the two intervals obtained in parts d and e . Explain the differnce between them.Which ine is wider,and why?

![[Linear regression Table B.3 Gasoline Mileage Performance for 32 Automobiles.pdf]]
## Problem 2.5
Consider the gasoline mileage data in Table B.3. Repeat Problem 2.4(parts a , b and c ) using vehicle weright $x_{10}$ as the regressor variable . Based on a comparison of the two models, can youconclude that $x_1$ is a better choice of tegressor that $x_{10}$.

# 回答：
## Problem 2.4：
### a. 
我們先使用SAS將引擎排量$x_1$作為預測變數，汽油里程$y$作為反應變數，建構一個簡單線性迴歸。程式碼如下：
```SAS
PROC IMPORT OUT= WORK.assignment2_data 
   DATAFILE= "C:\Users\kuku\Downloads\Linear Regression assignment 2 data.xlsx" 
   DBMS=EXCEL REPLACE;
 RANGE="sheet 1$"; 
 GETNAMES=YES;
 MIXED=NO;
 SCANTEXT=YES;
 USEDATE=YES;
 SCANTIME=YES;
RUN;

PROC PRINT;
RUN;

PROC REG;
model y=x1/p clm cli;
RUN;
```

![[Linear Regression Assignment 2 Problem 2.4 a SAS Parameter output.png]]
SAS輸出結果如上，我們可以看到：
- $\beta_0$的估計值為$33.72744$，其p-value小於$0.0001$，遠小於顯著水準$0.05$，故我們有強烈的證據可以說，當引擎排量等於0的時候，預測的汽油里程的平均為$33.72744$英里/加侖。

- $\beta_1$的估計值為$-0.04743$，其p-value小於$0.0001$，遠小於顯著水準$0.05$，故我們有強烈的證據可以說，引擎排量每增加一單位，汽油里程平均會減少$0.04743$英里/加侖。
故我們可以知道，其簡單線性迴歸模型應為：
$$
y=33.72744-0.04743\times x_1
$$
### b
![[Linear Regression Assignment 2 Problem 2.4 a SAS ANOVA output.png]]
在SAS的OUTPUT中，我們可以看到他已經幫我們建構了一個ANOVA table。我們可以看到這個ANOVA table，最後得出來的p-value，其值是小於0.0001，故我們可以說我們有強烈的證據去說，引擎排量與汽油里程具有顯著的線性關係。
### c
![[Linear Regression Assignment 2 Problem 2.4 a SAS other output.png]]
在SAS的output裡面，我們可以看到引擎排量跟汽油里程建構的簡單線性迴歸，他的$R^2$為$0.772$。故我們可以知道說這個飲請排量與汽油里程的簡單線性迴歸模型可以解釋的
