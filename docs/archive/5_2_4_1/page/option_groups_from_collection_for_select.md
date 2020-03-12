---
layout: archive_page
---
### 説明
グループ分けされた選択ボックスを生成

### 使い方
    option_groups_from_collection_for_select(要素の配列 or ハッシュ, グループメソッド, グループのラベル属性の項目, value属性の項目, textの項目 [, 選択された要素])

### 例
#### グループ分けされた選択ボックスを生成
    option_groups_from_collection_for_select(@continents, :countries, :name, :id, :name, 3)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L461)