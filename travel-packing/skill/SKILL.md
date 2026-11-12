# SKILL.md - travel-packing 執行流程

1. Extract (資訊提取)
   - 提取對話中的 {旅遊地點}、{出發時間}、{住宿類型}、{特殊行程}。若有缺失，主動詢問。

2. Action (工具調用)
   - 依據提取到的條件，參閱 TOOLS.md 的適用時機，呼叫對應的氣象與電壓連接器獲取實際資料。

3. Match (知識對照)
   - 讀取 `references/packing-reference.md`。
   - 將獲取到的外部資料，套入 Reference 的標準進行比對。

4. Output (產出結果)
   - 簡述天氣與當地觀察後，嚴格依照 Reference 規定的 Markdown 格式產出清單。