## 環境
### WSL
1. 在 powershell 啟動 WSL
2. (如果沒有) 安裝預設的 Ubuntu
   `wsl --install`
3. 切換到 user 資料夾
   `cd ~`
### Node.js
1. 更新 apt 並安裝 curl
   ```
   sudo apt update sudo 
   apt install -y curl
   ```
2. 安裝 NVM (node js 的版本管理器)
   `curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.6/install.sh | bash`
	- 此時很有可能碰到 WSL 預設使用 windows 現有 nvm, npm 而造成的錯誤
	- 關鍵錯誤資訊
		- npm error code ENOENT 
		  npm error syscall lstat 
		  npm error path C:\Users\xxxx\AppData\Roaming\npm 
		  npm error errno -4058 
		  npm error enoent ENOENT: no such file or directory
		- which node, which npm 出現
		  /mnt/c/Program Files/nodejs/node 
		  /mnt/c/Program Files/nodejs/npm
	- 解決方法
		- 重新載入 bash
		  `source ~/.bashrc
		- 然後確認 command，如果正確應該要出現 nvm
		  `command -v nvm`
3. 透過 NVM 安裝 Nodej.s LTS 版本並選用
   ```
   nvm install --lts # 安裝 LTS
   nvm use --lts # 使用 LTS
   nvm alias default 'lts/*' # 建立預設別名，不用每次的 use
   hash -r # 清除 bash 快取
   ```
## AI Agent
1. 安裝 Codex CLI (安裝完會直接問要不要執行，暫時不要)
   `curl -fsSL https://chatgpt.com/codex/install.sh | sh`
2. 確認版本
   ```
   source ~/.bashrc
   command -v codex
   codex --version
   ```
## 專案
1. 建立並移動到資料夾
   ```
   mkdir -p ~/projects/td-harness-lab 
   cd ~/projects/td-harness-lab
   ```
2. 安裝
