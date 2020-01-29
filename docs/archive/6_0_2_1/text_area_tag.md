---
layout: page
---
### 使い方
    text_area_tag(要素名 [, エリア配下のテキスト, オプション or HTMLオプション])

### オプション

オプション      | 説明
---------- | ------------------
:size      | フォームの幅
:rows      | rowsの設定
:cols      | columnsの設定
:disabled  | 無効化
:escape    | HTMLをエスケープするか

### HTMLオプション

オプション   | 説明
---------- | ------------------
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

### 例
    text_area_tag 'post'
    # <textarea id="post" name="post"></textarea>

    text_area_tag 'bio', @user.bio
    # <textarea id="bio" name="bio">This is my biography.</textarea>

    text_area_tag 'body', nil, rows: 10, cols: 25
    # <textarea cols="25" id="body" name="body" rows="10"></textarea>

    text_area_tag 'body', nil, size: "25x10"
    # <textarea name="body" id="body" cols="25" rows="10"></textarea>

    text_area_tag 'description', "Description goes here.", disabled: true
    # <textarea disabled="disabled" id="description" name="description">Description goes here.</textarea>

    text_area_tag 'comment', nil, class: 'comment_input'
    # <textarea class="comment_input" id="comment" name="comment"></textarea>

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L347)