---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/text_helper.rb#L132)