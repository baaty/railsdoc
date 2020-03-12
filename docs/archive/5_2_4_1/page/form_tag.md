---
layout: archive_page
---
### 説明
汎用的なフォームを生成  
form_withの利用を推奨(Rails5.1以降はform_forとform_tagはform_withに統合されたため)

### 使い方
    form_tag(リンク先 [オプション or HTML属性 or イベント属性]) do
    end

### オプション

オプション               | 説明
------------------- | -------------------------
:multipart          | マルチパートを指定
:method             | HTTPメソッドを指定
:authenticity_token | 認証トークンを指定
:remote             | Ajaxでリンクを処理
:enforce_utf8       | utf8用の非表示用を出力するか?

### HTML属性

HTML属性      | 説明
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

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_tag_helper.rb#L69)