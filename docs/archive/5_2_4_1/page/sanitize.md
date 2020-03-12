---
layout: archive_page
---
### 説明
サニタイズ

### 使い方
    sanitize(文字列 [,  オプション])

### オプション

名前         | 説明
----------- | ----
:tags       | 許可するHTMLタグ名
:attributes | 許可するHTML属性名
:scrubber   | スクラブ指定

### 例
#### サニタイズ
    sanitize "<h2>Ruby on Railsドキュメント</h2>"

#### 許可するHTMLタグを指定
    sanitize @comment.body, tags: %w(strong em a), attributes: %w(href)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/sanitize_helper.rb#L82)