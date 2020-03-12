---
layout: archive_page
---
### 説明
文字列をキャメルケースに変換  
ファイル名からクラス名へ変換など

### 使い方
    camelize(文字列 [, オプション])

### オプション

オプション     | 説明 | デフォルト値
------------ | ----- | ---
:lower | ローワーキャメルケース |
:upper | キャメルケース | o

### 例
##### キャメルケース
    camelize('product')
    # "Product"

#### 「/」を含む文字の変換
    camelize('backoffice/session')
    # "Backoffice::Session"

#### ローワーキャメルケース
    camelize('active_record'. :lower)
    # "activeRecord"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/core_ext/string/inflections.rb#L91)