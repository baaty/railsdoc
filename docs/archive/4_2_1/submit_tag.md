---
layout: page
---
### 説明
サブミットボタンを生成

### 使い方
    submit_tag([ボタンの名前 , オプション])

### 使用できるフォームタグ
* form_for
* form_tag

### オプション

オプション         | 説明
------------- | -------------------
:data         | Data要素のカスタマイズ
:disabled     | フォームの項目の利用禁止
:confirm      | 確認ダイアログに表示する文字列
:disabled     | ボタンを無効化
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

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/dd7af2c413a06ea44e50abf0df205314ba1bfc98/actionview/lib/action_view/helpers/form_tag_helper.rb#L441)

### その他
引数を指定しないと、対象のモデルが保存済みかを調べて、「Create モデル名」「Update モデル名」のどちらかを表示