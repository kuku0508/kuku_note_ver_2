# 標準常態分配：
當我們今天把常態分配[[標準化]]後，我們可以得到平均數為0、標準差為1的標準常態分配
得到**Z值**如下：
$$
Z=\frac{X-\mu}{\sigma}\sim N(0,1)
$$
得到的值我們通常稱為Z值（Z-Score；standatdized score）
而今天他的PDF跟CDF就會變成
### [[機率密度函數|PDF]]

$$
f(x)=\frac{1}{\sqrt{2\pi}}exp\left(-\frac{x^2}{2}\right)
$$
$e$：自然對數

### [[累積分配函數|CDF]]
$$
F(x;0,1)=\frac{1}{\sqrt{2\pi}}\int^x_{-\infty}exp\left(-\frac{t^2}{2}\right)dt
$$
其實就是把$\mu=0$、$\sigma=1$，代入原本的公式而已。

- - -
# 參考資料

- - -
parent::
sibling::
child::