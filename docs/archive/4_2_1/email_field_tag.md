---
layout: page
---
### 説明
メールアドレス入力ボックスを生成

### 使い方
    email_field_tag(要素名 [, 値, オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション      | 説明
---------- | ------------------
:size      | フォームの幅
:maxlength | 入力フィールドに入力可能な最大文字数
:accept    | フォームで受付可能なMIMEタイプ
:readonly  | フォームの内容変更禁止
:disabled  | フォームの項目の利用禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | フォームに移動するショートカットキー
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例
#### 基本形(オプションなし)
    <%= email_field_tag 'page[email]' %>
    # <input id="page_email" name="page[email]" type="email" />

#### 初期値指定

    # @page.email = "test@example.com"
    <%= email_field_tag 'page[email]', @page.email %>
    # <input id="page_email" name="page[email]" type="email" value="test@example.com"/>

#### sizeの指定

    <%= email_field_tag 'page[email], '', size =>> "40" %>
    # <input id="page_email" name="page[email]" size="40" type="email"/>

### email_fieldとemail_field_tagの違い
* size属性がつく
* POSTパラメータがハッシュ形式

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L741")