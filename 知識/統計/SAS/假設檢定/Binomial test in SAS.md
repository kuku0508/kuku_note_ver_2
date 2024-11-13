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
	`event $`：這個是表示結果的變數，通常我會用S（Success）跟F（Fail）來表示。
`cards`：
	`S 11`：S的出現次數為11
	