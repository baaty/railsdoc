---
layout: page
---
### 説明
ボタンでリンクを生成

### 使い方
    button_to(文字列 [, オプション, HTMLオプション]

### オプション

オプション       | 説明                                                                                | デフォルト
----------- | --------------------------------------------------------------------------------- | ------
:method     | HTTPメソッド(:get, :post, :put, :delete)を指定                                           | :post
:disabled   | ボタンを無効化                                                                           |
:data       | DATA属性                                                                            |
:remote     | Ajaxでリンクを処理                                                                       | submit
:form       | This hash will be form attributes                                                 |
:form_class | This controls the class of the form within which the submit button will be placed |
:paramss    | Hash of parameters to be rendered as hidden fields within the form                |

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
#### 新規作成ボタンを生成
    <%;= button_to "新規作成", :action => "new" %>
    # <form method="post" action="/blogs/new"  class="button_to"><div><input type="submit" value="新規作成" /><input name="authenticity_token" type="hidden" value="xxx" /></div></form>

#### 確認ダイヤログ付きで削除ボタンを生成
    <%= button_to "削除", { :action => "destroy", :id => @page.id }, :confirm => "本当に削除しますか?", :method => :delete %>
    # <form method="post" action="/blogs/1"  class="button_to"><div><input name="_method" type="hidden" value="delete" /><input data-confirm="本当に削除しますか？" type="submit" value="削除" /><input name="authenticity_token" type="hidden" value="xxx" /></div></form>

#### 作成ボタンをAjaxで生成
    <%= button_to "作成",  {:action => "create",} {:remote => true} %>
    # <form method="post" action="/blogs" data-remote="true" class="button_to"><div><input type="submit" value="create" /><input name="authenticity_token" type="hidden" value="xxx" /></div></form>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/606ce3f907cbccd9159bb558c0b57433b42f3975/actionview/lib/action_view/helpers/url_helper.rb#L279)