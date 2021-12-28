---
layout: page
---

### 説明

選択ボックスを生成

### 使い方

    select(オブジェクト名, メソッド名, 要素(配列 or ハッシュ)=nil, オプション={}, HTML属性={} or イベント属性={}, ブロック引数)

    # f.object
    f.select(メソッド名, 要素(配列 or ハッシュ)=nil, オプション={}, HTML属性={} or イベント属性={}, ブロック引数)

### オプション

| オプション     | 説明                               | デフォルト値 |
| -------------- | ---------------------------------- | ------------ |
| :multiple      | 複数選択を有効にするか             |              |
| :disabled      | 無効化                             | false        |
| :include_blank | 先頭に空の要素を追加(true or 文字列)         |              |
| :prompt        | 選択されていない時に表示される文字 |              |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

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
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### 選択ボックスを生成

    select("post", "person_name", ["佐藤", "鈴木", "高橋"])

#### 先頭に空の要素を追加

    select("post", "person_name", ["佐藤", "鈴木", "高橋"], { include_blank: "選択してください" })

#### リストボックスを生成

    select("post", "person_name", ["佐藤", "鈴木", "高橋"], { multiple: true })

##### 選択ボックスを生成(f.select)

    f.select(:person_name, ["佐藤", "鈴木", "高橋"])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L158)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L845)
