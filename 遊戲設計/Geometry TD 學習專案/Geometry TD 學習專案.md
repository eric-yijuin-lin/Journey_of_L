#ai
本專案主要用來學習 Harness Engineering，過程雖然可能把一些重要的遊戲設計基礎，記下或者連結到其他節點，但主要還是會著重在 AI Agent 的操作以及流程的驗證。

※ 專案名稱: ~/projects/td-harness-lab
## 選用技術
- [[Phaser3]]
- [[TypeScript]]
- [[Git]]
- [[Codex]]
- [[WSL]]

### [[學習地圖]]

| 階段  | 遊戲成果            | Harness Engineering 重點 |
| --- | --------------- | ---------------------- |
| 0   | 建立初始 repository | 環境探查、權限、Git 邊界         |
| 1   | Phaser 畫面能啟動    | `AGENTS.md`、專案命令、完成定義  |
| 2   | 顯示地圖與路徑         | 規格文件與架構決策              |
| 3   | 敵人沿路移動          | 小型任務切割、可觀察性            |
| 4   | 防禦塔攻擊敵人         | 驗收條件、單元測試              |
| 5   | 波次、金錢與生命        | 狀態管理、不變條件              |
| 6   | 勝敗與重新開始         | 垂直切片、端對端驗收             |
| 7   | 自動操作遊戲          | 瀏覽器測試、截圖與 log          |
| 8   | 重構與新增塔種         | Agent 自我 review、回歸測試   |
| 9   | 回顧整套流程          | 找出失敗模式、改良 Harness      |

### 專案架構
td-harness-lab/
├─ AGENTS.md
├─ README.md
├─ package.json
├─ src/
│  ├─ scenes/
│  ├─ entities/
│  ├─ systems/
│  ├─ config/
│  └─ main.ts
├─ tests/
├─ scripts/
│  └─ check.sh
└─ docs/
   ├─ product-spec.md
   ├─ architecture.md
   ├─ game-rules.md
   ├─ acceptance-tests.md
   ├─ current-task.md
   └─ decisions/