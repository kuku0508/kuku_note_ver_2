---
參考資料: 
屬於環節:
  - "[[datastep]]"
---
DELETE，是一種[[SAS敘述句]]。可以用來刪除觀測值。倘若觀測值被刪除，則不會出現在輸出的資料集中。
- - -
# 基本語法

通常DELETE會搭配[[IF]]來一起使用。
```SAS
IF 條件 THEN DELETE;
```
表示，如果觀測值符合條件的話，則刪除觀測值。
- - -
# 備註
- 倘若只有`DELETE`作為一句敘述句，SAS則會刪除所有觀測值。
- - -
# 範例
倘若今天有一個資料集customer，我們不希望她有任何一個變數存在遺失值，我們則可以透過以下的程式碼來達到這個要求：

```SAS
data customer_without_missing;
	set customer;
	 do i = 1 to 3;
        if var{i} = . then delete;  /* 只要任一欄位是缺失值就刪除 */
    end;
run;
```

- - -
parent::[[SAS敘述句]]
sibling::[[IF]]
child::