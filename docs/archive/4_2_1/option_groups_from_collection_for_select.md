---
layout: page
---
### 説明
グループ分けされた選択肢を生成する

### 使い方
    options_groups_from_collection_for_select(オブジェクトの配列, タグを取得するメソッド, タグのlabel属性, value属性の項目, textの項目 [, デフォルト値])

### 使用できるフォームタグ
* form_for
* form_tag

### 例
#### オブジェクトをグループ化
    # @categories = Category.all
    <%= select_tag 'page[name]', option_groups_from_collection_for_select(@categories, :pages, :name, :id, :name) %>
    # <select id="page_name" name="page[name]"><optgroup label="Railsの基礎知識"><option value="1">Ruby on Railsとは</option>
    # <option value="2">規約</option>
    # <option value="3">ディレクトリ構造</option>
    # <option value="4">アプリケーション作成の流れ</option>
    # </optgroup><optgroup label="Rubyの基礎知識"><option value="5">Rubyとは</option></optgroup></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/form_options_helper.rb#L454)