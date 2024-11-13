處理事件：[[二項檢定]]
使用的Procedure：[[FREQ]]
```SAS
DATA d1;
input event $ count;
cards;
S 11
F 14;
PROC FREQ ORDER = d1;
	WEIGHT COUNT;
	TABLE event/BINOMIAL(P=0.27);
	EXACT BINOMIAL;
RUN;
```
`input`：定義變數
	`event $`：這個表示節ㄍㄨㄛ