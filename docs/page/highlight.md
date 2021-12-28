---
layout: page
---

### 説明

ハイライト

### 使い方

    highlight(文字列, ハイライトする文字列, オプション={}, ブロック引数)

### 例

#### ハイライト

    highlight('指定した文字をハイライトすることができる', 'ハイライト')
    # => 指定した文字を<mark>ハイライト</mark>することができる

#### 複数指定

    highlight('指定した文字をハイライトすることができる', /指定した文字|ハイライト/)
    # => <mark>指定した文字</mark>を<mark>ハイライト</mark>することができる

#### ハイライト方法を変更

    highlight('指定した文字をハイライトすることができる', 'ハイライト', highlighter: '<em>\1</em>')
    # => 指定した文字を<em>ハイライト</em>することができる

#### リンクでハイライト

    highlight('指定した文字をハイライトすることができる', 'ハイライト')  do |match|
        link_to(search_path(q: match, match))
    end
    # => 指定した文字を<a href="search?q=ハイライト">ハイライト</a>することができる

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L125)
