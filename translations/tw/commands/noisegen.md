<!--
CO_OP_TRANSLATOR_METADATA:
{
  "original_hash": "bd41c3bf95af0093e76c3ffb3953ca30",
  "translation_date": "2025-05-13T02:22:23+00:00",
  "source_file": "commands/noisegen.md",
  "language_code": "tw"
}
-->
# Noisegen

所有子指令都在 `//eznoisegen`（`//noisegen`、`//ng`）底下\
例如 `//ng heightmap`

## `//eznoisegen ...`

### heightmap

<details>

<summary>Heightmap (2D)</summary>

**`//eznoisegen heightmap <palette> <noise> [height] [-z <zoom>] [-s <seed>] [-o <offset>] [-ct]`**

* **Palette**：指定要使用的方塊調色盤。
* **Noise**：定義要使用的噪音預設。
* **Height**（預設值：0）：控制從選取區域底部開始的高度。值為0時會採用選取區域的高度。_高度足夠時可在選取區域上方放置方塊_
* **-z**（預設值：1）：調整噪音的縮放等級。
* **-s**（預設值：-1）：設定噪音種子。
* **-o**（預設值：(0,0,0)）：以指定向量（X,Y,Z）偏移噪音生成座標。
* **-c**：使用時，會以選取區域的世界座標為噪音生成中心。
* **-t**：啟用平滑模式，特別針對調色盤中的雪、水和熔岩方塊 \[僅適用於 heightmap 模式]。

</details>

### terrain

<details>

<summary>Terrain (3D)</summary>

**`//eznoisegen terrain <palette> <noise> [height] [strength] [-z <scale>] [-s <seed>] [-l <smear>] [-o <offset>] [-c]`**

* **Palette**：指定要使用的方塊調色盤。
* **Noise**：定義要使用的噪音預設。
* **Height**（預設值：0）：控制從選取區域底部開始的高度。值為0時會採用選取區域的高度。_高度足夠時可在選取區域上方放置方塊_
* **Strength**（預設值：1,0.5,0）：接受最多3個以逗號分隔的數值，用以控制不同高度的噪音強度：
  * _`0.5` 代表各高度皆為50%強度_
  * _`0.7,0` 代表最底部為70%強度，頂部為0%，中間為平滑過渡_
  * _`0,1,0` 代表底部為0%，中間為100%，頂部為0%_
* **-z**（預設值：1）：調整噪音的縮放等級。
* **-s**（預設值：-1）：設定噪音種子。
* **-l**（預設值：0）：對3D噪音套用垂直模糊效果。
* **-o**（預設值：(0,0,0)）：以指定向量（X,Y,Z）偏移噪音生成座標。
* **-c**：使用時，會以選取區域的世界座標為噪音生成中心。

</details>

### advanced

<details>

<summary>Advanced</summary>

**`//eznoisegen <palette> <noise> [lowerThreshold] [upperThreshold] [-z <scale>] [-s <seed>] [-l <smear>] [-o <offset>] [-chnt]`**

* **Palette**：指定要使用的方塊調色盤。
* **Noise**：定義要使用的噪音預設。
* **Lower Threshold**（預設值：0）：設定噪音生成的下限閾值，支援 WorldEdit 表達式（範圍：0-1.0）。
* **Upper Threshold**（預設值：0.5）：設定噪音生成的上限閾值，支援 WorldEdit 表達式（範圍：0-1.0）。
* **-z**（預設值：1）：調整噪音的縮放等級。
* **-s**（預設值：-1）：設定噪音種子。
* **-l**（預設值：0）：對3D噪音套用垂直模糊效果。
* **-o**（預設值：(0,0,0)）：以指定向量（X,Y,Z）偏移噪音生成座標。
* **-c**：使用時，會以選取區域的世界座標為噪音生成中心。
* **-h**：啟用使用2D噪音的 heightmap 模式。\
  &#xNAN;_heightmap 模式僅支援 Cuboid、Cylinder 或 Polygon 區域類型。_
* **-n**：使用標準化（-1 到 1）且以選取區域為中心的座標進行噪音生成。
* **-t**：啟用平滑模式，特別針對調色盤中的雪、水和熔岩方塊 \[僅適用於 heightmap 模式]。

</details>

**免責聲明**：  
本文件係使用 AI 翻譯服務 [Co-op Translator](https://github.com/Azure/co-op-translator) 進行翻譯。雖然我們努力追求準確性，但請注意自動翻譯可能包含錯誤或不精確之處。原始文件之母語版本應視為權威來源。對於重要資訊，建議採用專業人工翻譯。我們不對因使用本翻譯所產生之任何誤解或誤譯負責。