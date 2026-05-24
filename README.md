# theater-logs

A personal theater logs.

## 資料範圍 (Data Range)

以演員為主體，範圍包含一般的戲劇演出、沉浸式，以及即興表演。

## 資料結構 (Data Schema)

本專案的主要紀錄存放於 `[theater_logs.csv](https://github.com/repeat/theater-logs/blob/main/theater-logs.csv)`。
為方便自動化分析與機器讀取，各欄位定義如下：

| 欄位名稱 (Column) | 資料型態 (Type) | 說明 (Description) |
| :--- | :--- | :--- |
| `show_full_datetime` | String | 原始格式的開演時間（含星期） |
| `show_date` | Date | 開演日期，格式為 `YYYY-MM-DD` |
| `show_time` | Time | 開演時間，格式為 `HH:MM:SS`。 ⚠️ **注意：所有時間均為 `Asia/Taipei (UTC+8)`。** |
| `show_weekday` | String | 星期縮寫（如 Sun, Mon） |
| `show_title` | String | 節目名稱 |
| `venue` | String | 演出場地 |
| `entries` | Integer | 觀賞同劇目的次數（例如 `1` 為首刷，`2` 為二刷） |
| `ticket_price` | Integer | 票價（新台幣），純數字格式 |
| `reasons_of_entry` | String | 觀劇動機或備註 |

## 免責聲明 (Disclaimer)

1. 由於記憶的不可靠性，如果我有記錯而修正記錄時，以最新修正內容為主。
2. 這個表理論上會不定時更新。

## 授權條款 (License)

[創用 CC 姓名標示-相同方式分享 4.0 國際 授權條款 (CC BY-SA 4.0)](https://creativecommons.org/licenses/by-sa/4.0/deed.zh-hant)
