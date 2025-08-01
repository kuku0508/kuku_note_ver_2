# 問題：
根據綠黨在2020年12月29日到2020年12月30日進行的抽樣調查，樣本數1044筆，蔡英文支持率為54.2%，試問蔡英文的實際支持率是否有大於50%？
# 回答：
在這題目裡面，虛無假設為：
$$
H_0\text{：}p\leq 0.5\quad versus \quad H_1\text{：}p>0.5
$$
針對檢定母體比例的問題，我們可以使用單樣本Z檢定來判斷。
檢定統計量會是：
$$
Z=\frac{0.542-0.5}{0.5^2/\sqrt{1044}}=5.4282
$$
透過查表，我們可以知道$P(Z>5.4282)\approx 0$
而因為P值遠低於顯著水準，故我們拒絕虛無假設，我們有足夠強烈的證據證明蔡英文的實際支持率大於50%。

而我們也可以看到，在2020年總統大選的選舉結果也顯示，蔡英文的實質得票率為57.13%。