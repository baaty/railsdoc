---
layout: page
---
### 説明
選択ボックスを生成

### 使い方
    モデル.select_tag(オブジェクト名, メソッド名, 要素(配列 or ハッシュ) [, オプション or HTMLオプション])

### オプション

オプション       | 説明 | デフォルト値
-------------- | ---- | ----
:multiple      | 複数選択を有効にするか |
:disabled      | 無効化 | false
:include_blank | 先頭に空の要素を追加するか |
:prompt        | 指定したオプションを先頭に追加 |

### HTMLオプション

オプション     | 説明
------------ | ----
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

### 例
    select_tag "people", options_from_collection_for_select(@people, "id", "name")
    # <select id="people" name="people"><option value="1">David</option></select>

    select_tag "people", options_from_collection_for_select(@people, "id", "name", "1")
    # <select id="people" name="people"><option value="1" selected="selected">David</option></select>

    select_tag "people", raw("<option>David</option>")
    # <select id="people" name="people"><option>David</option></select>

    select_tag "count", raw("<option>1</option><option>2</option><option>3</option><option>4</option>")
    # <select id="count" name="count"><option>1</option><option>2</option>
    # <option>3</option><option>4</option></select>

    select_tag "colors", raw("<option>Red</option><option>Green</option><option>Blue</option>"), multiple: true
    # <select id="colors" multiple="multiple" name="colors[]"><option>Red</option>
    # <option>Green</option><option>Blue</option></select>

    select_tag "locations", raw("<option>Home</option><option selected='selected'>Work</option><option>Out</option>")
    # <select id="locations" name="locations"><option>Home</option><option selected='selected'>Work</option>
    # <option>Out</option></select>

    select_tag "access", raw("<option>Read</option><option>Write</option>"), multiple: true, class: 'form_input', id: 'unique_id'
    # <select class="form_input" id="unique_id" multiple="multiple" name="access[]"><option>Read</option>
    # <option>Write</option></select>

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), include_blank: true
    # <select id="people" name="people"><option value="" label=" "></option><option value="1">David</option></select>

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), include_blank: "All"
    # <select id="people" name="people"><option value="">All</option><option value="1">David</option></select>

    select_tag "people", options_from_collection_for_select(@people, "id", "name"), prompt: "Select something"
    # <select id="people" name="people"><option value="">Select something</option><option value="1">David</option></select>

    select_tag "destination", raw("<option>NYC</option><option>Paris</option><option>Rome</option>"), disabled: true
    # <select disabled="disabled" id="destination" name="destination"><option>NYC</option>
    # <option>Paris</option><option>Rome</option></select>

    select_tag "credit_card", options_for_select([ "VISA", "MasterCard" ], "MasterCard")
    # <select id="credit_card" name="credit_card"><option>VISA</option>
    # <option selected="selected">MasterCard</option></select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L135)