# 題目：
![[nonparametric statistic Assignment 1.pdf]]
## 2.25
Fifteen heroin addicts were asked to state the age at which they first started using the drug.The results are shown in Table 2.25.Can one conclude from these data that the median age of the sampled population is not 20?Use the sign test,and determine the P-Value.

Table 2.25 Age at which 15 heroin addicts first used the drug.

| Subject | 1   | 2   | 3   | 4   | 5   | 6   | 7   | 8   | 9   | 10  |
| ------- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Age     | 22  | 24  | 37  | 28  | 15  | 14  | 22  | 16  | 18  | 17  |
| Subject | 11  | 12  | 13  | 14  | 15  |     |     |     |     |     |
| Age     | 23  | 16  | 20  | 18  | 15  |     |     |     |     |     |



## 2.29
A test to measure knowledge of current events was given to a sample of 25 elementary school children from an inner-city neighborhood. The scores are sown in Table 2.26.Can one conclude from these data that the population median is less than 70?Use the Wilcxon test and determine the P-Value.

Table 2.26 Scores made on a current-events test by 25 elementary school students from an inner-city neighborhood

| 80  | 68  | 30  | 6   | 70  | 62  | 69  | 65  | 53  | 29  | 65  | 68  |
| --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- | --- |
| 62  | 56  | 46  | 48  | 39  | 72  | 36  | 69  | 40  | 61  | 54  | 53  |
| 25  |     |     |     |     |     |     |     |     |     |     |     |

# 解答
## 2.25
1. 我先把第一次吸食海洛因的年齡從小到大排序：
	14,15,15,16,16,17,18,18,20,22,22,23,24,28,37
2. 確定假設：
	$$H_0：M=20 ,\quad H_1：M\neq 20$$
3. 標記正負號（大於20標記為+，小於20標記為-，等於20無視）
	-,-,-,-,-,-,-,-,+,+,+,+,+,+
	「-」有8個，「+」有6個
4. 計算P-Value
	When hypothesis is $H_0：M=20 ,\quad H_1：M\neq 20$，P-value will be $$
\text{p-value}=2\times P(K\leq k \mid n,0.5),\;\text{where k is the number of signs with the fewer occurrences}$$
	$$\text{p-value}=2\times P(K\leq 6\mid 14,0.5)14$$