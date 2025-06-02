# 問題：
In refernece to [[chapter 4 1.4|Exercise 1.4]]:
$$
f_{X,Y}(x,y)=\frac67\left(x^2+\frac{xy}{2}\right),\quad0<x\leq1,\, 0<y\leq 2
$$
calculate:
1. the marginal pdf's $f_X$,$f_Y$ and the conditional pdf $f_{Y\mid X}(\cdot\mid x)$; in all cases, specify the range of the variables involved.
2. $EY$ and $E(Y\mid X=x)$
3. $E[E(Y\mid X)]$ and observe that it is equal to EY
4. the probability $P(Y>\frac12\mid X<\frac12)$
# 回答：
##### 第一小題
$$
\begin{align}
f_X&=\int^2_0\frac67\left(x^2+\frac{xy}{2}\right)\,dy\\
&=\frac67\left(x^2y+\frac{xy^2}{4}\right)\bigg|^2_{y=0}\\
&=\frac67\left(2x^2+x\right)\\
&=\frac{12x^2}{7}+\frac{6x}{7}\\
&=\frac{12x^2+6x}{7}
\end{align}
$$
$$
f_X=\begin{cases}
\frac{12x^2+6x}{7},&0<x\leq1\\\\
0,x\leq0\,\,\text{or}\,\,x>1
\end{cases}
$$

$$
\begin{align}
f_Y&=\int^1_0\frac67\left(x^2+\frac{xy}{2}\right)\,dx\\
&=\frac67\left(\frac{x^3}{3}+\frac{x^2y}{4}\right)\bigg|^1_{x=0}\\
&=\frac67\left(\frac13+\frac y4\right)\\
&=\frac27+\frac{3y}{14}
\end{align}
$$
$$f_Y=
\begin{cases}
\frac27+\frac{3y}{14},&0<y\leq2\\\\
0,y\leq0\,\,\text{or}\,\,y>2
\end{cases}
$$

$$
\begin{align}
f_{Y\mid X}(\cdot\mid x)&=\frac{\frac67\left(x^2+\frac{xy}{2}\right)}{\frac{12x^2+6x}{7}}\\
&=\frac{\left(x^2+\frac{xy}{2}\right)}{2x^2+x}\\
&=\frac{\left(x+\frac{y}2\right)}{2x+1}\\
&=\frac{2x+y}{4x+2}\\
\end{align}
$$
$$
f_{Y\mid X}(\cdot\mid x)=
\begin{cases}
\frac{2x+y}{4x+2},&0<x\leq 1,\,\,0<y\leq2\\\\
0,&\text{otherwise}
\end{cases}
$$
##### 第二小題
$$
\begin{align}
E(Y)&=\int^2_0 y\,\cdot\,f_Y\,dy\\
&=\int^2_0y\cdot\frac{1}{14}\left(4+3y\right)\,dy\\
&=\frac{1}{14}\int^2_04y+3y^2\,dy\\
&=\frac{1}{14}\left(2y^2+y^3\right)\bigg|^2_{y=0}\\
&=\frac{8+8}{14}\\
&=\frac{8}{7}
\end{align}
$$
$$
\begin{align}
E(Y\mid X=x)&=\int^2_0 y\,\cdot\,\left(\frac{2x+y}{4x+2}\right)\,dy\\
&=\frac{1}{4x+2}\int^2_0 y\,\cdot\,(2x+y)\,dy\\
&=\frac{1}{4x+2}\int^2_02xy+y^2\,dy\\
&=\frac{1}{4x+2}\left(xy^2+\frac{y^3}{3}\right)\bigg|^2_{y=0}\\
&=\frac{1}{4x+2}\left(4x+\frac83\right)\\
&=\frac{4x+\frac83}{4x+2}\\
&=\frac{\frac{12x+8}{3}}{4x+2}\\
&=\frac{12x+8}{3(4x+2)}\\
&=\frac{12x+8}{12x+6}\\
&=\frac{6x+4}{6x+3},\quad 0<x\leq1
\end{align}
$$

##### 第三小題
題目要我們證明$E[E(Y\mid X)]=E(Y)$，那我們需要$E[E(Y\mid X)]$。可以參考一下[[chapter 4 2.5]]
$$
\begin{align}
E[E(Y\mid X)]&=\int^1_0 \frac{6x+4}{6x+3}\,\cdot\,f_X\,dx\\
&=\int^1_0\frac{6x+4}{6x+3}\,\cdot\,\frac{12x^2+6x}{7}\,dx\\
&=\int^1_0 6x\,\cdot\,\frac{6x+4}{6x+3}\,\cdot\,\frac{2x+1}{7}\,dx\\
&=\int^1_0 6x\,\cdot\,\frac{6x+4}{3}\,\cdot\,\frac{1}{7}\,dx\\
&=\int^1_0\frac{36x^2+24x}{21}\,dx\\
&=\frac{12}{21}\int^1_03x^2+2x\,dx\\
&=\frac{12}{21}\left(x^3+x^2\right)\bigg|^1_{x=0}\\
&=\frac{12}{21}(1+1)\\
&=\frac{24}{21}\\
&=\frac{8}{7}=E(Y)
\end{align}
$$
##### 第四小題
$$
\begin{align}
P\left(Y>\frac12\mid X<\frac12\right)=\int\int^2\frac{2x+y}{4x+2}\,dydx
\end{align}
$$