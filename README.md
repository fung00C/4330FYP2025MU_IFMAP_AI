# FYP - S&P 500 指數與成分股價格預測

使用 **LSTM** 深度學習模型預測 S&P 500 指數及 487 檔成分股股價的畢業設計專案。

---

## 📋 專案介紹

本專案分為兩個主要部分：

- **SP500 Model**：訓練單一 LSTM 模型預測 S&P 500 指數未來價格
- **Stocks Models**：為 S&P 500 指數的 **487 檔成分股** 分別訓練獨立的 LSTM 模型

兩個 Notebook 皆包含完整的資料收集、前處理、特徵工程、模型訓練、評估與視覺化流程。

---

## ✨ 主要功能

- 使用 yfinance 自動下載 2008 年至 2025 年的歷史股價資料
- 計算多種技術指標（Technical Indicators）使用 TA-Lib
- 時間序列資料處理（Sliding Window）
- 資料正規化（MinMaxScaler）
- LSTM 模型建構與訓練（含 Dropout 防止過擬合）
- 模型評估（RMSE、MSE、MAE）
- 實際 vs 預測價格走勢圖視覺化
- 批量訓練並自動儲存所有股票模型

---

## 🛠 技術棧

- **程式語言**：Python 3.11
- **資料取得**：yfinance
- **技術指標**：TA-Lib
- **資料處理**：pandas, numpy
- **深度學習**：Keras / TensorFlow (LSTM)
- **視覺化**：matplotlib
- **環境**：Google Colab (GPU 加速)

---

## 📁 專案目錄結構

```bash
/
├── sp500_model_training.ipynb          # S&P 500 指數模型訓練主程式
├── stocks_model_training.ipynb         # 487 檔成分股模型訓練主程式
├── stock_category.json                 # S&P 500 成分股分類資料
├── models/                             # 訓練完成後的模型存放目錄
│   ├── SP500_model.h5
│   └── AAPL_model.h5
│   └── ...
├── input/                              # (可選) 原始 CSV 資料夾
└── README.md

