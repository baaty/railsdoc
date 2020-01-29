---
layout: page
---
### 説明
外部スタイルシートを指定するリンクタグを生成

### 使い方
    stylesheet_link_tag(スタイルシートへのパス [, HTMLオプション])

### HTMLオプション

オプション     | 説明                                        | デフォルト
--------- | ----------------------------------------- | --------------------------------------
:href     | 関連ファイルの場所                                 | app/assets/stylesheets/スタイルシートへのパス.css
:hreflang | 関連ファイルの[言語コードを指定](/html_base#言語コード)       |
:type     | 関連ファイルの[MIMEタイプを指定](/html_base#MIMEタイプ)   | text/css
:media    | 関連ファイルの出力メディアの[リンクタイプ](/html_base#リンクタイプ) | screen
:rel      | この文章から見た、href属性で指定するリンク先の役割               | stylesheet
:rev      | href属性で指定するリンク先から見た、この文章の役割               |
:charset  | 関連ファイルの文字コード                              |
:target   | 関連ファイルを表示するウインドウ名                         |
:id       | 要素固有の識別子                                  |
:class    | 要素を分類するクラス名                               |
:title    | 要素の補足情報                                   |
:style    | 要素の補足情報                                   |
:dir      | 表記方向                                      |
:lang     | 基本言語                                      |

### 例
#### 外部スタイルシートを指定するリンクタグを生成
    <%= stylesheet_link_tag "style" %>
    # <link href="/stylesheets/style.css" media="screen" rel="stylesheet" type="text/css" />

#### 拡張子を付けて指定
    <%= stylesheet_link_tag "style.css" %>
    # <link href="/stylesheets/style.css" media="screen" rel="stylesheet" type="text/css" />

#### 外部サイトのCSSを指定
    <%= stylesheet_link_tag "http://www.example.com/style.css" %>
    # <link href="http://www.example.com/style.css" media="screen" rel="stylesheet" type="text/css" />

#### mediaオプションをallで指定
    <%= stylesheet_link_tag "style", :media => "all" %>
    # <link href="/stylesheets/style.css" media="all" rel="stylesheet" type="text/css" />

#### 複数指定
    <%= stylesheet_link_tag "style1", "style2" %>
    # <link href="/stylesheets/style1.css" media="screen" rel="stylesheet" type="text/css" />
    # <link href="/stylesheets/style2.css" media="screen" rel="stylesheet" type="text/css" />

#### 関連ファイルの言語コードを指定
    <%= stylesheet_link_tag "style", :hreflang => :ja %>
    # <link href="/stylesheets/style.css" hreflang="ja" media="screen" rel="stylesheet" type="text/css" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L92)