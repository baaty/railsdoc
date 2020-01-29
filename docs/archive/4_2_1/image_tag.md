---
layout: page
---
### 説明
イメージタグを生成

### 使い方
    image_tag(画像ファイルへのパス, [, (オプション or HTMLオプション)])

### オプション

オプション      | 説明                      | バージョン
---------- | ----------------------- | --------
:alt       | alt属性。省略時は、ファイル名から自動セット |
:size      | 画像サイズ(幅x高さ)             |
:mouseover | マウスオーバー時に入れ替える画像        | rails3まで

### HTMLオプション

オプション     | 説明
--------- | -----------------
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

### 例
#### icon.png画像を表示
    <%= image_tag("icon.png") %>
    # <img alt="Icon" src="/images/icon.png" />

#### 16x16でaltがEdit Entryのicon.png画像を表示
    <%= image_tag("icon.png", :size => "16x16", :alt => "アイコン") %>
    # <img alt="アイコン" height="16" src="/images/icon.png" width="16" />

#### classがmenu_iconのicon.png画像を表示
    <%= image_tag("/icons/icon.gif", :class => "menu_icon") %>
    # <img alt="Icon" class="menu_icon" src="/images/icon.png" />

#### 画像のリンクを生成
    <%= link_to image_tag("logo.png"), :action => "index" %>
    # <a href="/blogs"><img alt="Logo" src="/images/logo.png" /></a>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/asset_tag_helper.rb#L208)