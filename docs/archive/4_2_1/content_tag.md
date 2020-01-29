---
layout: page
---
### 説明
タグを動的に生成
HTMLとERBが混ざってしまう場合などに使用するとすっきり表現できる

### 使い方
    content_tag(タグの名前)

### 例
    content_tag :p, "Hello world"

    <p>Hello&nbsp;world</p>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/actionview/lib/action_view/helpers/tag_helper.rb#L103)