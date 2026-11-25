## 一、安裝 EIM
- 安裝方式二選一
	- 搜尋官網並下載安裝程式
	- 使用 CLI 指令安裝
		- AI 好像常推薦這個方式
		- 這個方式有可能遇到安裝完成後找不到 eim installer 的問題，需要手動確認下載路徑後再去找到它執行
## 二、安裝 ESP-IDF
### 安裝步驟
1. 選擇 Custom Installation
2. Select-Target
   根據手邊有的板子選擇安裝
3. Select IDF Version
   根據需求選擇版本，例如 5.X 版 CSI 範例多，所以選 5.X
4. Select Features
   根據需求選擇 optional feature，例如 ide 整合
5. 其他用預設即可
### 安裝的雷
- 過程如果中斷，有可能每次打開 EIM 都要 repair。重新安裝 IDF instance 可以解決

## 三、啟動 ESP-IDF Terminal 
執行 esp tool 安裝目錄下的啟動腳本
 `& 'C:\Espressif\tools\Microsoft.v5.5.5.PowerShell_profile.ps1'`
## 四、建立或開啟專案
### 建立新專案
1. 啟動 ESP-IDF Terminal
2. 移動到專案目錄
3. 執行 `idf.py create-project project_name`
4. 用 VS Code 打開資料夾
5. `ctrl + shift + P` -> `Select Current ESP-IDF Version`
6. 點選 Generate compile_json 選項，增加編譯效能
### 開啟現有專案
1. VS Code 打開資料夾
2. 開啟 VS Code 裡的 powershell -> deactivate -> `& 'C:\Espressif\tools\Microsoft.v5.5.5.PowerShell_profile.ps1'`
※ 目前不知道怎麼在原有的 uv 自動啟動 venv 情況下，啟動 ESP IDF Terminal，所以土炮先離開預設 venv，再進入 ESP-IDF Terminal

## 常用指令
- 建置專案
  `idf.py build`
- 燒錄專案
  `idf.py flash -p COMx`
- 監看序列輸出
  `idf.py monitor -p COMx`
- 停止序列輸出
  `ctrl + T -> X`
- 