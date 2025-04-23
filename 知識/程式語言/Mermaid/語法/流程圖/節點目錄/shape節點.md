先講一下，在寫Mermaid的流程圖相關的筆記的時候，我是邊看Mermaid官網的教學邊寫的。而我到現在才發現，流程圖很多筆記都可以用shape來寫，幹。小小抱怨一下而已，可能要新增一些筆記的內容。

在節點的建立上，我們有一個比較方便的方法可以去決定節點的形狀，就是在用`節點名稱@{ shape: 節點代號}`的方式來建立，而代號如下。


| 節點意義    | 形狀名稱    | 節點代號         | 描述      | 節點代號別名                          |
| ------- | ------- | ------------ | ------- | ------------------------------- |
| 卡片      | 有缺口的矩形  | `notch-rect` | 代表一張卡片  | `card`,`notched-rectangle`      |
| 整理      | 沙漏      | `hourglass`  | 代表整理操作  | `collate`,`hourglass`           |
| 通訊連結    | 閃電      | `bolt`       | 通訊連結    | `com-link`,`lightning-bolt`     |
| 註釋      | 左大括號    | `brace`      | 新增註釋    | `brace-l`,`comment`             |
| 右側註釋    | 右大括號    | `brace-r`    | 新增註釋    | 無                               |
| 雙邊註釋    | 雙大括號    | `braces`     | 新增註釋    | 無                               |
| 資料輸入/輸出 | 平行四邊形   | `lean-r`     | 表示輸入或輸出 | `in-out`,`lean-right`           |
| 資料輸出/輸入 | 逆-平行四邊形 | `lean-l`     | 表示輸出或輸入 | `lean-left`,`out-in`            |
| 資料庫     | 圓柱體     | `cyl`        | 資料庫儲存   | `cylinder`,`database`,`db`      |
| 決策      | 菱形      | `diam`       | 決策步驟    | `decision`,`diamond`,`question` |
| 延遲      | 半圓角矩形   |              |         |                                 |
|         |         |              |         |                                 |
|         |         |              |         |                                 |
|         |         |              |         |                                 |
|         |         |              |         |                                 |
|         |         |              |         |                                 |
```mermaid
flowchart
A@{ shape: lean-r}
```

- - -
# 參考資料
- [Flowcharts - Basic Syntax](https://mermaid.js.org/syntax/flowchart.html)
- - -
parent::[[節點目錄]]
sibling::
child::