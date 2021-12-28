---
layout: page
---
### 説明
画像サブミットボタンを生成

### 使い方
    image_submit_tag(値 [, オプション or HTML属性 or イベント属性])

### オプション

オプション     | 説明
----------|--------------
:data     | Data要素のカスタマイズ
:disabled | 無効化

### HTML属性

HTML属性      | 説明
-----------|-------------------
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
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
#### 画像サブミットボタンを生成
    image_submit_tag("login.png")
    # <input alt="Login" src="/images/login.png" type="image" />

#### class属性を付与
    image_submit_tag("search.png", class: 'search_button', alt: 'Find')
    # <input alt="Find" class="search_button" src="/images/search.png" type="image" />

#### 無効化
    image_submit_tag("agree.png", disabled: true, class: "agree_disagree_button")
    # <input alt="Agree" class="agree_disagree_button" disabled="disabled" src="/images/agree.png" type="image" />

#### data要素
    image_submit_tag("save.png", data: { confirm: "Are you sure?" })
    # <input alt="Save" src="/images/save.png" data-confirm="Are you sure?" type="image" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L555)