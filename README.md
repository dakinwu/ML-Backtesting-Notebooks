# Practical Python for Algorithmic Trading

這個專案是一組以 Jupyter Notebook 為核心的量化交易實作與教學筆記，涵蓋資料前處理、機器學習分類與回歸、策略回測、參數優化、過擬合分析，以及 Walk-Forward 驗證。另包含一個獨立的 `TQQQ` 回撤到前高(mean reversion)策略回測。

**Notebook 導覽**
- `01_Data Preprocessing.ipynb`：資料前處理
- `02_Machine Learning Classification Model.ipynb`：分類模型
- `03_1_Backtesting ML Classification-Based.ipynb`：分類策略回測
- `03_2_Backtesting ML Classification-Based.ipynb`：挑戰題，其他資料集回測
- `04_Machine Learning Regression Model.ipynb`：回歸模型
- `05_Backtesting ML Regression-Based.ipynb`：回歸策略回測
- `06_Interpret Backtesting Strategy.ipynb`：策略解讀
- `07_Optimizing Strategy Parameters.ipynb`：策略參數優化
- `08_1_Smart Optimization to Save Computing Time.ipynb`：節省計算時間的優化技巧
- `08_2_Smart Optimization to Save Computing Time.ipynb`：挑戰題，其他資料集優化
- `09_1_The Overfitting Problem.ipynb`：過擬合問題
- `09_2_The Overfitting Problem.ipynb`：挑戰題，其他資料集過擬合
- `10_1_Walk Forward Regression.ipynb`：Walk-Forward 回歸回測
- `10_2_Walk Forward Regression.ipynb`：挑戰題，其他資料集 Walk-Forward
- `TQQQ_Drawdown_Peak_Backtest.ipynb`：TQQQ 回撤到前高均值回歸回測

**快速開始**
1. 建立與啟用虛擬環境。
2. 安裝主要套件。
3. 以 Jupyter 開啟並依序執行 Notebook。

```powershell
python -m venv .venv
.\.venv\Scripts\Activate.ps1
pip install numpy pandas scikit-learn backtesting yfinance plotly matplotlib scikit-optimize jupyter
jupyter lab
```

**報表與產出**
- `reports_backtesting/`：回測報表 HTML，例如 `classification.html`、`regression.html`、`walk_forward_anchored.html` 等
- `plot.html`：互動式圖表輸出
- `models/`：已訓練模型（`.pkl`）

**專案結構**
- `data/`：範例資料集（股票/加密貨幣/企業關聯資料）
- `models/`：模型權重與序列化輸出
- `reports_backtesting/`：回測結果報表
- `strategies.py`：回歸與 Walk-Forward 策略實作（`backtesting` 套件）
- `src/`：圖表與補充資源

**注意事項**
本專案用於學習與研究，不構成任何投資建議。若需更新或替換資料集，請在 `data/` 內放置新檔案並依 Notebook 指示調整。
