# TOOLS.md - 工具呼叫設定

當你需要獲取外部資訊時，請根據情境與參數，呼叫對應的連接器網址：

### 1. `get_taiwan_weather` (連接器：台灣國內即時天氣)
- 適用時機：旅遊地點在台灣國內，且出發日在 7 天內。
- 連接器網址：`https://www.cwa.gov.tw/V8/C/W/County/index.html`
- 輸入參數：無（進入首頁後搜尋縣市）
- 讀取重點：擷取目標縣市的預測高低溫與降雨機率。

### 2. `get_global_weather` (連接器：全球即時預報)
- 適用時機：旅遊地點為國外，且出發日在 14 天內。
- 連接器網址：`https://www.timeanddate.com/weather/?query={location}`
- 輸入參數：`location` (請先將地點翻譯為英文)
- 讀取重點：擷取未來幾天的平均高低溫與天氣狀況。

### 3. `get_historical_climate` (連接器：全球歷史氣候)
- 適用時機：出發日期超過 14 天，或使用者僅提供出發月份。
- 連接器網址：`https://www.holiday-weather.com/country/{country}/`
- 輸入參數：`country` (請填入國家英文名稱，例如 `taiwan`、`japan`)
- 讀取重點：進入該國家的氣候總覽頁面後，尋找目標城市並擷取歷史平均氣溫。

### 4. `get_plug_voltage` (連接器：各國電壓與插座)
- 適用時機：確認跨國旅遊的基礎設施差異。
- 連接器網址：`https://www.power-plugs-sockets.com/tw/{country}/`
- 輸入參數：`country` (請填入國家英文名稱，例如 `japan`)
- 讀取重點：確認插座形狀（Type A~O）與標準電壓。