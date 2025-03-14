處理事件：[[單樣本符號檢定]]、[[魏克森符號等級檢定]]
使用的Procedure：[[UNIVARIATE]]
- - -
# 範例：
今天kuku建造了一條產線生產處理器。而我們以五分鐘為單位，進行了8次生產，數量分別為：180、185、195、190、185、195、195、200。試問，這條產線在五分鐘內生產處理器的母體中位數，是否等於180個。
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
我們可以看到不論是在[[單樣本符號檢定|Sign test]]或是在[[魏克森符號等級檢定|Wilcoxon signed-ranks test]]的P-value，都是遠大於0.1，故我們不拒絕虛無假設，我們沒有足夠的證據去證明，kuku建造的產線，在五分鐘內生產的處理器數量之中位數不等於180。
- - -
parent::[[魏克森符號等級檢定]],[[單樣本符號檢定]],[[SAS目錄]]