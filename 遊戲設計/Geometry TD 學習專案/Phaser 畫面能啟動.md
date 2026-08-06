由於 phaser + ts 有許多正確且完整的官方教學，AI agents 一般都能順利完成初始專案，並且能夠順利跑起專案。不過還是有一些值得留意跟學習的點。如下：
### 重要檔案
- index.html
	- 必須有一個 `<div id="app">`
	- 還要有一個 `<script type="module" scr="/src/main.ts"></script>`
- ts.config.json
	- noEmit: 不產生編譯結果檔案
	- strict: 嚴格檢查型別
- 