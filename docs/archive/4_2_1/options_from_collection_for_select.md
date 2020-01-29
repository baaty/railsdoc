---
layout: page
---
### 説明
データベースから動的に選択肢を生成

### 使い方
    options_from_collection_for_select(オブジェクトの配列, value属性の項目, textの項目 [, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション     | 説明
--------- | ----------
:selected | 選択されたオプション

### 例
#### タグの情報をオブジェクトで指定
    # @categories = Category.all
    <%= select_tag 'page[name]', options_from_collection_for_select(@categories, :id, :name) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎</option>
    # <option value="2">Rubyの基礎</option></select>

#### タグの情報をオブジェクトで指定(選択されたオプションを指定)
    # @categories = Category.all
    <%= select_tag 'page[name]', options_from_collection_for_select(@categories, :id, :name, 2) %>
    # <select id="page_name" name="page[name]"><option value="1">Railsの基礎</option>
    # <option value="2", selected="selected">Rubyの基礎</option></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/form_options_helper.rb#L393)