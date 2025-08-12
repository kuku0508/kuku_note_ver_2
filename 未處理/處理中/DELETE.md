---
參考資料: 
屬於環節:
  - "[[datastep]]"
---
DELETE，是一種[[SAS敘述句]]。可以用來刪除觀測值。倘若觀測值被刪除，則不會出現在輸出的資料集中。
- - -
# 基本語法

通常DELETE會搭配`IF`來一起使用。
```SAS
IF 條件 THEN DELETE;
```
表示，如果觀測值符合條件的話，則刪除觀測值。
- - -
# 備註
- 倘若只有`DELETE`作為敘述句
- - -
parent::
sibling::
child::