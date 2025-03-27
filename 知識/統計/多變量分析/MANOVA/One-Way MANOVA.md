單因子多變量變異數分析（One-Way Multivariate Analysi of Variance,One-Way MANOVA），是用來判斷一個[[類別資料|類別型]]的[[預測變數|自變數]]是否對多個[[連續型隨機變數|連續型]]的[[反應變數|應變數]]有影響。
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
$e_{\ell j}$：[[誤差項]]
