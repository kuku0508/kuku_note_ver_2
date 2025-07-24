---
參考資料:
  - Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
---
雙因子多變量變異數分析（Two-Way Multivariate Analysis of Variance, One-Way MANOVA），是用來判斷兩個[[類別資料|類別型]]的[[預測變數|自變數]]是否對多個[[連續型隨機變數|連續型]]的[[反應變數|應變數]]有影響。
- - -
# 假設前提
- $\bf{Y}_{\ell1},\bf{Y}_{\ell2},\ldots,\bf{Y}_{\ell g}$是一組樣本大小為$n\ell$的隨機樣本，來自一個[[多維常態分配]]，其[[多變量分析 - 平均|平均向量]]為$\mu_\ell$，$\ell=1,2,\ldots,g$。
- 隨機樣本互相獨立
- 所有母體擁有相同的[[多變量分析 - 共變異數|共變異數矩陣]]$\Sigma$

請注意，當母體大小 $n\ell$ 很大的時候，根據中央極限定理，多維常態性假設可以被放寬。
- - -
# Two-Way MANOVA表達式
具有交互作用的雙因子固定效果的MANOVA可以表示成：
$$
\bf{Y}_{\ell k r}=\bf{\mu}+\tau_\ell+\beta_k+\gamma_{\ell k}+\bf{e}\ell k r
$$
其中
- $\bf{Y}_{\ell k r}$：因子一的第$\ell$組，因子二的第k組的第r個觀察值。其中$\ell=1,2,\ldots,g$ ; $k=1,2,\ldots,b$ ; $r=1,2,\ldots,n$。
- $\mu$：參數向量
- $\tau_{\ell}、\beta_k$：因子一、因子二的固定效應（fixed effects），兩者皆滿足條件$\sum^g_{\ell=1}\tau_\ell=\sum^b_{k=1}\beta_k=0$
- $\gamma_{\ell k}$：交互作用項，滿足條件$\sum^g_{\ell=1}\gamma_{\ell k}=\sum^b_{k=1}\gamma_{\ell k}=0$
- 誤差項$\bf{e}_{\ell k r}\sim N_p(0,\Sigma)$

我們可以用以下表格分析One-Way MANOVA：
$$
\begin{array}{lll}
\hline
\text{Source} & \text{matrix of sum of squares and cross products(SSP)} & \text{df}\\
\hline
\text{Factor 1}&\text{SSP}_{fac1}&g-1 \\
\text{Factor 2}&\text{SSP}_{fac2}&b-1 \\
\text{Interaction}&\text{SSP}_{int}&(g-1)(b-1)\\
\text{Error}&\text{SSP}_{error}&gb(n-1)\\
\hline
\text{Corrected Total}&\text{SSP}_{total}&gbn-1
\end{array}
$$
- - -
# [[假設檢定|檢定]]
透過Wilks' Lambda，我們可以檢測交互作用、因子一以及因子二的主效應是否顯著。

#### 交互作用
$$
H_0：\gamma_{11}=\ldots=\gamma_{gb}=0
$$
我們用此統計量來進行檢定：
$$
\Lambda^*_1=\frac{\mid \text{SSP}_{error}\mid}{\mid \text{SSP}_{int}+\text{SSP}_{error}\mid}
$$
#### 因子一
$$
H_0：\tau_{1}=\ldots=\tau_{g}=0
$$
我們用此統計量來進行檢定：
$$
\Lambda^*_2=\frac{\mid \text{SSP}_{error}\mid}{\mid \text{SSP}_{fac1}+\text{SSP}_{error}\mid}
$$
#### 因子二
$$
H_0：\beta_{1}=\ldots=\beta_{b}=0
$$
我們用此統計量來進行檢定：
$$
\Lambda^*_3=\frac{\mid \text{SSP}_{error}\mid}{\mid \text{SSP}_{fac2}+\text{SSP}_{error}\mid}
$$
需要注意的是，上述統計亮在樣本數很大的時候，其極限分配（樣本數趨近無限大）為[[F分配]]或[[卡方分配]]。在檢定的時候，我們應該要先檢定交互作用，再檢定主效應。
倘若交互作用存在，則主效應也應存在。

$\Lambda^*$的精確分配如下：
$$
\begin{array}{lll}
\hline
變數數量p&組別數g&在常態假設下的抽樣分配\\
\hline
p=1 & g\geq2 & \left(\frac{\sum n_\ell-g}{g-1}\right) \left(\frac{1-\lambda}{\lambda^*}\right)\sim F_{g-1,\,\sum n_\ell-g-1}\\
p=2 & g\geq2 & \left(\frac{\sum n_\ell-g-1}{g-1}\right) \left(\frac{1-\sqrt{\lambda^*}}{\sqrt{\lambda^*}}\right)\sim F_{2(g-1),\,\sum n_\ell-p-1}\\
p\geq1 & g=2 & \left(\frac{\sum n_\ell-p-1}{p}\right) \left(\frac{1-\lambda^*}{\lambda^*}\right)\sim F_{p,\,\sum n_\ell-p-1}\\
p\geq1 & g=3 & \left(\frac{\sum n_\ell-p-2}{p}\right) \left(\frac{1-\sqrt{\lambda^*}}{\sqrt{\lambda^*}}\right)\sim F_{2p,\,2(\sum n_\ell-p-2)}\\
\hline
\end{array}
$$
- - -
# 備註
在多變量鑑定中，我們主要專注於統計量Wilks' lambda，其實其就等價於概似比（likelihood ratio）統計量。
- - -
parent::[[多變量分析目錄]],[[類別資料]],[[反應變數]],[[連續型隨機變數]],[[預測變數]],[[多維常態分配]],[[多變量分析 - 平均]],[[假設檢定]],[[F分配]],[[未處理/卡方分配]]
sibling::[[One-Way MANOVA]]
child::