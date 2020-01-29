---
layout: page
---
### 説明
任意のタグを生成

### 使い方
    tag(タグ名 [, オプション, HTML4互換, エスケープするか])

### 例
    tag.h1 'All titles fit to print'
    # <h1>All titles fit to print</h1>

    tag.div tag.p('Hello world!')
    # <div><p>Hello world!</p></div>

    tag.section class: %w( kitties puppies )
    # <section class="kitties puppies"></section>

    tag.section id: dom_id(@post)
    # <section id="<generated dom id>"></section>

    tag.input type: 'text', disabled: true
    # <input type="text" disabled="disabled">

    tag.article data: { user_id: 123 }
    # <article data-user-id="123"></article>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/tag_helper.rb#L236)