---
layout: page
---

### 説明

USの電話番号フォーマット

### 使い方

    number_to_phone(数値, オプション={})

### オプション

| オプション         | 説明         | デフォルト値 |
| ------------- | ---------- | ------ |
| :area_code    | エリアコード     |        |
| :delimiter    | 桁区切り文字     | -      |
| :extension    | 末尾に追加する拡張子 |        |
| :country_code | カントリーコード   |        |
| :pattern      | フォーマット     |        |
| :raise        | エラーの場合に例外  |        |

### 例

    number_to_phone(123456789)
    # 123456789.000

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/number_helper.rb#L62)
