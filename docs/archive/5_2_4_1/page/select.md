---
layout: archive_page
---
### 説明
選択ボックスを生成

### 使い方
    select(オブジェクト名, メソッド名, 要素(配列 or ハッシュ) [, オプション or HTML属性 or イベント属性])

#### f.object
    f.select(メソッド名, 要素(配列 or ハッシュ) [, オプション or HTML属性 or イベント属性])

### オプション

オプション       | 説明                         | デフォルト値
-------------- | ---------------------------- | ----
:multiple      | 複数選択を有効にするか           |
:disabled      | 無効化                        | false
:include_blank | 先頭に空の要素を追加するか        |
:prompt        | 選択されていない時に表示される文字 |

### HTML属性

HTML属性     | 説明
------------ | -------------------------
:accept      | フォームで受付可能なMIMEタイプ
:readonly    | フォームの内容変更禁止
:tabindex    | Tabキーによる入力欄の移動順
:accesskey   | フォームに移動するショートカットキー
:id          | 要素固有の識別子
:class       | 要素を分類するクラス名
:title       | 要素の補足情報
:style       | 要素の補足情報
:dir         | 表記方向
:lang        | 基本言語

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
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### select
##### 選択ボックスを生成
    select("post", "person_id", Person.all.collect { |p| [ p.name, p.id ] }, { include_blank: true })
    # <select name="post[person_id]" id="post_person_id">
    #   <option value=""></option>
    #   <option value="1" selected="selected">David</option>
    #   <option value="2">Eileen</option>
    #   <option value="3">Rafael</option>
    # </select>

#### f.select
##### 選択ボックスを生成
    f.select :person_id, Person.all.collect { |p| [ p.name, p.id ] }, include_blank: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L164)
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/form_options_helper.rb#L822)