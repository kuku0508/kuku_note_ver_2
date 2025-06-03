# 問題：
Show that the joint mgf of two r.v of $X$ and $Y$ satisfies the following property, where $c_1$, $c_2$, $d_1$ and $d_2$ are constants.
$$
M_{c_1X+d_1,c_2Y+d_2}(t_1,t_2)=e^{d_1t_1+d_2t_2}M_{X,Y}(c_1t_1,c_2t_2).
$$
# 回答：
$$
\begin{align}
M_{c_1X+d_1,c_2Y+d_2}(t_1,t_2)&=E(e^{t_1(c_1X+d_1)+t_2(c_2Y+d_2)})\\
&=E(e^{t_1c_1X+d_1t_1+t_2c_2Y+t_2d_2})\\
&=E(e^{d_1t_1+d_2t_2}\,\cdot\,e^{t_1c_1X+t_2c_2Y})\\
&=e^{d_1t_1+d_2t_2}\,\cdot\,E(e^{t_1c_1X+t_2c_2Y})\\
&=e^{d_1t_1+d_2t_2}\,\cdot\,M_{X,Y}(c_1t_1,c_2t_2)
\end{align}
$$
