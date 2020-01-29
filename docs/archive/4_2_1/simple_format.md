---
layout: page
---
### 説明
文字列を下記の条件で加工

* 文字列を<p>で括る
* 改行は<br />を付与
* 連続した改行は、</p><p>を付与

### 使い方
    simple_format(文字列 [, HTMLオプション])

### HTMLオプション

オプション  | 説明
------ | -----------
:align | 左右の配置
:id    | 要素固有の識別子
:class | 要素を分類するクラス名
:title | 要素の補足情報
:style | 要素の補足情報
:dir   | 表記方向
:lang  | 基本言語

### オプション

オプション       | 説明
----------- | ----------
:sanitize   | サニタイズ
wrapper_tag | 文字列のラッパータグ

### 例
#### 基本的な使い方
    <% text = <<EOL
    テキスト

    テキストテキスト
    EOL %>
    <%= simple_format(text) %>
    # <p>テキスト</p>
    # <p>テキストテキスト</p>

#### class名がtext1を付与
    <% text = <<EOL
    テキスト

    テキストテキスト
    EOL %>
    <%= simple_format(text, :calss => "text1") %>
    # <p class="text1">テキスト</p>
    # <p class="text1">テキストテキスト</p>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0e50b7bdf4c0f789db37e22dc45c52b082f674b4/actionview/lib/action_view/helpers/text_helper.rb#L283)