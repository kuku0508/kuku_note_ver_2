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
- 若一份資料中存在多種設限類型，則在參數`type`中可以使用`matate`
- 當缺少參數`type`時，R會根據以下規則假設一個類型：
	- 如果有兩個無名參數，他們將被視為`time`跟`event`。
	- 如果有三個無名參數，他們將被視為`time`、`time2`跟`event`。
	- 如果參數`event`是一個因子，則`type`將假設為`mstate`。
	- 如果沒有參數`time2`，則`type`將假設為`right`。
- 當`type`被省略時，`mstate`狀態將作為一個因子，因子的第一個level表示設限，其餘level表示過渡到給定的狀態。
- 區間設限數據有兩種方式可以表示：
	- 第一種方式使用`type="interval"`，在這種情況下，參數`time2`將被忽略，除非`event=3`
	- 第二種方法是將每個觀測值視為一個時間區間，例如($-\infty\,,\,t_2$)表示