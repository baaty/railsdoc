---
layout: page
---
### 説明
タグを動的に生成
HTMLとERBが混ざってしまう場合などに使用するとすっきり表現できる

### 使い方
    content_tag(タグの名前 [, コンテンツ or オプション, オプション])

### 例
#### pタグを生成
    content_tag :p, "Hello world"
    # <p>Hello&nbsp;world</p>

#### divタグをclass名を付けて生成
    content_tag(:div, content_tag(:p, "Hello world!"), class: "strong")
    # <div class="strong"><p>Hello world!</p></div>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/tag_helper.rb#L270)