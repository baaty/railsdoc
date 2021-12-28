---
layout: page
---

### 説明

リンクを生成

### 使い方

    link_to(リンクテキスト=nil, オプション=nil, HTML属性=nil or イベント属性=nil, ブロック引数)

### オプション

| オプション      | 説明                                                        |
| --------------- | ----------------------------------------------------------- |
| :controller     | コントローラ名                                              |
| :action         | アクション名                                                |
| :anchor         | アンカーを指定                                              |
| :only_path      | trueなら、URL全体ではなくパス部分を返す(デフォルト値: true) |
| :trailing_slash | 末尾にスラッシュを付与                                      |
| :host           | URLのホストを指定                                           |
| :protocol       | URLのプロトコルを指定                                       |
| :user           | HTTP認証                                                    |
| :password       | HTTP認証                                                    |
| :data           | DATA要素                                                    |
| :method         | HTTPメソッド(:post, :delete, :patch, :put)の指定            |
| :remote         | Ajaxでリンクを処理                                          |

### HTML属性

| HTML属性  | 説明                                               |
| --------- | -------------------------------------------------- |
| :name     | アンカー名                                         |
| :href     | リンク先                                           |
| :hreflang | 関連ファイルの言語コードを指定                     |
| :type     | 関連ファイルのMIMEタイプを指定                     |
| :media    | 関連ファイルの出力メディアのリンクタイプ           |
| :rel      | この文章から見た、href属性で指定するリンク先の役割 |
| :rev      | href属性で指定するリンク先から見た、この文章の役割 |
| :charset  | 関連ファイルの文字コード                           |
| :shape    | ホットスポット領域の形状                           |
| :coords   | ホットスポットの形状の座標                         |
| :target   | 関連ファイルを表示するウインドウ名                 |
| :id       | 要素固有の識別子                                   |
| :class    | 要素を分類するクラス名                             |
| :title    | 要素の補足情報                                     |
| :style    | 要素の補足情報                                     |
| :dir      | 表記方向                                           |
| :lang     | 基本言語                                           |

### イベント属性

| イベント属性 | 説明                                   |
| ------------ | -------------------------------------- |
| :onclick     | クリックされた時                       |
| :ondblclick  | ダブルクリックされた時                 |
| :onmousedown | マウスのボタンが押し下げられた時       |
| :onmouseup   | マウスのボタンが離された時             |
| :onmouseover | カーソルが重なった時                   |
| :onmousemove | カーソルが移動した時                   |
| :onmouseout  | カーソルが離れた時                     |
| :onkeypress  | キーが押されて離された時               |
| :onkeydown   | キーが押し下げられた時                 |
| :onkeyup     | キーが離された時                       |
| :onfocus     | フォーカスされた時                     |
| :onblur      | フォーカスを失った時                   |
| :onselect    | 入力欄のテキストが選択された時         |
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### URLヘルパー指定

    link_to "Profile", profile_path(@profile)
    #=> <a href="/profiles/1">Profile</a>

#### コントローラとアクションを直接指定

    link_to "Profile", controller: "profiles", action: "show", id: @profile
    #=> <a href="/profiles/show/1">Profile</a>

#### リンクテキストをURL

    link_to nil, "http://example.com"
    #=> <a href="http://www.example.com">http://www.example.com</a>

#### idとclassを付与

    link_to "Articles", articles_path, id: "news", class: "article"
    #=> <a href="/articles" class="article" id="news">Articles</a>

#### クエリを含むURL

    link_to "Comment wall", profile_path(@profile, anchor: "wall")
    #=> <a href="/profiles/1#wall">Comment wall</a>

#### メソッド固定

    link_to("Destroy", "http://www.example.com", method: :delete)
    #=> <a href='http://www.example.com' rel="nofollow" data-method="delete">Destroy</a>

#### Data属性

    link_to "Visit Other Site", "http://www.rubyonrails.org/", data: { confirm: "Are you sure?" }
    #=> <a href="http://www.rubyonrails.org/" data-confirm="Are you sure?">Visit Other Site</a>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/url_helper.rb#L209)
