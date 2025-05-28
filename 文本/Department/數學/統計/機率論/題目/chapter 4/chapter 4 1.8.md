# 問題：
The r.v's $X$ and $Y$ have the joint pdf $f_{X,Y}$ given by:
$$
f_{X,Y}(X,Y)=cye^{-xy/2},\quad0<y<x.
$$
Determine the constant c.
# 回答：
 這種題目，我們一樣用積分的方式，得到未知數的方法。
 當我們對pdf的定義域積分之後，我們就會得到1這個結果（必然事件）。

但這個題目比較特別，在積分之前，我們可看到，如果我們先積分y，我們會遇到要積分$ye^{-\frac{xy}2}$的情況。但這樣會比較不好積分，所以我們這邊可以先對x積分。接下來再對y積分，通常會比較簡單積分。
$$
\begin{align}
\int^{\infty}_0 \int^\infty_y cye^{-xy/2} \,dxdy&=\int^\infty_0 cy\int^\infty_y e^{-xy/2}\,dxdy\\
&=\int^\infty_0cy\left(\frac{-2}{y}e^{-xy/2}\right)\bigg|^\infty_{x=y}\,dy\\
&=\int^\infty_02ce^{-y^2/2}\,dy\\
&=2c\int^\infty_0e^{-y^2/2}\,dy\\
&=2c\left(\frac12\sqrt{2\pi}\right)\\
&=c\sqrt{2\pi}\\
&\Rightarrow c\sqrt{2\pi}=1\\
&\Rightarrow c=\frac{1}{\sqrt{2\pi}}
\end{align}
$$

P.S：你可以看到上面有一個指數函數的積分，是$e^{-y^2/2}$，這個東西跟一般的指數積分不太一樣，他是[[高斯積分]]，得到的結果跟一般的指數函數截然不同。建議讀一下[[高斯積分]]的筆記。