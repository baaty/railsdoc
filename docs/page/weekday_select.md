---
layout: page
---

### 説明

曜日のセレクトタグとオプションタグを生成

### 使い方

    weekday_select(要素名, メソッド, オプション={}, HTML属性={} or イベント属性={}, ブロック引数)

    # f.object
    .weekday_select(メソッド, オプション={}, HTML属性={} or イベント属性={}, ブロック引数)

### 例

    f.weekday_select :weekday, include_blank: true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L297)
