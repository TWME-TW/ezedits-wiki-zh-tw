<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "6bb05f3885cef7299c4fba617437b09e",
  "translation_date": "2025-05-13T02:23:12+00:00",
  "source_file": "commands/selections.md",
  "language_code": "tw"
}
-->
## Selection Management Commands

所有子指令都在 `//ezselection`（`//ezsel`）之下\
例如 `//ezsel list`

### `list [-g]`

列出使用者所有已儲存的選取範圍。點擊選取範圍名稱以載入。\
使用 `-g` 可依類型分組選取範圍。

### `load <selection>`

從玩家已儲存的選取範圍清單中取回先前儲存的選取範圍。

### `save <selectionName> [-f]`

以指定名稱儲存使用者目前的選取範圍。\
使用 `-f` 可覆蓋已存在的儲存選取範圍。

### `delete <selectionName>`

刪除使用者指定名稱的選取範圍。

**免責聲明**：  
本文件係使用 AI 翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 進行翻譯。雖然我們致力於翻譯的準確性，但請注意，自動翻譯可能會有錯誤或不準確之處。原始文件的母語版本應視為權威來源。對於重要資訊，建議採用專業人工翻譯。我們不對因使用本翻譯而產生的任何誤解或誤釋負責。