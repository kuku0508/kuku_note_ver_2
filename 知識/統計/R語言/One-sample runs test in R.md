處理事件：[[One-sample runs test]]
需安裝的套件：[[randtests]]

``` R
# 安裝套件randtest
install.packages("randtests")
# 載入套件randtest
library("rantests")
# 輸入樣本（定義sample為向量）
sample<-c(12,13,12,11,5,2,-1,2,-1,3,2,-6,-7,-7,-12,-9,6,7,10,6,1,1,6,7,-2,-6,-6,-5,-2,-1)
# 進行One-sample runs test
runs.test(temp,threshold=0)
```
