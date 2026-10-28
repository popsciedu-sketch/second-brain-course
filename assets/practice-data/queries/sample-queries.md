# 常用 Query 範例（可貼到儀表板）

## 所有 TODO
{{query (task TODO)}}

## 帶 #靈感 的塊（依版本可用 tags / page-tags）
{{query (and (task TODO DOING DONE NOW LATER) [[靈感]])}}

## 某頁的雙向連結周邊
在頁面底部查看 Linked References；或搜尋 `[[頁名]]`。

## 本教學建議每週回顧 Query
1. 未完成 TODO
2. 過去 7 天日記中未連結的塊（人工掃一遍即可）
3. 已完成專案是否該封存
