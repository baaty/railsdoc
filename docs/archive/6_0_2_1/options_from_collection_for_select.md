---
layout: page
---
### 説明
選択ボックスをデータベースから動的に生成

### 使い方
    options_from_collection_for_select(オブジェクトの配列, value属性の項目, textの項目 [, オプション])

### オプション

オプション  | 説明
--------- | ----------
:selected | 選択されたオプション

### 例
#### タグの情報をオブジェクトで指定
    select_tag 'page[name]', options_from_collection_for_select(@categories, :id, :name)
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎</option>
    # <option value="2">Rubyの基礎</option></select>

#### タグの情報をオブジェクトで指定(選択されたオプションを指定)
    select_tag 'page[name]', options_from_collection_for_select(@categories, :id, :name, 2)
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎</option>
    # <option value="2", selected="selected">Rubyの基礎</option></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L400)