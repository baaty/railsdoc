---
layout: page
---
### 説明
ボタンを生成

### 使い方
    button(文字列 [, オプション or データ属性 or HTMLオプション]

### オプション

オプション     | 説明
----------|--------------
:data     | Data要素のカスタマイズ
:disabled | 無効化

### データ属性

オプション         | 説明
--------------|----------------
:confirm      | 確認ダイアログに表示する文字列
:disable_with | 送信時にクリック禁止

### HTMLオプション

オプション      | 説明
-----------|------------------
:name      | 名称
:size      | サイズ。ピクセル数で指定
:readonly  | 内容変更を禁止
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
#### ボタンを生成
    button("作成")
    # <button name='button' type='submit'>作成</button>

#### ブロックでボタンを生成
    button do
      content_tag(:strong, 'Ask me!')
    end
    # <button name='button' type='submit'>
    #   <strong>Ask me!</strong>
    # </button>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/form_helper.rb#L2471)