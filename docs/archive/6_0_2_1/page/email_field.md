---
layout: page
---
### 説明
メールアドレス入力ボックスを生成

### 使い方
    email_field(オブジェクト名, メソッド名 [, オプション or HTML属性 or イベント属性])

#### f.object
    f.email_field(メソッド名 [, オプション or HTML属性 or イベント属性])

### オプション

オプション        | 説明
-------------|--------------------
:disabled    | 無効化
:size        | フォームの幅
:maxlength   | 入力フィールドに入力可能な最大文字数
:placeholder | フォーカスが当たるまで表示される文字列

### HTML属性

HTML属性      | 説明
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
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### email_field
##### メールアドレス入力ボックスを生成
    email_field :page, :email
    # <input id="page_email" name="page[email]" size="30" type="email" />

##### 初期値指定
    # @page.email = "test@example.com"
    email_field :page, :email
    # <input id="page_email" name="page[email]" size="30" type="email" value="test@example.com"/>

##### sizeの指定
    email_field :page, :email
    # <input id="page_email" name="page[email]" size="40" type="email"/>

#### f.email_field
##### メールアドレス入力ボックスを生成
    f.email_field :email
    # <input id="page_email" name="page[email]" size="30" type="email" />

##### 初期値指定
    # @page.email = "test@example.com"
    f.email_field :email
    # <input id="page_email" name="page[email]" size="30" type="email" value="test@example.com"/>

##### sizeの指定
    f.email_field :email, size: "40"
    # <input id="page_email" name="page[email]" size="40" type="email"/>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1506)
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L1878)