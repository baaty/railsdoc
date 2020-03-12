---
layout: archive_page
---
### 説明
配列・ハッシュから選択肢を生成

### 使い方
    options_for_select(要素の配列 or ハッシュ [, 選択された要素])

### 例
#### タグの情報を配列で指定
    select_tag 'page[name]', options_for_select([["Railsの基礎", "rails_base"], ["Rubyの基礎", "ruby_base"]])
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### タグの情報をハッシュで指定
    select_tag 'page[name]', options_for_select({Railsの基礎: "rails_base", Rubyの基礎: "ruby_base"})
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### 選択されたオプション
    select_tag 'page[name]', options_for_select({Railsの基礎: "rails_base", Rubyの基礎: "ruby_base"}, selected: "ruby_base")
    # <select id="page_name" name="page[name]"><option value="rails_base">Railsの基礎</option>
    # <option value="ruby_base">Rubyの基礎</option></select>

#### 選択された要素あり
    options_for_select([['Japanese', 'JPN']], 'JPN')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L357)