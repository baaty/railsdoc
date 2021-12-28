---
layout: page
---
### 説明
URL、スコープ、モデルなどからフォームタグを生成

### 使い方
    form_with(モデル or スコープ or URL [, オプション])

### オプション

オプション             | 説明                                    | デフォルト値
-------------------- | --------------------------------------- | ----
:url                 | URLを指定                                |
:method              | HTTPメソッドを指定                        | POST
:format              | フォーマットを指定                         | text/html
:scope               | スコープを指定                            |
:namespace           | 名前空間を指定                            |
:model               | モデルを指定                              |
:authenticity_token  | 認証トークンを指定                         |
:local               | リモート送信の無効                         | false
:skip_enforcing_utf8 | 送信時にutf8という名前の隠しフィールドを非表示 | false
:builder             | フォームで使うモデルをオーバライド            |
:id                  | id属性を指定                              |
:class               | class属性を指定                           |
:data                | data属性を指定                            |
:html                | id、class、data以外のHTMLタグ              |

### 例
#### URLからフォームを生成(form_tag的な使い方)
    <%= form_with url: posts_path do |form| %>
      <%= form.text_field :title %>
    <% end %>
    # <form action="/posts" method="post" data-remote="true">
    #  <input type="text" name="title">
    # </form>

#### モデルを指定してフォームを生成(form_for的な使い方)
    <%= form_with model: Post.new do |form| %>
      <%= form.text_field :title %>
    <% end %>
    # <form action="/posts" method="post" data-remote="true">
    # <input type="text" name="post[title]">
    # </form>

#### スコープを指定してフォームを生成
    <%= form_with scope: :post, url: posts_path do |form| %>
      <%= form.text_field :title %>
    <% end %>
    # <form action="/posts" method="post" data-remote="true">
    # <input type="text" name="post[title]">
    # </form>

#### 開始タグのみ生成
    form_with(model: @post, url: super_posts_path)

### form_forやform_tagとの違い
* デフォルトではid属性やclass属性は付与されない
* デフォルトでremote: trueが付与
* モデルの属性にない値も指定が可能

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L742)