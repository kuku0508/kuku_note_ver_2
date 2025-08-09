---
參考資料: 
屬於環節:
  - "[[datastep]]"
  - "[[procedures]]"
---
ATTRIB是一種[[SAS敘述句]]，這個比較是一個整合型的敘述句，他可以定義[[變數]]的：
- 輸出格式（[[FORMAT]]）
- 輸入格式（[[INFORMAT]]）
- 標籤（[[LABEL]]）
- 儲存位元組（[[LENGTH]]）
- - -
# 基本語法
```SAS
ATTRIB 變數名稱
		[FORMAT=輸出格式]
		[INFORMAT=輸入格式]
		[LABEL=輸出格式]
		[LENGTH=[$]儲存長度];
```
其中
FORMAT：指定輸出時的顯示格式，不影響變數在資料集的實際儲存值。
INFORMAT：定義輸入時的格式
LABEL：定義變數的標籤
LENGTH：定義變數儲存的長度
- - -
parent::[[SAS敘述句]],[[變數]]
sibling::[[FORMAT]],[[INFORMAT]],[[LABEL]],[[LENGTH]]
child::