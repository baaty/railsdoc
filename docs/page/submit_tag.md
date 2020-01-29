---
layout: page
---
### 説明
サブミットボタンを生成

### 使い方
    submit_tag([ボタンの名前 , オプション or HTMLオプション])

### オプション

オプション      | 説明
------------- | -------------------
:data         | Data要素のカスタマイズ
:disabled     | 無効化

### HTMLオプション

オプション      | 説明
------------- | -------------------
:confirm      | 確認ダイアログに表示する文字列
:disable_with | ボタンを無効化したときに表示する文字列
:size         | フォームの幅
:maxlength    | 入力フィールドに入力可能な最大文字数
:accept       | フォームで受付可能なMIMEタイプ
:readonly     | フォームの内容変更禁止
:tabindex     | Tabキーによる入力欄の移動順
:accesskey    | フォームに移動するショートカットキー
:id           | 要素固有の識別子
:class        | 要素を分類するクラス名
:title        | 要素の補足情報
:style        | 要素の補足情報
:dir          | 表記方向
:lang         | 基本言語

### 例
    submit_tag
    # <input name="commit" data-disable-with="Save changes" type="submit" value="Save changes" />

    submit_tag "Edit this article"
    # <input name="commit" data-disable-with="Edit this article" type="submit" value="Edit this article" />

    submit_tag "Save edits", disabled: true
    # <input disabled="disabled" name="commit" data-disable-with="Save edits" type="submit" value="Save edits" />

    submit_tag "Complete sale", data: { disable_with: "Submitting..." }
    # <input name="commit" data-disable-with="Submitting..." type="submit" value="Complete sale" />

    submit_tag nil, class: "form_submit"
    # <input class="form_submit" name="commit" type="submit" />

    submit_tag "Edit", class: "edit_button"
    # <input class="edit_button" data-disable-with="Edit" name="commit" type="submit" value="Edit" />

    submit_tag "Save", data: { confirm: "Are you sure?" }
    # <input name='commit' type='submit' value='Save' data-disable-with="Save" data-confirm="Are you sure?" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L451)