Hazard function(危險函數)，通常以h(t)或$\lambda(t)$表示，是指觀察對象在時間t依然存活時，在下一個瞬間發生事件的風險度。
- - -
我一開始很不能理解Hazard function這個概念，妳可以這樣想像Hazard function。
想像你是一艘船，在一條河流上運行，河流上面有一些地方有激流或是危險，會讓妳的船翻覆。Hazard function就是妳在河流的不同位置遇到激流或危險的機率。
- t就像妳在河流上面運行的時間
- h(t)表示妳在某一個特定位置(t)遇到危險的可能性。
- - -
# 公式：
$$
h(t)=\lambda(t)=\lim_{\Delta t\rightarrow 0}\frac{P(t\leq T <t+\Delta t|T\geq t)}{\Delta t}
$$
- - -
# 備註：

> 不是機率
> 不是機率
> 不是機率
- Average hazred rate：
$$
\bar{h}=\frac{\sum^k_{i=1}\lbrace failures\rbrace}{\sum^k_{i=1}t_{(i)}}
$$
- - - 
# 性質：
1. $h(t)$ is a conditional failure rate **not a probability**
2. $h(t) \geq0(h(t)\nleq1)$  
- - -
# Relationship bewteen $S(t)\,and\,h(t)$：
$$
\begin{align}
h(t)=&\lim_{\Delta t\rightarrow0}\frac{P(t\leq T <t+\Delta t\mid T \geq t)}{\Delta t}\\
=&\lim_{\Delta\rightarrow0}\frac{P(t\leq T<t+\Delta t)}{\Delta t}\times\frac{1}{P(T\geq t)}\\
=&\frac{f(t)}{S(t)}\\
=&\frac{-S^{'}(t)}{S(t)}\\
=&-\frac{d}{dt}\ln S(t)\\
\Rightarrow& S(t)=exp\left\lbrace-\int^t_0h(t)du\right\rbrace
\end{align}
$$
- - -
parent::[[Survival Time]],[[常用符號目錄]]
slbling::[[Survival Function]]