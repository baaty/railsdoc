---
layout: page
---

### 説明

リンクのみ取り除く

### 使い方

    strip_links(html)

### 例

#### リンクのみ取り除く

    strip_links('%3Ca+href%3D%22http%3A%2F%2Fwww.rubyonrails.org%22%3ERuby+on+Rails%3C%2Fa')
    #=> Ruby on Rails

#### リンクのみ取り除く

    strip_links('Please e-mail me at %3Ca+href%3D%22mailto%3Ame%40email.com%22%3Eme%40email.com%3C%2Fa%3E.')
    #=> Please e-mail me at me@email.com.

#### class属性などがある場合

    strip_links('Blog: %3Ca+href%3D%22http%3A%2F%2Fwww.myblog.com%2F%22+class%3D%22nav%22+target%3D%22_blank%22%3EVisit%3C%2Fa%3E.')
    #=> Blog: Visit.

#### エスケープされる文字あり

    strip_links('%3Ca+href%3D%22https%3A%2F%2Fexample.org%22%3Emalformed+%26+link%3C%2Fa%3E')
    #=> malformed &amp; link

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/sanitize_helper.rb#L120)
