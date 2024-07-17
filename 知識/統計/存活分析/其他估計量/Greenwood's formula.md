在估計[[Survival Function|存活函數]]的變異數，我們會使用Greenwood's formula。
- - -
# 公式推導：
- 在推導Greenwood's formula之前，需要先認知以下假設
	1. **每個事件時間點的獨立性**：在每個事件時間點，風險集合中的個體是否發生事件是獨立的。
	2. **二項分布**：在時間$t_i$時，發生事件的數量$d_i$可以近似為二項分布$Bin(n_i,p_i)$，其中$p_i=\frac{d_i}{n_i}$是發生事件的機率
- ## 步驟一、計算每個時間點的變異數：
	在每一個時間點$t_i$，事件發生的機率$p_i$ 近似為$\frac{d_i}{n_i}$。根據二項分布的變異數公式，我們可以得到以下公式：
$$
Var(\frac{d_i}{n_i})=\frac{p_i(1-p_i)}{n_i}=\frac{(\frac{d_i}{n_i}-(1-\frac{d_i}{n_i}))}{n_i}
$$
- ## 步驟二、累積變異數：
	存活函數嗜多個時間點上的存活機率的乘積，因此整體變異數需要考慮每個時間點的累積影響。
$$
Var(\hat{S}(t))=\hat{S}(t)^2\sum_{t_i\leq t}\frac{d_i}{n_i(n_i-d_i)}
$$
- ## 步驟三：得到Greenwood's formula：
	最後得到Greenwood's formula：
$$
\hat{\sigma}^2(t)=\hat{S}(t)^2\sum_{i:\,t_i \leq t}\frac{d_i}{n_i(n_i-d_i)}
$$
- - -
# 備註：
- 當我們得到了[[Survival Function|存活函數]]的變異數後，我們就可以去[[confidance Interval of Survival Function|估算存活函數的信賴區間]]。
- - -
parent::[[Survival Function]],[[Kaplan-Meier方法]]
child::[[confidance Interval of Survival Function]]