# 問題
In a sociological project, families with 0, 1, and 2 children are studied.
Suppose that the numbers of children occur with the following frequencies:
$$
\text{0 children}:30\%;\quad\text{1 child}:40\%;\quad\text{2 children}:30\%;
$$
Let X and Y be the r.v.’s denoting the number of children in a family from the
target population and the number of boys among those children, respectively.
Finally, suppose that P(observing a boy) = P(observing a girl) = 0.5.
Calculate the joint p.d.f. $f_{X,Y}(x, y) = P(X = x, Y = y), 0 ≤ y ≤ x$, $x = 0, 1, 2$.
Hint. Tabulate the joint probabilities as indicated below by utilizing the
formula:
$$
P(X=x,Y=y)=P(Y=y\mid X=x)P(X=x)
$$

# 答案

確定一下題目條件，$f_{XY}(X=x,Y=y)$，X是家庭中小孩的數量，Y是家庭中男孩的數量。
$f_{X,Y}(X=0)=0.3$、$f_{X,Y}(X=1)=0.4$、$f_{X,Y}(X=2)=0.3$，$P(生男生的機率)=P(生女生的機率)=0.5$。叫我們填聯合機率密度的表格。

我們可以先把一些簡單的格子填起來，$f_{X,Y}(X=0,Y=0)$，我們可以知道，當今天家庭沒有小孩的時候，就不會有男孩，所以$f_{X,Y}(X=0,Y=0)=f_{X,Y}(X=0)=0.3$。
且$f_{X,Y}(X=0,Y=1)=f_{X,Y}(X=0,Y=2)=0$

| x\y | 0   | 1   | 2   |
| --- | --- | --- | --- |
| 0   | 0.3 | 0   | 0   |
| 1   |     |     |     |
| 2   |     |     |     |
然後我們試著填完第二列，我們會發現，跟上面一樣，只有一個小孩的情況，不可能會有2個男孩，所以我們可以把$f_{X,Y}(X=1,Y=2)=0$。
$f_{X\mid Y}(X=1\mid Y=y)$我們可以用二項分配來做
$f_{X\mid Y}(X=1\mid Y=0)=C^1_0\times 0.5^{0}\times0.5^{1-0}=$

| x\y | 0   | 1   | 2   |
| --- | --- | --- | --- |
| 0   | 0.3 | 0   | 0   |
| 1   |     |     | 0   |
| 2   |     |     |     |
