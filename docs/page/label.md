---
layout: page
---

### 説明

labelタグを生成

### 使い方

    label(オブジェクト名, メソッド名, ラベル配下のコンテンツ=nil, オプション=nil, ブロック引数)

    # f.object
    f.label(メソッド名, ラベル配下のコンテンツ=nil, オプション=nil, ブロック引数)

### オプション

| オプション | 説明                                 |
| ---------- | ------------------------------------ |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### 例

#### labelタグを生成

    label(:post, :cost)
    #=> <label for="post_cost">Total cost</label>

#### ラベル名を指定

    label(:post, :title, "A short title")
    #=> <label for="post_title">A short title</label>

#### class属性を付与

    label(:post, :title, "A short title", class: "title_label")
    #=> <label for="post_title" class="title_label">A short title</label>

#### ブロック指定

    label(:post, :terms) do
      raw('Accept <a href="/terms">Terms</a>.')
    end
    #=> <label for="post_terms">Accept <a href="/terms">Terms</a>.</label>

##### ラベル配下のコンテンツなし(f.label)

    f.label :name
    #=> <label for="page_name">Name</label>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1141)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L2364)
