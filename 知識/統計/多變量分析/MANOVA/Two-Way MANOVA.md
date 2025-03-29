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
- 
- - -
# 參考資料
- Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
- - -
parent::[[多變量分析目錄]],[[類別資料]],[[反應變數]],[[連續型隨機變數]],[[預測變數]]
sibling::[[One-Way MANOVA]]
child::