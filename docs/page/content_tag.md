---
layout: page
---
### 説明
タグを動的に生成
HTMLとERBが混ざってしまう場合などに使用するとすっきり表現できる

### 使い方
    content_tag(タグの名前 [, コンテンツ or HTMLオプション])

### HTMLオプション

オプション      | 説明
-----------|------------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:accesskey | 移動するショートカットキー
:usemap    | この画像に対応させるイメージマップ
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### pタグを生成
    content_tag :p, "Hello world"
    # <p>Hello&nbsp;world</p>

#### divタグをclass名を付けて生成
    content_tag(:div, content_tag(:p, "Hello world!"), class: "strong")
    # <div class="strong"><p>Hello world!</p></div>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/tag_helper.rb#L270)