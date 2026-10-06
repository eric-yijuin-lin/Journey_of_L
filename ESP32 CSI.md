#Education 
## 官方 Demo
```
https://github.com/espressif/esp-csi.git
```
## 啟動步驟
1. clone repository
2. 用 VS Code 開啟專案
3. 設定 ESP-IDF 環境（參考[[ESP-IDF]]）
4. 設定板子 (以 esp32 為例)
   `idf.py set-target esp32`
5. 設定 menuconfig
	1. 在 (idf) Terminal 輸入 `idf.py menuconfig`
	2. 選擇 Example Connection Configuration
	3. 修改下方的 SSID 與 password
	4. Save (S) -> Exit (Q)
6. 設定 utf-8 編碼以避免輸出錯誤
   ` $env:PYTHONIOENCODING="utf-8"`
7. 