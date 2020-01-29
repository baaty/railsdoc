---
layout: page
---
### 説明
サニタイズ

### 使い方
    sanitize(文字列 [, tags => "許可するHTMLタグ名", attributes => "許可するHTML属性名"])

### 例
#### pとbrタグのみ有効にする
    <%= sanitize "<h2>Ruby on Railsドキュメント (v3.1.0)</h2><p class="rails">RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説<br />メソッドが使用できるオプションや使用例などを多く取り入れました</p>", :tags => %w(p br)
    # Ruby on Railsドキュメント (v3.1.0)<p>RubyとRails3の基本からビュー、モデル、コントローラなどを、分かりやすく解説<br />メソッドが使用できるオプションや使用例などを多く取り入れました</p>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/83e9005bf09974c004ded137eac679399add7f0e/actionview/lib/action_view/helpers/sanitize_helper.rb#L83)