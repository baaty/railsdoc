---
layout: page
---
### 説明
イメージタグを生成

### 使い方
    image_tag(画像ファイルへのパス, [, オプション or HTML属性 or イベント属性])

### オプション

オプション   | 説明
--------|----------------------
:size   | 画像サイズ(幅x高さ)
:srcset | ウィンドウサイズに合わせて画像を切り替える

### HTML属性

HTML属性     | 説明
----------|------------------
:src      | 画像ファイルのパス
:alt      | alt属性
:longdesc | 画像の説明文章のパス
:name     | 画像の名前
:ismap    | サーバサイド・イメージマップを使用
:usemap   | 画像に対応させるイメージマップ
:align    | 画像とテキストの配置
:width    | 画像の幅
:height   | 画像の高さ
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

### 例
#### icon.png画像を表示
    image_tag "icon.png"
    # <img alt="Icon" src="/images/icon.png" />

#### 16x16でaltがEdit Entryのicon.png画像を表示
    image_tag "icon.png", size: "16x16", alt: "アイコン"
    # <img alt="アイコン" height="16" src="/images/icon.png" width="16" />

#### classがmenu_iconのicon.png画像を表示
    image_tag "/icons/icon.gif", class: "menu_icon"
    # <img alt="Icon" class="menu_icon" src="/images/icon.png" />

#### 画像のリンクを生成
    link_to image_tag("logo.png"), action: "index"
    # <a href="/blogs"><img alt="Logo" src="/images/logo.png" /></a>

#### ウィンドウサイズに合わせて画像を切り替える
    image_tag "icon.png", srcset: { "icon_2x.png" => "2x", "icon_4x.png" => "4x" }
    # <img src="/assets/icon.png" srcset="/assets/icon_2x.png 2x, /assets/icon_4x.png 4x">

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/asset_tag_helper.rb#L340)