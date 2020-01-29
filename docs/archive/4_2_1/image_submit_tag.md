---
layout: page
---
### 説明
画像サブミットボタンを生成

### 使い方
    image_submit_tag(値 [, オプション])

### オプション

オプション      | 説明
---------- | ------------------
:data      | Data要素のカスタマイズ
:disabled  | フォームの項目の利用禁止
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

#### 例
    image_submit_tag("login.png")
    # => <input alt="Login" src="/images/login.png" type="image" />

    image_submit_tag("purchase.png", disabled: true)
    # => <input alt="Purchase" disabled="disabled" src="/images/purchase.png" type="image" />

    image_submit_tag("search.png", class: 'search_button', alt: 'Find')
    # => <input alt="Find" class="search_button" src="/images/search.png" type="image" />

    image_submit_tag("agree.png", disabled: true, class: "agree_disagree_button")
    # => <input alt="Agree" class="agree_disagree_button" disabled="disabled" src="/images/agree.png" type="image" />

    image_submit_tag("save.png", data: { confirm: "Are you sure?" })
    # => <input alt="Save" src="/images/save.png" data-confirm="Are you sure?" type="image" />

##### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L531)