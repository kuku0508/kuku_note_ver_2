# 問題：
Provide a justification o relations.That is:
1. $P(A^c\bigcap B^c)-P(A^c)P(B^c)=P(A\bigcap B)-P(A)P(B)$
2. $P(A^c\bigcap B)-P(A^c)P(B)=-P(A\bigcap B)+P(A)P(B)$
3. $P(A\bigcap B^c)-P(A)P(B^c)=-P(A\bigcap B)+P(A)P(B)$
# 回答：
在解這種集合的題目時，我都推薦畫一個這樣的圖：
![[文氏圖.png|400]]
$$
\begin{align}
P(A^c\bigcap B^c)-P(A^c)P(B^c)&=P(A\bigcup B)^c-(1-P(A))(1-P(B))\\
&=1-P(A\bigcup B)-(1-P(A)-P(B)+P(A)P(B))\\
&=\underbrace{P(A)+P(B)-P(A\bigcup B)}_{P(A\bigcap B)}-P(A)P(B)\\
&=P(A\bigcap B)-P(A)P(B)
\end{align}
$$

$$
\begin{align}
P(A^c\bigcap B)-P(A^c)P(B)&=P(B-A\bigcap B)-(1-P(A)P(B)\\
&=P(B)-P(A\bigcap B)-P(B)+P(A)P(B)\\
&=-P(A\bigcap B)+P(A)P(B)\\
\end{align}
$$

$$
\begin{align}
P(A\bigcap B^c)-P(A)P(B^c)&=P(A-A\bigcap B)-P(A)P(B^c)\\
&=P(A)-P(A\bigcap B)-P(A)(1-P(B))\\
&=P(A)-P(A\bigcap B)-P(A)-P(A)P(B)\\
&=-P(A\bigcap B)-P(A)P(B)
\end{align}
$$
