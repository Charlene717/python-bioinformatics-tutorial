# Python BioInfo Quiz · 互動考題

針對姐妹站 [`python-bioinformatics-interactive-tutorial`](../) 18 章內容製作的互動考題系統，雙語切換、考試／練習雙模式、進度可保存。

## 開始使用

直接以瀏覽器開啟 `index.html` 即可，或部署到 GitHub Pages / 任何靜態主機。

```bash
cd path/to/python-quiz
python -m http.server 8000
# 開啟 http://localhost:8000
```

## 題庫總覽

- **18 章 · 144 題**（每章 8 題）
- 題型分佈：單選 107、多選 18、是非 19
- 每題附中英雙語題幹、選項、解析

### 章節結構

| 區塊 | 章節 | 題數 |
|------|------|------|
| 基礎篇：環境與語法 | Ch 1：環境設定與安裝 | 8 |
| | Ch 2：Python 語法基礎 | 8 |
| | Ch 3：檔案路徑與 I/O | 8 |
| | Ch 4：函式、類別、模組 | 8 |
| 資料科學三大套件 | Ch 5：NumPy 數值運算 | 8 |
| | Ch 6：Pandas 資料框 | 8 |
| | Ch 7：視覺化 (Matplotlib/Seaborn) | 8 |
| 序列分析 | Ch 8：Biopython 基礎 | 8 |
| | Ch 9：FASTA / FASTQ 處理 | 8 |
| | Ch 10：BLAST 與序列比對 | 8 |
| 高通量定序 (NGS) | Ch 11：pysam 與 SAM/BAM | 8 |
| | Ch 12：變異呼叫 & VCF | 8 |
| 單細胞與空間轉錄組 | Ch 13：AnnData 與 scanpy 入門 | 8 |
| | Ch 14：scRNA-seq 完整流程 | 8 |
| | Ch 15：空間轉錄組 (Squidpy) | 8 |
| 進階 AI 與多體學 | Ch 16：多體學整合 | 8 |
| | Ch 17：單細胞 LLMs (scLLMs) | 8 |
| | Ch 18：AI 在生物資訊應用 | 8 |

## 主要功能（與 scrna-quiz 相同）

- **練習模式**：每題立即顯示對錯與解析
- **考試模式**：全部答完一次性交卷看結果
- **多使用者切換**：同一台電腦多人共用、進度互不干擾
- **錯題複習** + **🔖 標記題複習**
- **🎲 隨機練習**：可指定題數與題源（全部 / 錯題 / 標記題）
- **匯入 / 匯出**：JSON 進度備份、HTML 成績單、HTML 錯題講義
- **中英雙語切換**：右上角按鈕，記憶在 localStorage
- **鍵盤操作**：←/→ 切題、A/B/C/D 或 1-4 選擇單選、空白鍵切換多選、Enter 送出

## 檔案結構

```
python-quiz/
├── index.html      # 主頁面（UI + 互動邏輯）
├── data.js         # 題庫資料（中英雙語）
├── i18n.js         # 中英切換與字典
└── README.md
```

## 與 scRNA-seq 教程的隔離

雖然兩個 quiz 共用相同的程式架構，但 localStorage 鍵與資料模型 key 都已分離：

| 項目 | scrna-quiz | python-quiz |
|------|-----------|-------------|
| `QUIZ_DATA` 子鍵 | `scrna` | `python` |
| 進度 localStorage 前綴 | `scrnaquiz_` | `pyquiz_` |
| 語言 localStorage 鍵 | `scrna_lang` | `pybio_lang` |

兩套 quiz 可同時使用、進度與設定完全獨立。

## 授權

© Charlene — 教學用途，歡迎引用
