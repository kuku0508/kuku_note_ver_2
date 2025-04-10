處理事件：[[二項檢定]]
使用的Procedure：[[FREQ]]

# 範例
今天想要調查皮爾托福中，有多少人在追思會的襲擊中被攻擊並受傷。隨機抽樣25位出席追思會的民眾，其受傷人數11人，未受傷人數14人。試問，在追思會中有受傷民眾的比例是否會超過0.27。

- - -
# 輸入
```SAS
DATA d1;
input event $ count;
cards;
S 11
F 14
;
PROC FREQ DATA = d1 ORDER = data;
	WEIGHT COUNT;
	TABLE event/BINOMIAL(P=0.27);
	EXACT BINOMIAL;
RUN;
```
`input`：定義變數
	`event $`：這個是表示結果的變數，通常我會用S（Success）跟F（Fail）來表示。務必使用類別變數。
`cards`：
	`S 11`：S的出現次數為11
	`F 14`：F的出現次數為14
`PROC FREQ`：指定使用Procedure [[FREQ]]。
	`ORDER=DATA`：指定變數的類別順序按照資料輸入的順序進行，這樣根據`cards`，`S`和`F`會按照輸入順序排列。
`WEIGHT`：將`COUNT`視為次數的變數。這樣就可以正確地計算S的次數跟F的次數。
`TABLE event`：製作變數`event`的次數分配表
`/BINOMIAL(P=0.27)`：這邊是在對變數`event`(前面指定的)，做二項檢定，且將假設的比例設為0.27。
`EXACT BINOMIAL`：讓你對變數`event`做二項檢定。
- - -
# 輸出
![[binomial test sas output.png]]]
我假設的比例忘記打了，所以它顯示是0.5，但是其實你可以自己設定。
- - -
# 注意
你可能發現了，有兩個指令都是在做二項檢定，分別是在`TABLE`後面的`/BINOMIAL(P=0.27)`跟`EXACT BINOMIAL`，這兩個的確都在做二項檢定，差別只在於如果你沒有打`EXACT BINOMIAL`，只打了`/BINOMIAL`，那最後跑出來的OUTPUT，檢定統計量只會有近似常態的檢定值，而沒有用binomial test。
妳也可以只打後面的`EXACT BINOMIAL`，他還是會出現近似常態的檢定統計量，只是你就不能設定他的假設比例（預設是0.5）。
至於要用哪一個檢定統計量，請見[[二項檢定]]。
- - -
parent::[[SAS目錄]],[[二項檢定]],[[FREQ]]