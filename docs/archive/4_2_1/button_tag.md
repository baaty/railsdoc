---
layout: page
---
### 説明
ボタンを生成

### 使い方
    button_tag([オプション, HTMLオプション]

### オプション

オプション     | 説明              | デフォルト
--------- | --------------- | -----
:data     | Data要素のカスタマイズ   |
:disabled | ボタンを無効化         |
:confirm  | 確認ダイアログに表示する文字列 |

### HTMLオプション

オプション      | 説明
---------- | -----------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:disabled  | 利用禁止
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
    button_tag
    # => <button name="button" type="submit">Button</button>

    button_tag(type: 'button') do
      content_tag(:strong, 'Ask me!')
    end
    # => <button name="button" type="button">
    #     <strong>Ask me!</strong>
    #    </button>

    button_tag "Checkout", data: { disable_with => "Please wait..." }
    # => <button data-disable-with="Please wait..." name="button" type="submit">Checkout</button>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L485)