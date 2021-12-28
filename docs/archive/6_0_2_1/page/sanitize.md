---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/sanitize_helper.rb#L81)