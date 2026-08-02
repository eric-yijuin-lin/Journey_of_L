## 粗略理解
透過 feedforward (Guide) + feedback (Sensor) 一方面給予 AI 更明確的指令與理解 (Guide)，一方面透過監測 (Sensor) 讓 AI 知道自己沒做好的地方，並且持續修正。

Harness 約略可分為：
- Context: AI Agent 該做什麼
- Constrains: AI Agent 不允許做什麼
- Tools: AI Agent 能使用那些工具
- Feedback: AI Agent 如何知道結果
- Evidence: 結果的好壞如何證明
## 基本流程
- 想法 -> 任務邊界 -> AI Agent 執行 -> 自動化測試 -> 檢驗結果 -> 修正程式或 Harness
- 以做 Phaser3 + TS 為例：
	1. 決定遊戲規格
	2. 撰寫 AGENTS.md 與任務描述
	3. Codex 根據 Spec (AGENTS.md) 修改程式馬
	4. Typescript、lint、單元測試
	5. 啟動遊戲
	6. 瀏覽器測試、截圖、讀取遊戲狀態
	7. Codex 根據測試回饋修正
## 學習專案
### [[Geometry TD]]