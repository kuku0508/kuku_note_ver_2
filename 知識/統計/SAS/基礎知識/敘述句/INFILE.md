---
參考資料:
---
INFILE，是一種[[SAS敘述句]]，專門用來讀取SAS外部的[[資料]]。屬於[[datastep]]使用的敘述句。常見可以讀取的資料有CSV、TXT、DAT，只要內容是文字格式就能讀。

而為了讓讀取的資料的變數被定義，通常會搭配[[INPUT]]使用。
- - -
# 基本語法
```SAS
INFILE "外部檔案路徑";
```
- - -
# 常用參數
- `FIRSTOBS`：從第幾個觀測值開始讀取資料
- `OBS`：最多讀幾個觀測值
- `DLM`：指定欄位分隔符號（預設為空白）
- `MISSOVER`：如果該行不足INPUT欄位，將缺值設為空值，而不繼續跳到下一行。
- - -
# 範例
```SAS
DATA d1;
INFILE "C:\SAS\sales_2025.txt" /*外部檔案在C槽的SAS資料夾裡*/
   dlm=';'  /*資料用 ; 來分隔變數*/
   firstobs=2 /*從第二行開始讀取*/
   obs=100 /*讀取一百個觀測值*/
INPUT X1 X2;
RUN;
```
- - -
parent::[[SAS敘述句]],[[資料]]
sibling::[[INPUT]]
child::