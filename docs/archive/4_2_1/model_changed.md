---
layout: page
---
### 説明
属性の変更点を取得

### 使い方
    モデル.changed

### 例
    person.changed # => []
    person.name = 'bob'
    person.changed # => ["name"]