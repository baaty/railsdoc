---
layout: page
---

### 説明

与えられたフィールドのHTMLのid属性値を生成

### 使い方

    field_id(オブジェクト名, メソッド名, 接尾語, index: インデックス)

    # f.object
    f.field_id(フィールド, 接尾語, index: インデックス)

### 例

#### 与えられたフィールドのHTMLのid属性値を生成

    text_field_tag :post, :title, aria: { describedby: field_id(:post, :title, :error) }

#### 与えられたフィールドのHTMLのid属性値を生成(f.object)

    form_for @post do |f|
        f.label :title
        f.text_field :title, aria: { describedby: f.field_id(:title, :error) }
        tag.span("is blank", id: f.field_id(:title, :error)
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_helper.rb#L1752)
