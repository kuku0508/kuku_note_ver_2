# 問題：
Let $X$ and $Y$ be r.v.'s jointly distributed with pdf $f_{X,Y}=2/c^2$, for $0<x\leq y < c$.
Determine the constant c .
# 回答：
這種題目反正我們知道pdf是$2/c^2$，我們只要對她積分，然後積分結果必須要是1，我們就可以透過解未知數的方式，來知道c是多少。
而我們也有pdf的定義域了，所以我們就直接積分
$$
\begin{align}
\int^{c}_{0} \int^{y}_{0} \frac{2}{c^2} \,dxdy&=\int^c_0\frac2{c^2}\int^y_01\,dxdy\\
&=\int^c_0\frac2{c^2}y\,dy\\
&=\frac2{c^2}\int^c_0y\,dy\\
&=\frac{2}{c^2}\left(\frac {y^2}2\right)\bigg|^{c}_{y=0}\\
&=\frac{2}{c^2}\cdot\frac{c^2}{2}\\
&=\frac{c^2}{c^2}=1
\end{align}
$$
因為最後我們發現積分結果自己就等於1了，所以我們可以知道c可以是任意實數，但因為原本的pdf的定義域限制$c>0$，所以c其實是任意正數。

