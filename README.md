本專案用於 **自動抓取康和期貨股票期貨保證金資料**，並與 **台灣期貨交易所（TAIFEX）股票代碼表** 進行整合，產出一份可直接用於量化分析或風控計算的完整資料表。
<img width="1301" height="506" alt="image" src="https://github.com/user-attachments/assets/ea74cd3c-235e-43dd-a92a-65bc8ac91c43" />

核心重點在於：
- 正確模擬 **ASP.NET WebForm 分頁**
- 自動偵測末頁，避免死迴圈
- 處理「一般 / 小型」股票期貨的對應關係
- 解決實務上常見的欄位型別與 merge 對不到問題

---

## 功能特色

- ✅ 自動抓取康和期貨「股票期貨保證金」**所有分頁**
- ✅ 支援 ASP.NET `__VIEWSTATE / __EVENTARGUMENT` 翻頁機制
- ✅ 以「頁面資料是否重複」作為 **安全終止條件**
- ✅ 自動辨識 **小型股票期貨（mini）**
- ✅ 與 TAIFEX 股票代碼表整合
- ✅ 輸出單一 `DataFrame`，可直接用於後續分析

---

## 資料來源

- **康和期貨**
  - 股票期貨保證金說明頁  
  - https://www.concordfutures.com.tw/Promote/ProductInformation/EquityFuturesMargin.aspx

- **台灣期貨交易所（TAIFEX）**
  - 股票期貨保證金適用標的  
  - https://www.taifex.com.tw/cht/5/stockMargining

---

## 環境需求

- Python 3.8+
- 套件：
  - `requests`
  - `pandas`
  - `beautifulsoup4`
  - `lxml`

安裝方式：

```bash
pip install requests pandas beautifulsoup4 lxml
