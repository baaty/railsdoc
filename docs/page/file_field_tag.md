---
layout: page
---
### 説明
モデルと関連のないファイル選択ボックスを生成

### 使い方
    file_field_tag(要素名 [, オプション])

### オプション

オプション      | 説明
---------- | ------------------
:disabled  | 無効化
:multiple  | 複数選択可能
:accept    | フォームで受付可能なMIMEタイプ
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:readonly  | フォームの内容変更禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語
:value     | 初期値

### 例
#### ファイル選択ボックスを生成
    file_field_tag 'attachment'
    # <input id="attachment" name="attachment" type="file" />

#### class付与
    file_field_tag 'avatar', class: 'profile_input'
    # <input class="profile_input" id="avatar" name="avatar" type="file" />

#### 無効化
    file_field_tag 'picture', disabled: true
    # <input disabled="disabled" id="picture" name="picture" type="file" />

#### 初期値
    file_field_tag 'resume', value: '~/resume.doc'
    # <input id="resume" name="resume" type="file" value="~/resume.doc" />

#### 複数タイプ指定
    file_field_tag 'user_pic', accept: 'image/png,image/gif,image/jpeg'
    # <input accept="image/png,image/gif,image/jpeg" id="user_pic" name="user_pic" type="file" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_tag_helper.rb#L281)