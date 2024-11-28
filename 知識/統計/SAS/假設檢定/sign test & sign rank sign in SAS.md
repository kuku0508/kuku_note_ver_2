處理事件：[[單樣本符號檢定]]、[[魏克森符號等級檢定]]
使用的Procedure：[[UNIVARIATE]]
- - -
# 範例：
今天kuku建造了一條產線生產處理器，
``` SAS
/*建立資料集*/
data d1;
/*辨識變數*/
input X @@;
/*輸入資料*/
card;
180 185 195 190 185 195 195 200
;
/*開始用Procedure UNIVARIATE & 設定假設檢定的中位數*/
PROC UNIVARIATE Mu0=180;
 VAR X;
RUN;
```
`PROC UNIVARIATE`
`Mu0`：sign test的假設的中位數。
`VAR`：要進行UNIVARIATE的變數。
- - -
# 結果
![[SAS output of sign test and Wilcoxon sign rank test.png]]
- - -
parent::[[魏克森符號等級檢定]],[[單樣本符號檢定]],[[SAS目錄]]