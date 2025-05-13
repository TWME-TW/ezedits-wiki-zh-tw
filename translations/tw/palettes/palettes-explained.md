<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "8734204b547864b0ecc2e7c0881d4288",
  "translation_date": "2025-05-13T02:27:57+00:00",
  "source_file": "palettes/palettes-explained.md",
  "language_code": "tw"
}
-->
# 調色盤說明

在 ezEdits 中，調色盤代表一組方塊清單，可用於多個指令中，且方塊的順序會被保留。

調色盤可以使用 **`#`** 前綴來存取使用者儲存的調色盤，或使用 **`##`** 來存取[內建預設調色盤](default-palettes.md)。

以下是範例供參考：

<figure><img src="../.gitbook/assets/palette_Grayscale.png" alt=""><figcaption><p>##灰階調色盤</p></figcaption></figure>

使用調色盤的功能包含：

* `//eztexture ...` - [貼圖指令](../commands/texturing.md)
* `#palette` - [調色盤遮罩](../masks-and-patterns/masks.md#palette-mask)
* `//ezbrush gradient ...` - [畫筆](../../../brushes-and-tools/brushes)

調色盤可以是簡單的方塊清單，或是透過多種修飾符建立：

* **`,`** - <mark style="color:orange;">**串接**</mark>：
  * 將一個方塊或調色盤加到前一個方塊或調色盤的尾端。\
    例如 `stone,dirt` 是由石頭和泥土兩個方塊組成的調色盤。`stone,##Grayscale` 是由石頭和 ##灰階 預設調色盤的方塊組成的調色盤。
* **`-`** - <mark style="color:orange;">**反轉**</mark>：
  * 將調色盤的順序反過來。\
    例如 `-##Grayscale` 是 ##灰階 預設調色盤的反向排列（從白色開始，而非黑色）
* **`(start:end)`** - <mark style="color:orange;">**子調色盤**</mark>：
  * 取回調色盤的一部分。\
    例如 `##Grayscale(1:8)` 會回傳 ##灰階 預設調色盤的前 8 個方塊。
* **`*`** - <mark style="color:orange;">**重複器**</mark>：
  * 重複前一段指定的次數。\
    例如 `gold_block*10,diamond_block` 會回傳由 10 個金塊組成的調色盤，接著是一個鑽石塊。
* **`[]`** - <mark style="color:orange;">**群組**</mark>：
  * 將調色盤群組在一起，讓修飾符可以將它們視為單一調色盤。\
    例如 `-##Grayscale,gold_block` 會回傳反轉順序的 ##灰階 預設調色盤，尾端加上一個金塊。`-[##Grayscale,gold_block]` 則會把金塊放在最前面。
* **`=`** - <mark style="color:orange;">**結果**</mark>：
  * 允許調色盤在需要時以列表形式完成輸入。

### 影片教學

[MegRae](https://megrae.art/) 也製作了調色盤的教學影片：

{% embed url="https://youtu.be/VGsTle3g9AU" %}

**免責聲明**：  
本文件係使用 AI 翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 所翻譯。雖然我們力求準確，但請注意，自動翻譯可能包含錯誤或不準確之處。原始文件之母語版本應視為權威來源。對於重要資訊，建議採用專業人工翻譯。本公司不對因使用此翻譯而產生之任何誤解或誤譯負責。