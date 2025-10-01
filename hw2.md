# HW2 專案管理作業

## 1. 任務分解與工期估算 (WBS)

| 任務編號 | 任務名稱           | 工期 (天) |
|----------|--------------------|-----------|
| 1        | 第一階段功能整合測試 | 7         |
| 2        | 第二階段功能構想     | 5         |
| 3        | 工作分配             | 1         |
| 4        | 撰寫程式碼           | 30        |
| 5        | 功能測試             | 1         |
| 6        | Debug 與優化         | 21        |
| 7        | 第二階段功能整合測試 | 7         |
| 8        | 撰寫文件與教學整理   | 10        |

---

```mermaid
graph TD
    A1[1 研擬計畫 4天] --> A2[2 任務分配 1天]
    A1 --> A3[3 取得硬體 17天]
    A2 --> A4[4 程式開發 70天]
    A3 --> A5[5 安裝硬體 3天]
    A4 --> A6[6 程式測試 30天]
    A5 --> A7[7 撰寫使用手冊 25天]
    A5 --> A8[8 轉換檔案 20天]
    A6 --> A9[9 系統測試 25天]
    A7 --> A10[10 使用者訓練 20天]
    A8 --> A10
    A9 --> A11[11 使用者測試 25天]
    A10 --> A11

    classDef critical fill:#f77,stroke:#333,stroke-width:2px;
    class A1,A2,A4,A6,A9,A11 critical;


```
## 2. 甘特圖
```mermaid


gantt
title 作業:甘特圖
dateformat YYYY-MM-DD
axisFormat %m/%d

section 任務
研擬計畫 :crit,a1, 2025-10-01, 4d
任務分配 :crit,a2, after a1, 1d
取得硬體 :a3, after a1, 17d
程式開發 :crit,a4, after a2, 70d
安裝硬體 :a5, after a3, 3d
程式安裝 :crit,a6, after a4, 30d
撰寫使用手冊 :a7, after a5, 25d
轉換檔案 :a8, after a5, 20d
系統測試 :crit,a9, after a6, 25d
使用者訓練 :a10, after a7, 20d
使用者測試 :crit,a11, after a9, 25d

``` 


