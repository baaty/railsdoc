---
layout: page
---

### 説明

文字列を下記の条件で加工

- 文字列を<p>で括る
- 改行は<br />を付与
- 連続した改行は、</p><p>を付与

### 使い方

    simple_format(文字列, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション   | 説明             |
| ------------ | ---------------- |
| :sanitize    | サニタイズ       |
| :wrapper_tag | 文字列を囲むタグ |

### HTML属性

| HTML属性 | 説明                   |
| -------- | ---------------------- |
| :align   | 左右の配置             |
| :id      | 要素固有の識別子       |
| :class   | 要素を分類するクラス名 |
| :title   | 要素の補足情報         |
| :style   | 要素の補足情報         |
| :dir     | 表記方向               |
| :lang    | 基本言語               |

### イベント属性

| イベント属性 | 説明                             |
| ------------ | -------------------------------- |
| :onclick     | クリックされた時                 |
| :ondblclick  | ダブルクリックされた時           |
| :onmousedown | マウスのボタンが押し下げられた時 |
| :onmouseup   | マウスのボタンが離された時       |
| :onmouseover | カーソルが重なった時             |
| :onmousemove | カーソルが移動した時             |
| :onmouseout  | カーソルが離れた時               |
| :onkeypress  | キーが押されて離された時         |
| :onkeydown   | キーが押し下げられた時           |
| :onkeyup     | キーが離された時                 |

### 例

#### 文字列を下記の条件で加工

    <% text = <<EOL
    テキスト

    テキストテキスト
    EOL %>
    <%= simple_format(text) %>
    #=> <p>テキスト</p><p>テキストテキスト</p>

#### class名がtext1を付与

    <% text = <<EOL
    テキスト

    テキストテキスト
    EOL %>
    <%= simple_format(text, calss: "text1") %>
    #=> <p class="text1">テキスト</p><p class="text1">テキストテキスト</p>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L306)
