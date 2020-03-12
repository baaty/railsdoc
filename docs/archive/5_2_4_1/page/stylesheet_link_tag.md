---
layout: archive_page
---
### 説明
外部スタイルシートを指定するリンクタグを生成

### 使い方
    stylesheet_link_tag(スタイルシートへのパス [, HTML属性 or イベント属性])

### HTML属性

HTML属性     | 説明                                  | デフォルト
----------|-------------------------------------|---------------------------------------
:href     | 関連ファイルの場所                         |
:hreflang | 関連ファイルの言語コードを指定                 |
:type     | 関連ファイルのMIMEタイプを指定                 | text/css
:media    | 関連ファイルの出力メディアのリンクタイプ              | screen
:rel      | この文章から見た、href属性で指定するリンク先の役割 | stylesheet
:rev      | href属性で指定するリンク先から見た、この文章の役割 |
:charset  | 関連ファイルの文字コード                      |
:target   | 関連ファイルを表示するウインドウ名                |
:id       | 要素固有の識別子                       |
:class    | 要素を分類するクラス名                      |
:title    | 要素の補足情報                         |
:style    | 要素の補足情報                         |
:dir      | 表記方向                              |
:lang     | 基本言語                              |

### イベント属性

イベント属性     | 説明
-------------|--------------------
:onclick     | クリックされた時
:ondblclick  | ダブルクリックされた時
:onmousedown | マウスのボタンが押し下げられた時
:onmouseup   | マウスのボタンが離された時
:onmouseover | カーソルが重なった時
:onmousemove | カーソルが移動した時
:onmouseout  | カーソルが離れた時
:onkeypress  | キーが押されて離された時
:onkeydown   | キーが押し下げられた時
:onkeyup     | キーが離された時

### 例
#### 外部スタイルシートを指定するリンクタグを生成
    stylesheet_link_tag "style"
    # <link href="/assets/style.css" media="screen" rel="stylesheet" />

#### 拡張子まで指定
    stylesheet_link_tag "style.css"
    # <link href="/assets/style.css" media="screen" rel="stylesheet" />

#### URLで指定
    stylesheet_link_tag "http://www.example.com/style.css"
    # <link href="http://www.example.com/style.css" media="screen" rel="stylesheet" />

#### media属性を指定
    stylesheet_link_tag "style", media: "all"
    # <link href="/assets/style.css" media="all" rel="stylesheet" />

#### 印刷用CSSを設定
    stylesheet_link_tag "style", media: "print"
    # <link href="/assets/style.css" media="print" rel="stylesheet" />

#### 複数指定
    stylesheet_link_tag "random.styles", "/css/stylish"
    # <link href="/assets/random.styles" media="screen" rel="stylesheet" />
    # <link href="/css/stylish.css" media="screen" rel="stylesheet" />

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/asset_tag_helper.rb#L137)