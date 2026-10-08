# 【Code Review】AI 時代的 CR 還有意義麼？

- 影片 ID：lWbY9R8qR-w
- 時長：15:48
- 來源：https://www.youtube.com/watch?v=lWbY9R8qR-w
- 逐字稿：Whisper small（中文）

## 一句話總結
以 Python 小專案 TempArts 為例，說明 AI 時代的 Code Review 已從抓小錯轉向審視設計、介面與工程實踐。

## 專案與設計
- 功能：依母版從字串擷取資料，支援型別（int/float/complex/json）轉換與泛型。
- 亮點：用 t-string（3.14 新特性）解析、預先 compile regex、泛型強化 type check。

## Review 重點
- 命名：`i` 這種變數名易與 index/integer 混淆，降低可讀性。
- 設計冗餘：`conversion` / `format_conversion` decorator 未帶來足夠價值，可直接傳入轉換函式。
- 使用者體驗：`str`、`int` 等重複輸入，應給合理預設。
- 一致性：`json` 直接當模板與其他設計不一致，應改 `json.loads`。
- 工程面：缺 coverage、CI 只有 publish，沒有 lint/format/test。
- 型別檢查：既然重視型別，建議 runtime type check。

## 一句話
「AI 讓小細節問題變少，但 design、interface、CI 仍有大量值得 review 之處——關鍵是你有沒有意識去和 AI 溝通這些。」
