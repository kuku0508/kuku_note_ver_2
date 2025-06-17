---
參考資料:
  - Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
---
Hotelling's $T^2$ test（霍特林T平方檢定），是檢測[[多變量資料]]的[[多變量分析 - 平均|平均值]]是否為給定值的[[假設檢定]]。為一種[[多變量分析]]方法。
- - -
# 由來
Hotelling's $T^2$ test是以Harold Hotelling命名，他是美國數理統計學家，最著名的貢獻包含Hotelling's $T^2$ 分配以及 典型相關分析（canonical correlation analysis）。
![[Harold hotelling.png|300]]
- - -
# 前提
- 隨機樣本$\bf{X}_1,\bf{X}_2,\ldots,\bf{X}_n$必須來自[[多維常態分配]]$N_p(\mu,\Sigma)$
- - -
# [[假設檢定|檢定]]
#### 虛無假設
Hotelling's $T^2$ test的虛無假設為：

令
$\mu$為來自[[多維常態分配]]$N_p(\mu,\Sigma)$的隨機樣本之[[多變量分析 - 平均#母體平均|母體平均矩陣]]；
$\mu_0$為給定之平均矩陣。則：

$$
H_0：\bf{\mu}=\mu_0\,\,\text{versus}\,\,\rm{H_1}：\mu\neq\mu_0
$$

#### 檢定統計量
在Hotelling's $T^2$ test中，我們會透過$T^2$來決定是否要拒絕虛無假設。
而在多變量的$T^2$檢定其實也是由單變量的T檢定衍伸而來，在單變量中，T值為：
$$
\begin{align}
&t=\frac{\bar{x}-\mu_0}{s/\sqrt{n}}\\\\
\Rightarrow\,&t^2=n(\bar{x}-\mu_0)(s^2)^{-1}(\bar{x}-\mu_0)
\end{align}
$$
而推廣到多變量的情況，檢定統計量Hotelling's $T^2$將會變成：
$$
T^2=n(\bar{\bf{X}}-\mu_0)'\bf{S}^{-1}(\bar{\bf{X}}-\mu_0)
$$
$n$：樣本數
$\bar{\bf{X}}$：[[多變量分析 - 平均#樣本平均|樣本平均矩陣]]
$\bf{S}$：[[多變量分析 - 共變異數#樣本共變異數|樣本共變異數矩陣]]
$\mu_0$：給定的平均向量

且
$$
T^2\sim\frac{(n-1)p}{(n-p)}F_{p,n-p}
$$
$n$：樣本數
$p$：變數數
- - -
# 跟[[Wilks' lambda]]之間的關係
Hotelling's $T^2$跟likelihood ratio統計量$\Lambda$的關係如下：
$$
\Lambda^{2/n}=\left[1+\frac{T^2}{(n-1)}\right]^{-1}
$$
$\Lambda^{2/n}$被稱為[[Wilks' lambda]]，其虛無假設為$\mu=\mu_0$，虛無假設會在$\Lambda^{2/n}$很小或是$T^2$很大時被拒絕。 
- - -
# 備註
- 在單變量的情況下，t統計量可以用來檢定單一樣本的平均數，或是兩個獨立樣本或配對樣本之間的平均數差異。
- Hotelling's $T^2$可以配對比較（paired comparison）或兩個獨立樣本的檢定，用來檢定：$$H_0：\mu_1=\mu_2$$
  其中，母體共變異數矩陣相同或不相同不影響可以檢定與否。
- 對於配對比較或兩群平均數差異的檢定，Hotelling $T^2$的抽樣分配會服從[[F分配]]或正比的或正比的關係。
- 對於大樣本而言，Hotelling $T^2$的抽樣分配可以近似為[[卡方分配]]

- - -
# 例題
- [[MA Assignment 2]]
- - -
parent::[[多變量分析目錄]],[[多變量資料]],[[多變量分析 - 平均]],[[多變量分析 - 共變異數]],[[多維常態分配]],[[假設檢定]],[[多變量分析]],[[F分配]],[[卡方分配]],[[假設檢定]]
sibling::[[Wilks' lambda]]
child::