# 問題：
The r.v's $X$ and $Y$ have the joint pdf $f_{X,Y}$ given by:
$$
f_{X,Y}(X,Y)=cye^{-xy/2},\quad0<y<x.
$$
Determine the constant c.
# 回答：
 這種題目，我們一樣用積分的方式，得到未知數的方法。
 當我們對pdf的定義域積分之後，我們就會得到1這個結果（必然事件）。

所以我們就先去定義積分範圍，我自己的習慣是，我會把0當下界，另外一個隨機變數當成上界，在這個題目裡面，就會是Y的上界要是X，下界是0，範圍就會是
$$
Y\in(0,x)
$$
因為我們已經處理好Y的範圍問題，接下來在處理X的時候，我們就不用考慮Y。所以X的上界會是$\infty$，下界會是0。
$$
X\in(0,\infty)
$$
最後我們就可以開始積分了，但我們可以看到如果我們先積分y，那我們就會遇到$y\cdot e^{-xy/2}$，這種比較麻煩的積分。所以當我們遇到這種比較麻煩的積分時，又找不到辦法可不可以讓這個變得比較好積分，那我建議可以從另外一個積分。可能可以解決問題。
$$
\begin{align}
\int^\infty_0 \int^x_0 cye^{-xy/2} \,dxdy&=\int^\infty_0 cy\int^{x}_0e^{-xy/2}\,dxdy\\
&=\int^\infty_0cy\left(-\frac{2}{y}e^{-xy/2}\right)^x
\end{align}
$$