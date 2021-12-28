---
layout: page
---
### 説明
モデルと関連のないボタンを生成

### 使い方
    button_tag([オプション or データ属性 or HTML属性 or イベント属性])

### オプション

オプション     | 説明
----------|--------------
:data     | Data要素のカスタマイズ
:disabled | 無効化

### データ属性

オプション         | 説明
--------------|----------------
:confirm      | 確認ダイアログに表示する文字列
:disable_with | 送信時にクリック禁止

### HTML属性

HTML属性   | 説明
-----------|-------------------
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
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

### 例
#### ボタンを生成
    button_tag
    # <button name="button" type="submit">Button</button>

#### リセットボタンを生成
    button_tag 'Reset', type: 'reset'
    # <button name="button" type="reset">Reset</button>

#### ボタンにstringダグを含める
    button_tag(type: 'button') do
      content_tag(:strong, 'Ask me!')
    end
    # <button name="button" type="button">
    #  <strong>Ask me!</strong>
    # </button>

#### データ属性を指定
    button_tag "Checkout", data: { disable_with: "Please wait..." }
    # <button data-disable-with="Please wait..." name="button" type="submit">Checkout</button>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L509)