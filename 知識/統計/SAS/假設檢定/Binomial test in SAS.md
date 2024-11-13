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
	`F 14`：F的出現次數為14
`PROC FREQ`：生成次數分配表和進行統計檢定。
	`ORDER=DATA`：指定變數的類別順序按照資料輸入的順序進行，這樣根據`cards`，`S`和`F`會按照輸入順序排列。
`WEIGHT`：將`COUNT`視為次數的變數。這樣就可以正確地計算S的次數跟F的次數。
