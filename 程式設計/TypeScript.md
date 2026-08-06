
## 雜項知識
- `project references` 是什麼？
	- TypeScript 的 **Project References（專案參照）**，是讓一個 `tsconfig.json` 宣告：
	  「這個 TypeScript 專案依賴哪些其他 TypeScript 專案。」
	- 感覺有點像以前 Visual Studio 在一個 Solution 中，把一個 C# Project 設定為另一個 C# Project 的參考
	- 可以把大專案拆成小專案，只編譯更改過的專案，提高編譯的效率