# LLM Application & Data Engineering (ETL + NoSQL)

![Python](https://img.shields.io/badge/Python-3776AB?style=flat&logo=python&logoColor=white)
![MongoDB](https://img.shields.io/badge/MongoDB-47A248?style=flat&logo=mongodb&logoColor=white)
![LLM](https://img.shields.io/badge/LLM-Gemma%207B-blue)
![API](https://img.shields.io/badge/API-Whisper-red)

本倉庫展示了從 **端到端 (End-to-End) 資料工程** 到 **大語言模型 (LLM) 應用** 的實作流程。包含自動化新聞爬蟲系統與 NoSQL 資料庫整合，以及基於 AI 的影音內容自動化摘要工具。

## 📂 專案目錄

1. [AI 影音逐字稿與條列式摘要系統 (LLM & Whisper API)](#1-ai-影音逐字稿與條列式摘要系統-llm--whisper-api)
2. [多來源熱門新聞爬蟲與 MongoDB 資料整合系統](#2-多來源熱門新聞爬蟲與-mongodb-資料整合系統)

---

## 1. AI 影音逐字稿與條列式摘要系統
**技術棧：** `LLM (Gemma 7B)`, `Whisper API`, `Ollama`, `Python`, `Google Colab`

### 📌 專案說明
開發一個自動化工具，能從使用者指定的 YouTube URL 中提取音訊，並透過 AI 進行高精度的逐字稿轉換與智慧摘要，解決長影片資訊獲取效率低下的問題。

### 🛠 核心實作
- **自動化語音轉文本 (STT)**：串接 **Whisper API** 處理中英文音訊，實現精準的逐字稿提取。
- **LLM 文本校正與翻譯**：
    - **英文影片**：利用 LLM 自動將逐字稿翻譯為流暢中文。
    - **中文影片**：針對原始逐字稿（無標點）利用 LLM 進行**語義斷句與標點符號自動修正**。
- **智慧摘要生成**：導入 **Gemma 7B (via Ollama)** 模型，將冗長的逐字稿自動濃縮為結構化的 **條列式 (Bullet Points) 重點摘要**。

---

## 2. 多來源熱門新聞爬蟲與 MongoDB 資料整合系統
**技術棧：** `Requests`, `BeautifulSoup`, `NoSQL (MongoDB)`, `JSON`, `ETL`

### 📌 專案說明
建立一個自動化爬蟲系統，能從多個報社（如：東森、中時等）抓取即時熱門新聞，並將非結構化的網頁資料清洗、轉換後存入文件式資料庫，實現數據的持久化管理。

### 🛠 核心實作
- **多來源爬蟲引擎**：利用 `requests` 與 `BeautifulSoup` 針對不同報社的 DOM 結構進行解析，擷取標題、超連結、發表時間等核心欄位。
- **資料清洗與 JSON 轉換**：將爬取到的原始資訊標註資料來源，並封裝成標準的 **JSON 格式** 以利後續應用。
- **NoSQL 資料庫整合**：
    - 獨立架設 **MongoDB** 伺服器，設計彈性的 Document Schema。
    - 實作資料寫入與讀取驗證流程，確保資料在 NoSQL 環境中的一致性與完整性。

---

## 🚀 核心技能展示
- **非結構化資料處理**：具備處理網頁 HTML、影音逐字稿等非結構化資料的能力，並轉化為具商業價值的結構化資訊。
- **AI 代理與 API 整合**：熟練操作 LLM（如 Gemma/Llama-3）與 Whisper API，具備開發 AI 驅動之自動化工具的能力。
- **數據工程 (ETL)**：掌握從資料爬取 (Extract)、格式轉換 (Transform) 到資料庫儲存 (Load) 的完整流程。
- **環境部署**：具備在 Colab 環境中配置 Ollama 模型伺服器與 MongoDB 資料庫的實務經驗。

---
*備註：本專案僅供學術交流與技術展示使用，所有爬蟲行為均遵守相關規範。*
