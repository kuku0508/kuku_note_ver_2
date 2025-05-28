# 問題：
The joint pdf of the r.v's $X$ and $Y$ is given by:
$$
f_{X,Y}(x,y)=xy^2\,,\,0<x\leq c_1,\,0<y\leq c_2
$$
Determine the condition that $c_1$ and $c_2$ must satisfy so that $f_{X,Y}$ is, indeed, a pdf.
# 回答：
確定是pdf了，所以積分結果要為1。
然後有函數了，知道積分範圍了，開始積分。
$$
\begin{align}
\int^{c_2}_0\int^{c_1}_0 xy^2\,dxdy&=\int^{c_2}_0y^2\int^{c_1}_0x\,dxdy\\
&=\int^{c_2}_0y^2\left(\frac12 x^2\right)\bigg|^{c_1}_{x=0}\,dy\\
&=\int^{c_2}_0\frac12 c_1^2\cdot y^2\,dy\\
&=\frac12 c_1^2\int^{c_2}_0y^2\,dy\\
&=\frac12 c_1^2\left(\frac13y^3\right)\bigg|^{c_2}_{y=0}\\
&=\frac{1}{6}c^2_1c^3_2\\
&\Rightarrow
\end{align}
$$
