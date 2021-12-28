---
layout: page
---
### 説明
ボタンでリンクを生成

### 使い方
    button_to(文字列 [, オプション, データ属性 or HTML属性 or イベント属性])

### オプション

オプション           | 説明                                       | デフォルト値
----------------|-------------------------------------------|-------
:controller     | コントローラ名                                   |
:action         | アクション名                                    |
:anchor         | アンカー(URLの#以降)を指定                       |
:only_path      | trueなら、URL全体ではなくパス部分を返す               | true
:trailing_slash | 末尾にスラッシュを付与                            |
:host           | URLのホストを指定                               |
:protocol       | URLのプロトコルを指定                             |
:user           | HTTP認証                                   |
:password       | HTTP認証                                   |
:method         | メソッド名(:post, :get, :delete, :patch, :put) | :post
:disabled       | 無効化                                     | false
:data           | カスタムData属性                               |
:remote         | Ajaxでリンクを処理                              |
:form           | フォーム属性                                   |
:form_class     | 送信ボタンのフォームクラス                            |
:params         | 非表示パラメータとして追加される値                    |

### データ属性

オプション         | 説明
--------------|----------------
:confirm      | 確認ダイアログに表示する文字列
:disable_with | 送信時にクリック禁止

### HTML属性

オプション      | 説明
---------- | -----------------
:method     | HTTPメソッド(:get, :post, :put, :delete)を指定 | :post
:disabled   | 無効化                                       | false
:data       | DATA属性                                      |
:remote     | Ajaxでリンクを処理                              | false
:form       | フォームの属性                                 |
:form_class | ボタンが配置されるフォーム                        |
:params    | パラメータをハッシュで渡す                         |
:name      | 名称                                            |
:size      | サイズ。ピクセル数で指定                            |
:readonly  | 内容変更を禁止                                    |
:accesskey | 移動するショートカットキー                          |
:usemap    | この画像に対応させるイメージマップ                   |
:id        | 要素固有の識別子                                  |
:class     | 要素を分類するクラス名                             |
:title     | 要素の補足情報                                    |
:style     | 要素の補足情報                                    |
:dir       | 表記方向                                         |
:lang      | 基本言語                                         |

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
:onselect    | 入力欄のテキストが選択された時
:onchange    | フォーカスを失う際に値が変化していた時

### 例
#### ボタンを生成
    button_to "新規作成", action: "new"
    # <form method="post" action="/blogs/new"  class="button_to"><div><input type="submit" value="新規作成" /><input name="authenticity_token" type="hidden" value="xxx" /></div></form>

#### コントローラを指定してボタンを生成
    button_to "新規作成", action: "new", controller: "items
    # <form method="post" action="/items/new"  class="button_to"><div><input type="submit" value="新規作成" /><input name="authenticity_token" type="hidden" value="xxx" /></div></form>

#### 確認ダイヤログ付きで削除ボタンを生成
    button_to 'Destroy', 'http://www.example.com', method: "delete", remote: true, data: { confirm: '本当に削除しますか?', disable_with: 'loading...' }
    # <form class='button_to' method='post' action='http://www.example.com' data-remote='true'>
    # <input name='_method' value='delete' type='hidden' />
    # <input value='Destroy' type='submit' data-disable-with='loading...' data-confirm='本当に削除しますか?' />
    # <input name="authenticity_token" type="hidden" value="10f2163b45388899ad4d5ae948988266befcb6c3d1b2451cf657a0c293d605a6"/>
    # </form>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/url_helper.rb#L300)