---
參考資料:
---
RUN，是比較特別的[[SAS敘述句]]。當我們今天在SAS的[[datastep]]或[[procedures]]的任何地方放了RUN這個敘述句。SAS系統便會開始執行RUN之前的敘述句。執行完所有敘述句之後，再繼續執行接下來的敘述句。
- - -
```SAS
data d1;
input x1 x2;
card;
1 2
3 2
5 1
2 3
5 2
;
proc print;
run;/* 執行前面的所有敘述句*/
```
- - -
parent::[[SAS敘述句]]
sibling::
child::