<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "1a4652c25be33e93506f16fdb3463b18",
  "translation_date": "2025-05-13T02:26:51+00:00",
  "source_file": "noise/noise-commands.md",
  "language_code": "tw"
}
-->
# Noise Commands

所有子指令都在 `//eznoise`  (`//ezn`) 底下 \
例如 `//eznoise list`

## `//eznoise ...`

### `list [SET]`

* `ALL`\
  列出所有可用的 noise 預設
* `DEFAULT`\
  列出所有預設的 plugin noise 預設
* `MINE`\
  列出所有使用者自訂的 noise 預設

### `save <presetName> <noise> [-f]`

以指定名稱儲存使用者自訂的 noise 預設。\
使用 `-f` 來覆寫已存在的 noise 預設。

### `delete <presetName>`

刪除與指定名稱相符的使用者自訂 noise 預設。

### `print <noise>`

在聊天中顯示指定 noise 預設的設定。

**免責聲明**：  
本文件係使用 AI 翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 所翻譯。雖然我們力求準確，但請注意，自動翻譯可能包含錯誤或不準確之處。原始文件之母語版本應視為權威來源。對於重要資訊，建議採用專業人工翻譯。我們不對因使用本翻譯而產生之任何誤解或誤譯負責。