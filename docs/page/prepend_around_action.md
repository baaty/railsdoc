---
layout: page
---

### 説明

アクションの前後に処理を追加  
around_actionより前に処理

### 使い方

    prepend_around_action(アクション名, only: 実行するアクション=nil, except: 実行しないアクション=nil, if: 実行する条件を指定=nil, unless: 実行されない条件を指定=nil, ブロック)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/abstract_controller/callbacks.rb#L181)
