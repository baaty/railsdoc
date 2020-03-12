---
layout: archive_page
---
### 説明
USの電話番号フォーマット

### 使い方
    number_to_phone(数値 [, オプション])

### オプション

オプション         | 説明              | デフォルト値
--------------|-------------------|-------
:area_code    | エリアコード            |
:delimiter    | 桁区切り文字       | -
:extension    | 末尾に追加する拡張子 |
:country_code | カントリーコード          |
:pattern      | フォーマット            |
:raise        | エラーの場合に例外     |

### 例
    number_to_phone(123456789)
    # 123456789.000

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/number_helper.rb#L62)