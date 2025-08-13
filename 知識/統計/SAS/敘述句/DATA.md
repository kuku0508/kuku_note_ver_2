---
參考資料: 
屬於環節: "[[datastep]]"
---
DATA，是一個[[SAS敘述句]]，專門用來建立一個新的[[資料集]]。
- - -
# 基礎語法
``` SAS
DATA 資料集名稱;
```

- 當我們今天要建立[[永久性資料集]]時，我們可以在資料集名稱前面加上「[[資料館指引]].」就可以建立。若只有資料集名稱，則會建立[[暫時性資料集]]
- 可以將欲產生的永久性資料集名稱與路徑直接寫在DATA後面，即可以建立永久性資料集。
- 若沒有給資料集名稱，系統則會自動給予不同的名稱，「DATAi」$i=1,2,\cdots n$
- - -
# 範例
**建立一個名稱為d1的暫時性資料集：**
```SAS
DATA d1;
input x1 x2;
card;
1 2
3 4
5 6
7 8
;
RUN;
```

**建立一個名稱為d1的永久性資料集：**
方法一：使用資料館指引
```SAS
LIBNAME kuku "C:\Users\kuku\download";
DATA kuku.d1;
input x1 x2;
card;
1 2
3 4
5 6
7 8
;
RUN;
```
方法二：直接使用路徑
```SAS
DATA "C:\Users\kuku\download\d1";
input x1 x2;
card;
1 2
3 4
5 6
7 8
;
RUN;
```
- - -
parent::[[SAS敘述句]],[[資料集]]
sibling::
child::