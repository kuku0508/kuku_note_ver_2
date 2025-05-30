# 問題：
The joint pdf of the r.v's $X$ and $Y$ is given by：
$$
f_{X,Y}(x,y)=cx,\quad x>0,\quad y>0,\quad 1\leq x+y<2\quad (c>0)
$$
Determine the constant c.
**Hint.** The above diagram should facilitate the calculations. The range of the pair (x,y) is the shadowed area.
![[plot of 1.10.png|400]]
# 回答：
這題比較麻煩一點，我們看圖會比較好理解。
當我們今天在積分的時候，我們需要知道定義域，但這題的定義域會比較麻煩一點。
我們可以看到上圖，會有$x+y=2$跟$x+2=1$是因為$1\leq x+y<2$這個限制式。我們所要求的範圍就是圖中的陰影區域。

在$0<x<1$這個範圍，y的上界會是$x+y=2$，而下界會是$x+y=1$。其實就是題目限制式告訴我們的$1\leq x+y<2$，我們稍微改寫一下，會變成$2-x<y<1-x$。

而在$1<x<2$這個部分，就會有一點不同。我們可以看到x+y=1已經到第四象限了，但題目又要求我們$x>0;y>0$。所以我們這邊就需要再做另外一個積分，讓我們得到正確的積分範圍的結果。我們可以很明顯的看到下界都是0，而上界還是$y=2-x$。

所以從上面的結論我們可以知道我們的積分會變成這樣：
$$
\begin{align}
\iint_Dcx\,dxdy&=\left(\int^1_0\int^{2-x}_{1-x}cx\,dydx\right)+\left(\int^2_1\int^{2-x}_0cx\,dydx\right)\\
&=\left(\int^1_0cxy\bigg|^{2-x}_{y=1-x}\,dx\right)+\left(\int^2_1cxy\bigg|^{2-x}_{y=0}\,dx\right)\\
&=\left(\int^1_0cx\,dx\right)+\left(\int^2_1cx(2-x)\,dx\right)\\
&=\left(\int^1_0cx\,dx\right)+\left(\int^2_12cx-cx^2\,dx\right)\\
&=\left(\frac{cx^2}{2}\bigg|^{1}_{x=0}\right)+\left(cx^2-\frac{cx^3}{3}\bigg|^2_{x=1}\right)\\
&=\frac{c}{2}+\left[\frac{12c-8c}{3}-\left(\frac{3c-c}{3}\right)\right]\\
&=\frac{3c}{6}+\frac{4c}{6}\\
&=\frac{7c}{6}\\
&\Rightarrow\frac{7c}{6}=1\\
&\Rightarrow c=\frac67
\end{align}
$$
