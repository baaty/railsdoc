---
layout: page
---
### 説明
USの電話番号フォーマット

### 使い方
    number_to_phone(数値 [, オプション])

### オプション

オプション         | 説明         | デフォルト
------------- | ---------- | -----
:area_code    | エリアコード     |
:delimiter    | 桁区切り文字     | -
:extension    | 末尾に追加する拡張子 |
:country_code | カントリーコード   |

### 例
    <%= number_with_precision(123456789) %>
    # 123456789.000

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/44260581bec06e4ce05f3dd838c8b4736fc7eb1d/actionview/lib/action_view/helpers/number_helper.rb#L56)