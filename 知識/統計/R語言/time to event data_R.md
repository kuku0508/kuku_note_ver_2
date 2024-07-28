這份筆記會帶著你來透過R建構time to event data。
- - -
# 函數說明：
``` r
Surv(time,time2,event,type=("right","left","interval","mstate"))
```
- `time`：對於右設限函數，這是追蹤時間。對於區間設限數據，第一個參數是區間的起始時間。
- `time2`：對於區間設限數據，這是區間的結束時間。
- `event`：表示事件發生狀態，通常0=右設限，1=事件發生，2=左設限，3=區間設限
- `type`：整體數據的設限類型，幫助`surv`函數正確解數`event`參數的訊息。
	- `right`：右設限
	- `left`：左設限
	- `interval`：區間設限
	- `mstate`：多狀態
- - -
# 細節補充：
- 若一份資料中存在多種設限類型，則在`type`中可以使用`matate
- `