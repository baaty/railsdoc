---
layout: page
---
### 説明
配列・ハッシュから選択肢を生成する

### 使い方
    options_for_select(タグの配列 or ハッシュ [, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

#### オプション

オプション     | 説明
--------- | ----------
:selected | 選択されたオプション

### 例
#### タグの情報を配列で指定
    <%= select_tag 'page[name]', options_for_select([["Railsの基礎", "rails_base"], ["Rubyの基礎", "ruby_base"]]) %>
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### タグの情報をハッシュで指定
    <%= select_tag 'page[name]', options_for_select({"Railsの基礎" => "rails_base", "Rubyの基礎" => "ruby_base"}) %>
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### 選択されたオプション
    <%= select_tag 'page[name]', options_for_select({"Railsの基礎" => "rails_base", "Rubyの基礎" => "ruby_base"}, :selected => "ruby_base") %>
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/form_options_helper.rb#L350)