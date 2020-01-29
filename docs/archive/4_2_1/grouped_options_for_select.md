---
layout: page
---
### 説明
配列・ハッシュから作成した選択肢をグループ化

### 使い方
    grouped_options_for_select(タグの配列 or ハッシュ [, 選択されたオプション[, 選択オプションの先頭に表示される文字列]])

### 使用できるフォームタグ
* form_for
* form_tag

### 例
#### タグの情報を配列で指定
    <%= select_tag 'page[name]', grouped_options_for_select([["基礎", [["Railsの基礎", "rails_base"], ["Rubyの基礎", "ruby_base"]]]]) %>
    # <select id="page_name" name="page[name]"><optgroup label="基礎"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></optgroup></select>

#### タグの情報をハッシュで指定
    <%= select_tag 'page[name]', grouped_options_for_select({"基礎" => [["Railsの基礎" ,"rails_base"], ["Rubyの基礎", "ruby_base"]]}) %>
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### 選択されたオプション
    <%= select_tag 'page[name]', grouped_options_for_select({"基礎" => [["Railsの基礎" ,"rails_base"], ["Rubyの基礎", "ruby_base"]]}, "rails_base") %>
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### 選択オプションの先頭に表示される文字列
    <%= select_tag 'page[name]', grouped_options_for_select({"基礎" => [["Railsの基礎" ,"rails_base"], ["Rubyの基礎", "ruby_base"]]}, "", "選択してください") %>
    # <select id="page_name" name="page[name]"><option value="">選択してください</option><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/form_options_helper.rb#L524)