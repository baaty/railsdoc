---
layout: page
---

### 説明

アクションの後に処理を実行

### 使い方

    after_action(アクション名, only: 実行するアクション=nil, except: 実行しないアクション=nil, if: 実行する条件を指定=nil, unless: 実行されない条件を指定=nil, ブロック)

### 例

#### アクションの後に処理を実行

    after_action :store_location

#### 実行するアクションを指定

    after_action :render_form, only: [:new :edit]

#### 複数指定

    after_action :user1
    after_action :user2

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/abstract_controller/callbacks.rb#L147)
