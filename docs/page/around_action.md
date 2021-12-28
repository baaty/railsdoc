---
layout: page
---

### 説明

アクションの前後に処理を実行

### 使い方

    around_action(アクション名, only: 実行するアクション=nil, except: 実行しないアクション=nil, if: 実行する条件を指定=nil, unless: 実行されない条件を指定=nil, ブロック)

### 例

#### アクションの前後に処理を実行

    around_action :render_form, only: [:new :edit]

#### 複数指定

    around_action :user1
    around_action :user2

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/abstract_controller/callbacks.rb#L174)
