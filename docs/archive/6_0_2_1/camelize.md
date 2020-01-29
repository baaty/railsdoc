---
layout: page
---
### 説明
文字列をキャメルケースに変換

### 使い方
    文字列.camelize([オプション])

### オプション

オプション     | 説明
------------ | --
:lower | ローワーキャメルケース
:upper | キャメルケース

### 例
##### 「product」を変換
    "product".camelize
    # "Product"

#### 「backoffice/session」を変換
    "backoffice/session".camelize
    # "Backoffice::Session"

#### ローワーキャメルケース
    'active_record'.camelize(:lower)
    # "activeRecord"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/string/inflections.rb#L91)

