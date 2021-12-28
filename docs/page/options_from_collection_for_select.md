---
layout: page
---

### 説明

選択ボックスを生成

### 使い方

    options_from_collection_for_select(要素の配列, value属性の項目, textの項目, 選択された要素=nil)

### 例

#### 選択ボックスを生成

    options_from_collection_for_select @categories, :id, :name

#### 選択された要素あり

    options_from_collection_for_select @categories, :id, :name, 2

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L400)
