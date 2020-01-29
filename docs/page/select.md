---
layout: page
---
### 説明
選択ボックスを生成

### 使い方
    モデル.select(オブジェクト名, メソッド名, 要素(配列 or ハッシュ) [, オプション or HTMLオプション])

### オプション

オプション       | 説明                         | デフォルト値
-------------- | ---------------------------- | ----
:multiple      | 複数選択を有効にするか           |
:disabled      | 無効化                        | false
:include_blank | 先頭に空の要素を追加するか        |
:prompt        | 選択されていない時に表示される文字 |

### HTMLオプション

オプション     | 説明
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

### 例
    select("post", "person_id", Person.all.collect { |p| [ p.name, p.id ] }, { include_blank: true })
    # <select name="post[person_id]" id="post_person_id">
    #   <option value=""></option>
    #   <option value="1" selected="selected">David</option>
    #   <option value="2">Eileen</option>
    #   <option value="3">Rafael</option>
    # </select>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_options_helper.rb#L164)