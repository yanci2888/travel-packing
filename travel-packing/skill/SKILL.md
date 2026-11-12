# SKILL.md - travel-packing 執行流程

1. Extract (資訊提取)
   - 提取對話中的 {旅遊地點}、{出發時間}、{住宿類型}、{特殊行程}。若有缺失，主動詢問。

2. Action (工具調用)
   - 依據提取到的條件：
     - 若出發日在 14 天內：國內呼叫 `get_taiwan_weather`；國外將地點轉為英文，呼叫 `get_global_weather`。
     - 若出發日超過 14 天：將國家轉為英文，呼叫 `get_historical_climate`。
     - 若為跨國旅遊：將國家轉為英文，呼叫 `get_plug_voltage`。

3. Match (知識對照)
   - 讀取 `references/packing-reference.md`。
   - 將獲取到的外部資料，套入 Reference 的標準進行比對。

4. Output (產出結果)
   - 簡述天氣與當地觀察後，嚴格依照 Reference 規定的 Markdown 格式產出清單。