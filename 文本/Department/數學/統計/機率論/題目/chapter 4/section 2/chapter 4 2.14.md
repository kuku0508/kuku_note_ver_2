# 問題：
In reference to [[chapter 4 1.8]], determine the marginal pdf of $f_Y$ and the conditional pdf of $f_{X\mid Y}(\cdot\mid y)$.
$$
f_{X,Y}(X,Y)=\frac{1}{\sqrt{2\pi}}ye^{-xy/2},\quad0<y<x.
$$
# 回答：
$$
\begin{align}
f_Y&=\int^\infty_y \frac{1}{\sqrt{2\pi}}ye^{-xy/2}\,dx\\
&=\frac{1}{\sqrt{2\pi}}y\int^\infty_y e^{-xy/2}\,dx\\
&=\frac{1}{\sqrt{2\pi}}y\left(-\frac{2}{x}e^{-xy/2}\right)\bigg|^\infty_{x=y}\\
&=\frac{1}{\sqrt{2\pi}}y\left(\frac{2}{y}e^{-y^2/2}\right)\\
&=\frac{2e^{-y^2/2}}{\sqrt{2\pi}}
\end{align}
$$
$$
f_Y=
\begin{cases}
\frac{2e^{-y^2/2}}{\sqrt{2\pi}},&0<y\\\\
0,&\text{otherwise}
\end{cases}
$$

$$
\begin{align}
f_{X\mid Y}(\cdot\mid y)&=\frac{f_{X,Y}(x,y)}{f_Y}\\
&=\frac{\frac{1}{\sqrt{2\pi}}ye^{-xy/2}}{\frac{2e^{-y^2/2}}{\sqrt{2\pi}}}\\
&=\frac{ye^{-xy/2}}{2e^{-y^2/2}}\\
&=\frac y2 e^{(-xy/2 \,\,+y^2/2)}
\end{align}
$$
$$
\begin{cases}
\frac y2 e^{(-xy/2 \,\,+y^2/2)},&0<y<x\\\\
0,&\text{otherwise}
\end{cases}
$$