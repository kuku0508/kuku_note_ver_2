F
 
 兩個 **獨立卡方變數** χ₁²、χ₂² 各除以其自由度，再相除後得到的比值  
$$
F=\frac{\chi_{1}^{2}/d_1}{\chi_{2}^{2}/d_2}\sim F_{\,d_1,d_2}
$$
其中 $d_1, d_2$ 為自由度。

---

## 1. 來源與定義
- 若 $X\sim\chi^2_{d_1}$、$Y\sim\chi^2_{d_2}$ 且 $X\perp Y$，則  
  $
    F=\frac{X/d_1}{Y/d_2}\sim F_{d_1,d_2}
    \quad(\text{右偏且支援 }x>0)
  $
- 可視為 **Gamma 分配** 比值的特殊情形。

---

## 2. 性質
| 項目 | 公式 | 說明 |
|------|------|------|
| 期望 | $E[F]=\dfrac{d_2}{d_2-2}$（需 $d_2>2$） | 自由度愈大→趨近 1 |
| 變異數 | $\displaystyle \operatorname{Var}[F]=\frac{2d_2^{2}(d_1+d_2-2)}{d_1(d_2-2)^{2}(d_2-4)}$（需 $d_2>4$） | 右尾拖得長 |
| 對稱性 | $1/F_{d_1,d_2}\sim F_{d_2,d_1}$ | 做 **雙尾檢定** 時常用 |

---

## 3. 常見應用
1. **兩變異數比檢定**  
   $$
F_\text{obs}=\frac{S_1^{2}}{S_2^{2}}
\sim F_{\,n_1-1,\;n_2-1}\quad(H_0)
   $$
2. **單因子 ANOVA**：  
   $$
F=\frac{\text{組間均方 (MSB)}}{\text{組內均方 (MSW)}}\sim F_{\,k-1,\,N-k}
   $$
   用來比較 $k$ 組平均數是否相等。
3. **Welch ANOVA**（變異數不等）與 **共變數分析 (ANCOVA)** 亦以 F 統計量檢定。

---

## 4. p 值計算
- **右尾**：`pf(F_obs, d1, d2, lower.tail = FALSE)`  
- **雙尾**：$F^*=\max(F_{\text{obs}},1/F_{\text{obs}})$，  
  `p = 2 * pf(F*, d1, d2, lower.tail = FALSE)`

---

## 5. 範例 (R)
```r
f_obs <- 2.4
d1 <- 9; d2 <- 11
p_right <- pf(f_obs, d1, d2, lower.tail = FALSE)
