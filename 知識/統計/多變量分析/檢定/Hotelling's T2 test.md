Hotelling's $T^2$ test（霍特林T平方檢定），是檢測[[多變量資料]]的[[多變量分析 - 平均|平均值]]是否為給定值的[[假設檢定]]。為一種[[多變量分析]]方法。
- - -
# 由來
Hotelling's $T^2$ test是以Harold Hotelling命名，他是美國數理統計學家，最著名的貢獻包含Hotelling's $T^2$ 分配以及 典型相關分析（canonical correlation analysis）。
![[Harold hotelling.png|300]]
- - -
# 前提
- 隨機樣本$\bf{X}_1,\bf{X}_2,\ldots,\bf{X}_n$必須來自[[多維常態分配]]$N_p(\mu,\Sigma)$
- - -
# 檢定
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

且
$$
T^2\sim\frac{(n-1)p}{(n-p)}F_{p,n-p}
$$
- - -
# 跟Wilk's lamba之間的關係
Hotelling's $T^2$跟likelihood ratio統計量$\Lambda$的關係如下：
$$
\Lambda^{2/n}=\left[1+\frac{T^2}{(n-1)}\right]^{-1}
$$
$\Lambda^{2/n}$被稱為Wilk's lambda，其虛無假設為\mu
- - -
# 參考資料
- Applied Multivariate Statistical Analysis, sixth editon ,Johnson Richard A. ;  Dean W. Wichern
- - -
parent::[[多變量資料]],[[多變量分析 - 平均]],[[假設檢定]],[[多變量分析]]
sibling::
child::