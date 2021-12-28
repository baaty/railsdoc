---
layout: page
---

### 説明

モデルのコレクションを生成  
newの別名

### 使い方

    モデルのコレクション.build(属性={}, ブロック引数)

### 例

#### モデルを生成

    person.pets.build

#### 属性を指定

    person.pets.build(name: 'Fancy-Fancy')

#### ブロックを指定

    person.pets.build([{name: 'Spook'}, {name: 'Choo-Choo'}, {name: 'Brain'}])

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/associations/collection_proxy.rb#L316)
