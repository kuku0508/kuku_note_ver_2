# 問題
Let X and Y be r.v's denoting, denoting, respectively, the number of cars and buses
lined up at a stoplight at a given point in time, and suppose their joint p.d.f. is
given by the following table:
![[table of chapter 4 1.1.png|400]]
Calculate the following probabilities:
(i) There are exactly four cars and no buses.
(ii) There are exactly five cars.
(iii) There is exactly one bus.
(iv) There are at most three cars and at least one bus.
- - -
# 答案
X是在給定的點紅燈時，車子的數量；Y是在給定的點紅燈時，巴士的數量。
##### (i)
要我們找出四輛車還有沒有巴士的機率，那我們就需要去看當今天 $f_{X,Y}(x=4,y=0)$的情況。
那我們可以看到在表格中，機率就是0.100。
##### (ii)
這邊問的是五輛車的機率，但沒有給巴士的數量，所以我們今天要考慮所有五輛車的情況，也就是$f_{X,Y}(x=5)$，包括0、1、2輛巴士。
所以我們就把0.05、0.03、0.02相加，即可得到答案為0.1。
##### (iii)
跟前一題一樣，就是把$x$改成$y$，找出$f_{X,Y}(y=1)$的情況。
所以我們就把0.015、0.03、0.075、0.09、0.06、0.03相加，得到答案為0.3。
##### (iv)
這次要找的是最多3輛車，至少1輛巴士的情況，也就是$f_{X,Y}(x\leq3,y\geq1)$。
所以就是將0.015、0.03、0.075、0.09、0.01、0.02、0.05、0.06加總，得到答案為0.35。