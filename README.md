# Python for Bioinformatics — Interactive Tutorial

**🌐 Live demo / 線上瀏覽**: <https://charlene717.github.io/python-bioinformatics-interactive-tutorial/>


從零開始的 Python 生物資訊互動式教程，雙語（中文 / 英文）切換。架構與風格參考自姊妹站 [scrna-interactive-tutorial](https://charlene717.github.io/scrna-interactive-tutorial/)。

## 開始使用

直接以瀏覽器開啟 `index.html` 即可，或部署到 GitHub Pages / 任何靜態主機。

```bash
# 本機快速啟動（可選）
cd path/to/python-bioinformatics-interactive-tutorial
python -m http.server 8000
# 開啟 http://localhost:8000
```

## 章節地圖

### 01 基礎篇
1. **setup** — 環境設定（Anaconda / Miniconda、IDE、虛擬環境、套件管理）
2. **syntax** — Python 語法基礎（變數、容器、控制流、例外）
3. **paths** — 檔案路徑與 I/O（pathlib、CWD、CSV/JSON/壓縮檔）
4. **functions** — 函式、類別、模組（dataclass、import、專案結構）

### 02 資料科學三大套件
5. **numpy** — 數值運算（ndarray、broadcasting、稀疏矩陣）
6. **pandas** — 資料框（loc/iloc、groupby、merge、pivot）
7. **visualization** — Matplotlib / Seaborn（volcano、heatmap、論文圖）

### 03 序列分析
8. **biopython** — Seq / SeqRecord / Entrez
9. **fasta-fastq** — SeqIO 讀寫、Phred 品質、pyfastx 加速
10. **blast** — 線上 / 本機 BLAST、E-value、pairwise2、MSA

### 04 高通量定序 (NGS)
11. **pysam** — SAM/BAM 欄位、CIGAR、coverage、區段查詢
12. **variant-calling** — GATK Best Practices、VCF、cyvcf2

### 05 單細胞與空間
13. **scanpy-anndata** — AnnData 結構、scanpy API 慣例
14. **scrna-workflow** — QC → UMAP → 註解 → 整合
15. **spatial** — Squidpy / SpatialData（Visium、Xenium、Moran's I）

### 06 進階 AI 與多體學
16. **multi-omics** — MuData、CITE-seq (totalVI)、Multiome (MultiVI / MOFA)
17. **scllms** — scGPT / Geneformer / scFoundation（單細胞大型語言模型）
18. **ai-bioinformatics** — PyTorch、ESM-2、AlphaFold

## 互動元素

- 中英雙語切換（右上角按鈕，記憶於 localStorage）
- 進度捲軸條
- 程式碼分頁（多語言切換）
- 互動模擬器：
  - Ch 1 conda 指令產生器
  - Ch 2 DNA → 蛋白質 即時翻譯器
  - Ch 3 路徑解析器
  - Ch 5 向量化 vs 迴圈速度比較
  - Ch 7 Volcano plot 閾值模擬
  - Ch 9 Phred 品質分數轉換器
- 每章自我檢測 quiz

## 技術說明

純靜態網站，僅依賴：

- `styles.css`（自訂 CSS variables，藍 + 琥珀色主題以區別 scRNA 教程的綠色）
- `i18n.js`（語言切換、localStorage 持久化）
- Chart.js（Ch 7、Ch 9 互動圖）— 透過 CDN 引入
- 字型：Crimson Pro / DM Sans / JetBrains Mono（Google Fonts）

無建置流程，可直接部署。

## 授權

© Charlene — 教學用途，歡迎引用
