---
參考資料:
---
KEEP，是一種[[SAS敘述句]]。我們可以利用他選擇我們要把哪些變數留在資料集中。
- - -
# 基本語法
```SAS
KEEP 變數名稱1 變數名稱2 ......;
```
- - -
# 範例
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
例如我們現在有一個資料集C1有學生的「學號」、「姓名」、「平時成績」、「期中成績」、「期末成績」、「學期總成績」以及「備註」。

而為了要項同學公布成績，且保護隱私，我們想要只保留學號、各項成績以及備註。那我們就可以利用KEEP：
```SAS
data score_without_name;

```
- - -
parent::
sibling::
child::