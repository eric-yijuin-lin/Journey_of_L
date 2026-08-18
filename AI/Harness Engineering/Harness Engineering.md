#AI 
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
### [[Geometry TD 學習專案]]

## 基本習慣
- 先探查現況，再做看似無害的變更。
- 建議使用英文，原因：
	- 程式、套件與錯誤訊息通常是英文
	- 未來複製到其他專案比較容易
	- 可以減少技術名詞翻譯造成的歧義
	- (我自己猜的)稍微省錢
- 實作階段建議
	- 簡單無傷大雅小工作
		1. 直接進入 codex
		2. 要求 AI agent 讀取長期規範（AGENTS.md）與當前任務（task.md) 並回報理解
		3. 人類確認需求理解
		4. 允許開工
		5. 人工驗證（git 狀態、親自跑一次 commands、畫面驗收...等）
	- 高風險或多人協作
		1. 以唯讀沙盒模式開啟 codex
		   `codex --sandbox read-only --ask-for-approval never`
		2. 要求 AI agent 讀取長期規範（AGENTS.md）與當前任務（task.md) 並回報理解
		3. 人類確認需求理解
		4. 離開並重新以正常權限進入 codex
		5. 要求 AI agent 將理解寫入 implementation-plan.md
		6. 人類確認 implementation-plan
		7. 允許開工
		8. 人工驗證（git 狀態、親自跑一次 commands、畫面驗收...等）

### 重要檔案
- [[AGENTS.md]]
- [[task.md]]
