## uv pip install 注意事項
- 適合用來快速測試或修緊急的 bug
- 如果要長期加入專案，還是要走 uv add，反則依賴不會被加入  project.toml、uv.lock，版空失效而無法直接在其他地方 uv sync

## uv 預設行為
- uv add 預設執行 sync
- uv sync 預設安裝 dev
## optional dependency
- 確定**系統需要這個功能**，但是某些環境並不需要這個功能的依賴時，可以只安裝特定依賴
- 加入依賴時，使用 `uv add PACKAGE --optional DEPENDENCY` 把某個套件加入某個依賴，例如 `uv add openai --optional agent`
- 同步依賴時，使用 `uv sync --extra DEPENDENCY` 來同步

## dev dependency
- 開發環境需要、部署環境不用時的依賴，例如 jupyter
- 加入依賴時，使用 uv add PACKAGE --dev
