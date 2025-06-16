單因子多變量變異數分析（One-Way Multivariate Analysis of Variance,One-Way MANOVA），是用來判斷一個[[類別資料|類別型]]的[[預測變數|自變數]]是否對多個[[連續型隨機變數|連續型]]的[[反應變數|應變數]]有影響。
- - -
# 假設前提
- $\bf{Y}_{\ell1},\bf{Y}_{\ell2},\ldots,\bf{Y}_{\ell g}$是一組樣本大小為$n\ell$的隨機樣本，來自一個[[多維常態分配]]，其[[多變量分析 - 平均|平均向量]]為$\mu_\ell$，$\ell=1,2,\ldots,g$。
- 隨機樣本互相獨立
- 所有母體擁有相同的[[多變量分析 - 共變異數|共變異數矩陣]]$\Sigma$

請注意，當母體大小 $n\ell$ 很大的時候，根據中央極限定理，多維常態性假設可以被放寬。
- - -
# One-Way MANOVA表達式
$$
\bf{Y}_{\ell \,j}=\mu+\tau_\ell+\bf{e}_{\ell j}\quad \rm{for \quad j=1,2,\ldots,n_{\ell}\,\,;\,\,\ell=1,2,\ldots,g}
$$
其中
$\bf{Y}_{\ell j}$：反應變數矩陣
$\mu$：整體的參數平均矩陣
$\tau_\ell$：第$\ell$組處理效應向量（treatment effect），並滿足限制條件
$$
\sum^g_{\ell=1}n_\ell\tau_\ell=0
$$
$e_{\ell j}$：各反應變數的[[誤差項|誤差項矩陣]]，服從$N_p(0,\Sigma)$，且各誤差項間相互獨立。


我們可以用以下表格分析One-Way MANOVA：
$$
\begin{array}{lll}
\hline
\text{Source} & \text{matrix of sum of squares and cross products(SSP)} & \text{df}\\
\hline
\text{Treatment} & \bf{B}=\sum^g_{\ell=1} \rm{n_\ell} (\bar{\bf{y}}_\ell-\bar{\bf{y}})(\bar{\bf{y}}_\ell-\bar{\bf{y}})'&g-1\\
\text{error} & \bf{W}=\sum^g_{\ell=1}\sum^{n\ell}_{j=1}(\bf{y}_{\ell j}-\bar{\bf{y}})(\bf{y}_{\ell j}-\bar{\bf{y}})' & \sum^g_{\ell=1}n_\ell-g\\
\hline
\text{Corrected Total} & \bf{B}=\bf{W}=\sum^g_{\ell=1}\sum^{n\ell}_{j=1}(\bf{y}_{\ell j}-\bar{\bf{y}})(\bf{y}_{\ell j}-\bar{\bf{y}})' & \sum^g_{\ell=1}n_\ell-1
\end{array}
$$
- - -
# [[假設檢定|檢定]]
當我們今天要檢定一個自變數對於多個應變數是否有影響的時候，我們可以對以下的虛無假設進行檢定：
$$
H_0：\tau_1=\tau_2=\ldots=\tau_g=0
$$
而對於這個假設進行檢定，我們可以透過[[Wilks' lambda]] $\Lambda^*=\mid \bf{W}\mid/\mid \bf{B}+\bf{W}\mid$
來拒絕或不拒絕虛無假設。

而$\Lambda^*$會服從自由度為p跟g的F分配。
$$
\Lambda^*\sim F(p,g)
$$
在大樣本的情況下，[[Wilks' Lambda]]也會趨近自由度為p(g-1)的卡方分配。
- - -
# [[信賴區間|區間]]
如果我們通過了假設檢定，確定了處理（treatment）之間是有差異的話，我們可以透過多重比較來確認處理之間的差異約為多少。
$100(1-\alpha)$%的多重比較信賴區間可以被表示為：
$$
\bar{y}_{ki}-\bar{y}_{\ell i}\pm t_{n-g}\left(\frac{\alpha}{pg(g-1)}\right)\sqrt{\frac{w_{ii}}{n-g}\left(\frac{1}{n_k}+\frac{1}{n_\ell}\right)}
$$
其中
$w_{ii}$：矩陣$\bf{W}$的第i個對角元素
$n=\sum^g_{\ell=1}n\ell$：總樣本數
- - -
# 備註
當我們透過了One-Way MANOVA來得到處理（treatment）對於應變數是有顯著影響的時候，我們應該還需要用[[Hotelling's T2 test|Hotelling's T2 test]]等方式來檢視該處理是否對於各個應變數是有顯著影響的。因為在整體顯著的情況，還是會有單變量不顯著的狀況發生。
- - -
# 參考資料
- Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
- - -
parent::[[多變量分析目錄]],[[假設檢定]],[[類別資料]],[[反應變數]],[[預測變數]],[[量性資料]],[[連續型隨機變數]],[[多維常態分配]],[[多變量分析 - 平均]],[[多變量分析 - 共變異數]],[[誤差項]],[[Wilks' lambda]],[[信賴區間]]
sibling::[[Hotelling's T2 test]]
child::