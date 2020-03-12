---
layout: archive_page
---
### 説明
選択ボックスを生成

### 使い方
    options_from_collection_for_select(要素の配列, value属性の項目, textの項目 [, 選択された要素])

### 例
#### 選択ボックスを生成
    options_from_collection_for_select @categories, :id, :name

#### 選択された要素あり
    options_from_collection_for_select @categories, :id, :name, 2

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L400)