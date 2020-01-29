---
layout: page
---
### 説明
ボタンを生成

### 使い方
    button(文字列 [, オプション, HTMLオプション]

### オプション

オプション       | 説明                                                                                | デフォルト
----------- | --------------------------------------------------------------------------------- | ------
:method     | HTTPメソッド(:get, :post, :put, :delete)を指定                                           | :post
:disabled   | ボタンを無効化                                                                           |
:confirm    | 確認ダイアログに表示する文字列                                                                   |
:remote     | Ajaxでリンクを処理                                                                       | submit
:form       | This hash will be form attributes                                                 |
:form_class | This controls the class of the form within which the submit button will be placed |

### HTMLオプション

オプション      | 説明
---------- | -----------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
:disabled  | 利用禁止
:tabindex  | Tabキーによる入力欄の移動順
:accesskey | 移動するショートカットキー
:usemap    | この画像に対応させるイメージマップ
:id        | 要素固有の識別子
:class     | 要素を分類するクラス名
:title     | 要素の補足情報
:style     | 要素の補足情報
:dir       | 表記方向
:lang      | 基本言語

### 例

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/477fae3eb3d3b3bfdbe28586fecb8578c0be4721/actionview/lib/action_view/helpers/form_helper.rb#L1857)