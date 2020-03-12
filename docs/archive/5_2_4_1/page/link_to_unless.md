---
layout: archive_page
---
### 説明
条件に一致しなかったらリンクを生成

### 使い方
    link_to_unless(条件式, リンクテキスト, url [, オプション, HTML属性 or イベント属性])

### オプション

オプション           | 説明                                      | デフォルト値
----------------|------------------------------------------|-------
:controller     | コントローラ名                                  |
:action         | アクション名                                   |
:anchor         | アンカー(URLの#以降)を指定                      |
:only_path      | trueなら、URL全体ではなくパス部分を返す              | true
:trailing_slash | 末尾にスラッシュを付与                           |
:host           | URLのホストを指定                              |
:protocol       | URLのプロトコルを指定                            |
:user           | HTTP認証                                  |
:password       | HTTP認証                                  |
:data           | DATA要素                                  |
:method         | HTTPメソッド(:get, :post, :put, :delete)の指定 |
:remote         | Ajaxでリンクを処理                             |

### HTML属性

HTML属性     | 説明
----------|------------------------------------------
:name     | アンカー名
:href     | リンク先
:href     | 関連ファイルの場所
:hreflang | 関連ファイルの言語コードを指定
:type     | 関連ファイルのMIMEタイプを指定
:media    | 関連ファイルの出力メディアのリンクタイプ
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
:onfocus     | フォーカスされた時
:onblur      | フォーカスを失った時

### 例
#### @pageが空じゃなかったら、編集のリンクを表示
    link_to_unless(@page.nil?, "編集", { controller: "pages", action: "edit" })

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/url_helper.rb#L408)