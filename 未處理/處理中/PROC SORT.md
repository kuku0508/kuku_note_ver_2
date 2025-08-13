---
參考資料: 
屬於環節:
---
PROC SORT，是一種SAS的[[procedures]]。我們主要可以透過PROC SORT來對資料集的特定變數進行排序。
- - -
# 基本語法
```SAS
PROC SORT (第一參數=);
	BY (DESCENDING) 變數1 (DESCENDING) 變數2......;
RUN;
```

#### 第一參數

| 參數名稱 | 功能            |
| ---- | ------------- |
| DATA | 指定要排序的資料集     |
| OUT  | 指定產生排序後結果的資料集 |

- `DESCENDING`：指定

- - -
parent::[[SAS敘述句]]
sibling::
child::