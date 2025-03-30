Box's M test，是一種檢定[[多變量資料]]中多個群組之間的[[多變量分析 - 共變異數|共變異數矩陣]]之間是否相等的[[假設檢定|檢定]]方法。
群組就是，以某一個變數作為分組依據，將資料分成多個組別。
e.g 將資料分為(男生、國文分數、數學分數、英文分數)；(女生、國文分數、數學分數、英文分數)，就是以性別為分組依據，將資料分為男生，女生兩個群組。
- - -
# 假設前提
- 各個變數的資料必須服從或近似[[多維常態分配]]
- 每個觀測值之間必須互相獨立
- - -
# [[假設檢定|檢定]]
當我們今天遇到以下的虛無假設，我們就可以選擇使用Box's M test來進行假設檢定：
$$
\text{H}_0：所有組別的共變異數相等\,\,\text{versus}\,\, H_1：至少有一個群組的共變異數矩陣與其他不同。
$$
我們可以透過統計量Box's M 來對上述的假設進行檢定。
統計量Box's M被給定為：
$$
M=\left[\sum(n_\ell-1)\right]\ln\mid \bf{S}_{pooled}\mid - \sum\left[(n_\ell-1)\ln\mid \bf{S}_\ell \mid\right]
$$
其中：
$\bf{S}_\ell$：為第$\ell$組的樣本共變異數矩陣
$\bf{S}_{pooled}$：合併的共變異數矩陣

而統計量Box's M服從自由度為$p(p+1)(g-1)/2$的卡方分配
$$
M\sim \chi^2_{p(p+1)(g-1)/2}
$$
- - -
# 備註
當今天樣本數不是大樣本十，Box's M會變得非常敏感，可能會導致[[Type I error|型一誤（Type I error）]]。當今天樣本數越大，Box's M test會越可靠。
- - -
# 參考資料
- Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
- - -
parent::[[多變量資料]],[[多變量分析 - 共變異數]],[[假設檢定]],[[多維常態分配]]
sibling::
child::