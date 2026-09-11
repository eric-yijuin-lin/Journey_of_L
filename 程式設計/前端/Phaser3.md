#js #ts #frontend
# 基礎知識

## Scene 物件
- create()
	- Scene 物件被建立時會呼叫的函式
- update(time: number, delta: number)
	- 遊戲進行時會不斷呼叫的函式
	- time 會傳入一個高精度時戳（但不是  UTC），隨著遊戲進行增加
	- delta 會傳入距離上一個 frame 過了多少時間

# 指令參考
## 新增專案
1. 使用 [[vite]] 建立新 TS 樣板專案（中間多一對 -- 代表後面參數不要給 npm 而是給下一個程式）
  `npm create vite@latest phaser-game -- --template vanilla-ts`
2. 進到專案資料夾，安裝 TS 專案需要的 module
   `npm install`
3. 安裝 Phaser 3
   `npm install phaser@3`
4. 測試能否執行
   `npm run dev`