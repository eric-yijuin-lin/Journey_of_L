#AI
## 相關指令
- 在 Linux (WSL2) 安裝 Codex CLI
  `curl -fsSL https://chatgpt.com/codex/install.sh | sh`
- 確認安裝完成與版本
  ```
  source ~/.bashrc 
  command -v 
  codex codex --version
  ```
- 登入 Codex
  ```
  cd ~/projects/td-harness-lab
  codex
  ```
- 
## 錯誤訊息線索
### config.toml 警告
- 警告訊息
	- ⚠ Ignored unsupported project-local config keys in /mnt/c/xxx/config.toml: notify. If you want these settings to apply, manually set them in your user-level config.toml.
	- ⚠ MCP client for `node_repl` failed to start: MCP startup failed: No such file or directory (os error 2)
	- ⚠ MCP startup incomplete (failed: node_repl)
- 原因
	- 忘記先切目錄到 project 資料夾
- 解法
	- cd ~/projects/my-projects