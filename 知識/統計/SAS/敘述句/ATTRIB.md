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
簡單來說就是，他就是將許多個敘述句可以做到的事情整合到了一個敘述句上面，讓你可程式碼可以更簡潔一點。
- - -
# 基本語法
```SAS
ATTRIB 變數名稱
		FORMAT=輸出格式
		INFORMAT=輸入格式
		LABEL="標籤文字"
		LENGTH=($)儲存長度;
```
其中
FORMAT：指定輸出時的顯示格式，不影響變數在資料集的實際儲存值。
INFORMAT：定義輸入時的格式
LABEL：定義變數的標籤
LENGTH：定義變數儲存的長度
- - -
# 範例
```SAS
DATA D1;
	INPUT id name$ sex$ score1-score3;
	average=(score1+score2+score3)/3;
	LENGTH mark$6;
	IF average >=60 then mark="及格";
	IF average<60 then mark="不及格";
	LABEL id="學號" name="姓名" sex="性別" score1="平時成績" score2="期中成績" 
			score3="期末成績";
	FORMAT average 5.2;
CARDS;
123456789 Ameria F 100 96 95
123456790 Gura F 70 66 79
123456791 kuku M 80 92 90
123456792 Ina F 100 95 96
123456793 calli F 80 83 79
;
PROC PRINT;
RUN;
```
上面的程式碼用到了`LENGTH`、`LABEL`、`FORMAT`三個敘述句來定義變數，而我們完全可以用`ATTRIB`來替代這三個敘述句。改成下面的程式碼：
```SAS
DATA C1;
	ATTRIB
	id 
		LABEL ="學號"
	name
		LABEL="姓名"
	sex
		LABEL="性別"
	score1
		LABEL="平時成績"
	score2
		LABEL="期中成績"
	score3
		LABEL="期末成績"
	mark
		LABEL="備註"
		LENGTH =$6
	average
		LABEL="學期總成績"
		FORMAT=5.2;
	INPUT id name$ sex$ score1-score3;
	average=(score1+score2+score3)/3;
	IF average >=60 then mark="及格";
	IF average<60 then mark="不及格";
CARDS;
123456789 Ameria F 100 96 95
123456790 Gura F 70 66 79
123456791 Kuku M 80 92 90
123456792 Ina F 100 95 96
123456793 Calli F 80 83 79
123456794 Jarry M 10 0 5
;
PROC PRINT DATA=C1 LABEL;
RUN;
```

- - -
parent::[[SAS敘述句]],[[變數]]
sibling::[[FORMAT]],[[INFORMAT]],[[LABEL]],[[LENGTH]]
child::