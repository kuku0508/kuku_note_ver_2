---
參考資料:
---
procedures，簡單來說是[[SAS]]中用來分析、處理或著輸出資料的程式碼區塊。
當我們今天已經有了[[資料集]]（通常是透過[[datastep]]建立的），SAS會透過各種PROC指令來進行運算、分析、圖形繪製或資料管理。

在執行一個`PROCstep`時，SAS會呼叫對應的內建程序（procedures），並依照使用者設定的選項以及參數，讀取資料集並產生結果。這些輸出可能是表格、統計檢定結果、圖形或是新的資料集。
- - -
# 常用的程序

#### 資料管理
- [[PROC SORT]]：資料排序
- [[PROC PRINT]]：顯示資料內容
- [[PROC TRANSPOSE]]：資料轉置
- [[PROC DATASETS]]：管理資料集（刪除、修改變數之類的）
#### 統計分析
- [[PROC MEANS]]：計算描述統計量（平均數、變異數、最大最小值之類的）
- [[PROC FREQ]]：計算次數分配與交叉表
- [[PROC TTEST]]：t檢定
- [[PROC ANOVA]]：變異數分析
- [[PROC REG]]：線性迴歸分析
- [[PROC CORR]]：相關係數計算
- [[PROC GLM]]：廣義線性模型分析
#### 圖形輸出
- [[PROC SGPLOT]]


- - -
parent::[[SAS]],[[資料集]],[[datastep]]
sibling::
child::