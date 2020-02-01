---
layout: page
---
### 説明
特定のモデルに特化したフォームを生成

### 使い方
    form_tag(リンク先 [オプション or HTMLオプション]) do
    end

### オプション

オプション               | 説明
------------------- | -------------------------
:multipart          | マルチパートを指定
:method             | HTTPメソッドを指定
:authenticity_token | 認証トークンを指定
:remote             | Ajaxでリンクを処理
:enforce_utf8       | utf8用の非表示用を出力するか?

### HTMLオプション

オプション      | 説明
---------- | -----------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:disabled  | 無効化
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | 移動するショートカットキー
:usemap    | この画像に対応させるイメージマップ
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### 基本形(オプションなし)
    <%= form_tag('/users') do %>
    <% end %>
    # <form action="users" method="put">
    # </form>

#### putメソッド指定
    <%= form_tag('/users', method: :put) do %>
    <% end %>
    # <form action="users" method="post">
    # </form>

#### multipart指定
    <%= form_tag('/users', multipart: true) do %>
    <% end %>
    # <form action="users" method="post" enctype="multipart/form-data">
    # </form>

#### JavaScriptを使う
    <%= form_tag('/posts', remote: true) %>
    # <form action="/posts" method="post" data-remote="true">

#### 外部リソースへのForm
    form_tag('http://far.away.com/form', authenticity_token: "cf50faa3fe97702ca1ae")

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L71)