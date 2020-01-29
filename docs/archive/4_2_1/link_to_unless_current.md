---
layout: page
---
### 説明
現在のURLと一致しなかったらリンクを生成

### 使い方
    link_to_unless_current(文字列, url [, オプション, HTMLオプション])

### オプション

オプション   | 説明                                      | デフォルト
------- | --------------------------------------- | -----
:data   | DATA要素                                  |
:method | HTTPメソッド(:get, :post, :put, :delete)の指定 |
:remote | Ajaxでリンクを処理                             |

### HTMLオプション

オプション     | 説明
--------- | -----------------------------------------
:name     | アンカー名
:href     | リンク先
:href     | 関連ファイルの場所
:hreflang | 関連ファイルの[言語コードを指定](/html_base#言語コード)
:type     | 関連ファイルの[MIMEタイプを指定](/html_base#MIMEタイプ)
:media    | 関連ファイルの出力メディアの[リンクタイプ](/html_base#リンクタイプ)
:rel      | この文章から見た、href属性で指定するリンク先の役割
:rev      | href属性で指定するリンク先から見た、この文章の役割
:charset  | 関連ファイルの文字コード
:shape    | ホットスポット領域の形状
:coords   | ホットスポットの形状の座標
:target   | 関連ファイルを表示するウインドウ名
:id       | 要素固有の識別子
:class    | 要素を分類するクラス名
:title    | 要素の補足情報
:style    | 要素の補足情報
:dir      | 表記方向
:lang     | 基本言語

### 例
#### 現在のページだったらリンクを表示しない
    <%= link_to_unless_current "新規作成", :controller => "profiles", :action => "new" %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/606ce3f907cbccd9159bb558c0b57433b42f3975/actionview/lib/action_view/helpers/url_helper.rb#L359)