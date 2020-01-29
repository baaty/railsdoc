---
layout: page
---
### 説明
本体を持たない任意のタグを生成

### 使い方
    tag(タグ名 [, タグの属性])

### 例
#### brタグを生成
    tag("br")

#### inputタグを生成
    tag("input", { :type => 'text', :disabled => true })

#### imgタグを生成
    tag("img", { :src => "open & shut.png" })

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/861b70e92f4a1fc0e465ffcf2ee62680519c8f6f/actionview/lib/action_view/helpers/tag_helper.rb#L74)