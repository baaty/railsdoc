---
layout: page
---
### 説明
グループ分けされた選択ボックスをデータベースから動的に生成

### 使い方
    option_groups_from_collection_for_select(要素の配列, グループメソッド, グループのラベル属性の項目, value属性の項目, textの項目 [, オプション])

### オプション

オプション  | 説明
--------- | ----------
:selected | 選択されたオプション

### 例
    option_groups_from_collection_for_select(@continents, :countries, :name, :id, :name, 3)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L461)