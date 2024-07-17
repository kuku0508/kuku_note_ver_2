cumulative hazard function(累積危險函數)，通常用H(t)表示，即危險函數的cdf。表示在時間t時的累積危險函數。
- - -
# 公式：
$$H(t)=\int^t_0 h(u)du$$
- - -
# 性質：
$$
\begin{align}
&h(t)=\frac{-d}{dt}\ln S(t)\\
\Rightarrow& H(t)=-\ln S(t)\\
\Rightarrow &S(t)=exp\left\lbrace-H(t)\right\rbrace
\end{align}
$$
- - -
parent::[[Hazard function]],[[常用符號目錄]]