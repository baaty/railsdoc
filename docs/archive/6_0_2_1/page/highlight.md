---
layout: page
---
### 説明
ハイライト

### 使い方
    highlight(文字列, ハイライトする文字列 [, highighter: ハイライトする文字列を置き換える形式)

### 例
#### 「Rails」をハイライトする
    highlight('RubyとRails6の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails')
    # Rubyと**Rails**3の基本からビュー、モデル、コントローラなどを、分かりやすく解説

#### ハイライトする文字列をリンクにする
    highlight('RubyとRails6の基本からビュー、モデル、コントローラなどを、分かりやすく解説', 'Rails', highlighter: '[¥1](/¥1)')
    # Rubyと[¥1](/¥1)3の基本からビュー、モデル、コントローラなどを、分かりやすく解説

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0e50b7bdf4c0f789db37e22dc45c52b082f674b4/actionview/lib/action_view/helpers/text_helper.rb#L125)