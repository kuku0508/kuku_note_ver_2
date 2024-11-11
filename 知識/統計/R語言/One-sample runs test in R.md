處理事件：[[One-sample runs test]]
需安裝的套件：[[randtests]]

# 連續型資料
``` R
# 安裝套件randtest
install.packages("randtests")
# 載入套件randtest
library("randtests")
# 輸入樣本（定義sample為向量）
sample<-c(12,13,12,11,5,2,-1,2,-1,3,2,-6,-7,-7,-12,-9,6,7,10,6,1,1,6,7,-2,-6,-6,-5,-2,-1)
# 進行One-sample runs test
runs.test(temp,threshold=0)
```

`runs.test(資料,threshold=門檻值)`，
所謂門檻值就是當數據大於某個值，他是類別1；小於某個值，他是類別2。
如果等於門檻值，R會直接無視那筆數據。



而今天R使用的檢定統計量是以最多runs，的情況
- - -
parent::[[randtests]],[[One-sample runs test]]
