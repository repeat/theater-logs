# theater-logs

A personal theater logs.

## 資料範圍 (Data Range)

以演員為主體，範圍包含一般的戲劇演出、沉浸式，以及即興表演。

## 資料結構 (Data Schema)

本專案的主要紀錄存放於 [theater_logs.csv](https://github.com/repeat/theater-logs/blob/main/theater-logs.csv)。
為方便自動化分析與機器讀取，各欄位定義如下：

| 欄位名稱 (Column) | 資料型態 (Type) | 說明 (Description) |
| :--- | :--- | :--- |
| `show_full_datetime` | String | 原始格式的開演時間（含星期） |
| `show_date` | Date | 開演日期，格式為 `YYYY-MM-DD` |
| `show_time` | Time | 開演時間，格式為 `HH:MM:SS`。 ⚠️ **注意：所有時間均為 `Asia/Taipei (UTC+8)`。** |
| `show_weekday` | String | 星期縮寫（如 Sun, Mon） |
| `troupe` | String | 演出劇團或製作單位名稱 |
| `project_tag` | String | 系列企劃或活動標籤（如人間條件、臺北藝穗節），無則留空 |
| `show_title` | String | 節目名稱 |
| `venue` | String | 演出場地 |
| `entries` | Integer | 同一劇目的第幾次入場（例如 `1` 為首刷，`2` 為二刷）。純粹計算入場次數，不代表演出內容或卡司相同，詳見免責聲明第 3 點 |
| `ticket_price` | Integer | 票價（新台幣），純數字格式 |
| `reasons_of_entry` | String | 觀劇動機或備註 |
| `new_followed_actors` | String | 觀劇後新關注的演員 |

## 免責聲明 (Disclaimer)

1. 由於記憶的不可靠性，如果我有記錯而修正記錄時，以最新修正內容為主。
2. 觀劇動機或備註緩慢補齊中。
3. `entries` 只代表「第 N 次為同一劇目購票入場」，不代表每次演出內容完全相同。同一劇目可能因劇團採 A/B 卡或 ABCD 多組卡司排列組合而每場卡司不同，或本身即為即興演出而每場互動內容都不可複製，這類差異目前不會反映在 `entries` 上，僅記錄在 `reasons_of_entry`（如提及特定卡別、來賓）中，且不保證完整。

## 授權條款 (License)

[創用 CC 姓名標示-相同方式分享 4.0 國際 授權條款 (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.zh-hant)
