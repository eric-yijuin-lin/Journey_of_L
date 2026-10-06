因為自己在 DigitalOcean 上的 vsftpd 金鑰常常在搞丟，加上有時候莫名其妙從可以連變成不能連，再從不能連變成可以連 (中間沒做任何更動)，所以決定實驗看看 AI 推薦的 rclone

## 簡易步驟
### 一、安裝 rclone
1. 先更新 apt 不然可能會卡住 
   `curl https://rclone.org/install.sh | bash`
2. 如果之前有手動安裝，有可能會找不到 bin，可以先試試看清除 快取
   `hash -r`
3. 確認安裝成功 & 版本
   `rclone version`
### 二、設定 remote
1. 執行 `rclone config`
2. 輸入 n (選擇 New remote)
3. 取一個名字
4. 選擇雲端硬碟代碼，本筆記使用 Google Drive (24)
5. 取得 credential (**介面一直在改版，就盡量找相關的**)
	1. 進入 Google Cloud Console
	2. 找到 Google Drive API 並啟用 (如果還沒的話)
	3. 進入 OAuth screen
	4. 建立 client (如果沒有的話)
	5. 選取 client
	6. 取得 client_id 與 client_secrete
6. 輸入 client_id 與 client_secrete
7. 選擇要賦予的權限 (目前選 1，因為好像不支援開一個資料夾封住 rclone)
8. service account file 留白，因為目前用 client_id + client_secret
9. 設定進階選項
	1. 輸入 y 進入 advcanced config
	2. 除了 root_folder_id 其他選項都直接 enter 留白
	3. 到 Google Drive 找到目標資料夾
	4. 從網址複製 folder_id
10. 離開進階選項後，選擇不要用瀏覽器授權 (Use web browser to automatically authenticate rclone with remote? -> No)
11. 用瀏覽器取得 Rclone 驗證碼
	1. 到一台有瀏覽器的電腦，從官網下載 Rclone 執行檔
	2. 開啟 CMD 或 powershell 並執行 rclone.exe
	3. rclone 會打開瀏覽器，進行驗證（如果 client_id 新建，Google 會因為新建的 + 要求很高的權限，警告這個應用沒有被驗證，評估之後選擇繼續）
	4. 完成後，回到 CMD 或 powershell，複製 token
	5. 貼回 Ubuntu rclone

### 三、常用指令
- 顯示資料夾
  `rclone lsd 設定的硬碟名稱`
- 