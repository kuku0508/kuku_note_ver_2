# 問題：
In reference to [[chapter 4 1.7]], 
$f_{X,Y}=2/c^2$, for $0<x\leq y < c$
calculate:
1. the marginal pdf of $f_X$ and $f_Y$.
2. the conditional pdf of $f_{X\mid Y}(\cdot\mid y)$ and $f_{Y\mid X}(\cdot\mid x)$.
3. the probability $P(X\leq1)$.
# 回答：
##### 第一小題
把c視為常數就好了
$$
\begin{align}
f_X&=\int^c_x\frac{2}{c^2}\,dy\\
&=\frac{2}{c^2}y\bigg|^c_{y=x}\\
&=\frac2c-\frac{2x}{c^2}\\
&=\frac{2c-2x}{c^2}
\end{align}
$$
$$
f_X(x)=
\begin{cases}
\frac{2c-2x}{c^2},&0<x<c\\\\
0,&\text{otherwise}
\end{cases}
$$

$$
\begin{align}
f_Y&=\int^y_0\frac{2}{c^2}\,dx\\
&=\left(\frac{2}{c^2}x\right)\bigg|^y_{x=0}\\
&=\frac{2}{c^2}y
\end{align}
$$
$$
f_Y=
\begin{cases}
\frac{2}{c^2}y,&0<y<c\\\\
0,&\text{otherwise}
\end{cases}
$$
##### 第二小題
$$
\begin{align}
f_{X\mid Y}(\cdot\mid y)=\frac{f_{X,Y}(x,y)}{f_Y}=\frac{\frac{2}{c^2}}{\frac{2}{c^2}y}=\frac{1}{y}
\end{align}
$$
$$
f_{X\mid Y}(\cdot\mid y)=
\begin{cases}
\frac1y,&0<x\leq y<c\\\\
0,&\text{otherwise}
\end{cases}
$$

$$
f_{Y\mid X}(\cdot\mid x)=\frac{f_{X,Y}(x,y)}{f_X}=\frac{\frac{2}{c^2}}{\frac{2}{c^2}(c-x)}=\frac{1}{c-x}
$$
$$
f_{Y\mid X}(\cdot\mid x)=
\begin{cases}
\frac{1}{c-x},&0<x\leq y<c\\\\
0,&\text{otherwise}
\end{cases}
$$
##### 第三小題
$$
\begin{align}
 P(X\leq1)&=\int^1_0\frac{2c-2x}{c^2}\,dx\\
 &=\int^1_0\frac{2}{c^2}(c-x)\,dx\\
 &=\frac{2}{c^2}\int^1_0c-x\,dx\\
 &=\frac{2}{c^2}\left(cx-\frac{x^2}{2}\right)\bigg|^1_{x=0}\\
 &=\frac{2}{c^2}\left(c-\frac{1}{2}\right)\\
 &=\frac2c-\frac{1}{c^2}
\end{align}
$$
