---
layout: page
---

### 説明

選択ボックスをグループ化

### 使い方

    grouped_collection_select(オブジェクト名, メソッド名, オブジェクトの配列, タグを取得するメソッド, タグのラベル, valueの項目, テキストの項目, オプション={}, HTML属性={} or イベント属性={})

    # f.object
    f.grouped_collection_select(メソッド名, オブジェクトの配列, タグを取得するメソッド, タグのラベル, valueの項目, テキストの項目, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション           | 説明                                     |
| -------------------- | ---------------------------------------- |
| :object              | 選択タグに使用されるクラスのインスタンス |
| :method              | 選択タグに対応する属性                   |
| :collection          | タグを表すオブジェクトの配列             |
| :group_method        | グループ名                               |
| :group_label_method  | グループ属性                             |
| :option_key_method   | collectionと使用される値                 |
| :option_value_method | optionタグのコンテンツとして使用される値 |

### HTML属性

| HTML属性   | 説明                               |
| ---------- | ---------------------------------- |
| :name      | 名称                               |
| :size      | サイズ。ピクセル数で指定           |
| :readonly  | 内容変更を禁止                     |
| :tabindex  | Tabキーによる入力欄の移動順        |
| :accesskey | 移動するショートカットキー         |
| :usemap    | この画像に対応させるイメージマップ |
| :id        | 要素固有の識別子                   |
| :class     | 要素を分類するクラス名             |
| :title     | 要素の補足情報                     |
| :style     | 要素の補足情報                     |
| :dir       | 表記方向                           |
| :lang      | 基本言語                           |

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

#### 選択ボックスをグループ化

    grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name)

#### 空のオプションを先頭に追加

    grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name, include_blank: true)

#### 指定したオプションを先頭に追加

    grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name, :prompt = "選択してください")

#### 選択したオプション

    grouped_collection_select(:page, :name, @categories, :pages, :name, :id, :name)

#### 選択ボックスをグループ化(f.grouped_collection_select)

    f.grouped_collection_select(:name, @categories, :pages, :name, :id, :name)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L257)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L869)
