---
layout: page
---
### 説明
リンクを生成

### 使い方
    link_to(文字列, パス [, オプション, HTMLオプション])

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
#### newアクションへのリンク
    <%= link_to "新規作成", :controller => "pages", :action => "new" %>
    # <a href="/pages/new">新規作成</a>

#### 確認メッセージを表示
    <%= link_to "新規作成", {:controller => "pages", :action => "new"}, :confirm => "本当に移動しますか？" %>
    # <a href="/pages/new" data-confirm="新規作成してよろしいでしょうか？">新規作成</a>

#### 外部サイト(Ruby on Rails)へのリンク
    <%= link_to "Ruby on Rails", "http://rubyonrails.org/" %>
    # <a href="http://rubyonrails.org">Ruby on Rails</a>

#### class属性を設定
    <%= link_to "新規作成", { :controller => "pages", :action => "new'") }, { :class => "class_1" }  %>
    # <a href="/pages/new" class="class_1">新規作成</a>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/606ce3f907cbccd9159bb558c0b57433b42f3975/actionview/lib/action_view/helpers/url_helper.rb#L175)