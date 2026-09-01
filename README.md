# ResearchAssistant (醫學文獻自動化研究助理工作流) 📚🤖

專為醫學、職能治療與臨床研究者設計的 n8n 自動化文獻追蹤與 AI 摘要工作流，大幅縮短文獻追蹤（Literature Review）與閱讀整理時間。

## 🌟 包含工作流 / Workflows

### 1. PubmedSeeker (`PubmedSeeker.json`)
- ⏱️ **定時排程自動檢索**：自動按設定排程定時查詢 PubMed API。
- 🔍 **多重關鍵字與過濾器**：自動追蹤復健醫學、職能治療、神經認知等最新出版文獻。
- 📬 **智慧通知與輸出**：自動過濾已讀項目，將符合條件之最新論文標題、作者、期刊與摘要推播至指定頻道或試算表。

### 2. PaperReviewer (`PaperReviewer.json`)
- 📖 **Zotero 書目庫即時同步**：監聽個人或團隊 Zotero API，偵測新加入的論文與 PDF。
- 🧠 **結構化 AI 論文解析**：調用大型語言模型自動萃取核心重點：
  - 研究目的（Objective & Background）
  - 受試者與收案條件（Participants & Population）
  - 介入方式與實驗設計（Intervention & Methodology）
  - 評估工具與量表（Outcome Measures）
  - 統計結果與結論（Results & Key Findings）
  - 臨床價值與限制（Clinical Implications & Limitations）

## 📂 檔案結構 / File Structure

```text
ResearchAssistant/
├── PubmedSeeker.json   # PubMed 自動定時檢索 n8n 工作流
├── PaperReviewer.json  # Zotero + LLM 自動論文摘要 n8n 工作流
└── README.md           # 專案說明文件
```

## 🚀 使用方式 / Usage

1. 啟動本機或雲端 [n8n](https://n8n.io/) 實例。
2. 於 n8n 工作區點擊「Import from File」，分別匯入 `PubmedSeeker.json` 與 `PaperReviewer.json`。
3. 填入您的 Zotero API Key 與 OpenAI/Claude API Key。
4. 啟動工作流（Activate）即可全自動化運行。

## 📄 授權 / License

MIT License
