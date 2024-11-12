處理事件：[[單樣本符號檢定]]、[[魏克森符號等級檢定]]
使用的Procedure：[[UNIVARIATE]]
- - -
# 範例：
有一組資料，變數為
``` SAS
/*建立資料集*/
data d1;
/*辨識變數*/
input X @@;
/*輸入資料*/
card;
180 185 195 190 185 195 195 200
;
/*開始用Procedure UNIVARIATE & 設定假設檢定的μ*/
PROC UNIVARIATE Mu0=180
```