---
layout: page
---

### 説明

モデルからチェックボックスを自動生成

### 使い方

    collection_check_boxes(要素名, メソッド名, コレクション名, オプション={}, checked_value={}, ブロック引数)

    # f.object
    f.collection_check_boxes(メソッド名, コレクション名, オプション={}, checked_value={}, ブロック引数)

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :checked   | チェックボックスのチェックの有無     |
| :size      | フォームの幅                         |
| :maxlength | 入力フィールドに入力可能な最大文字数 |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
| :disabled  | 無効化                               |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### 例

#### モデルからチェックボックスを自動生成

    collection_check_boxes(:post, :author_ids, Author.all, :id, :name_with_initial)

#### ブロックで指定

    collection_check_boxes(:post, :author_ids, Author.all, :id, :name_with_initial) do |b|
      b.label { b.check_box }
    end

#### モデルからチェックボックスを自動生成(f.collection_check_boxes)

    form_for @post do |f|
      f.collection_check_boxes :author_ids, Author.all, :id, :name_with_initial
      f.submit
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L779)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L905)
