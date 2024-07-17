Survival Function(存活函數)，通常以S(t)表示。是指時間t觀察對象依然存活的機率。
- - -
公式表示：
$$
\begin{align}
&S(t)\\
=&P(T>t)\\
=&1-P(T\leq t)\\
=&1-F(t)
\end{align}
$$
- - -
特性：
1. $0\leq S(t)\leq 1$
2. monotone decreasing as t $\uparrow$
3. $$f(t)=\frac{-ds(t)}{dt}$$
4. 在$t=0$時，所有個體都存活，因此S(0)=1。
5. $\lim_{t\rightarrow \infty}S(t)$
6. 如果t是連續的，則S(t)通常是連續且可微的。
- - -
![[survival function example.png]]
- - -
parent::[[常用符號目錄]],[[Survival Time]]
sibling::[[Hazard function]]
child::[[pth quantile]]