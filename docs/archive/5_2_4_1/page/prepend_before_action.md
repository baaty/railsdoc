---
layout: archive_page
---
### 説明
アクションの前に処理を追加  
before_actionより前に処理

### 使い方
    prepend_before_action(コールバック名 [, オプション])

### オプション

オプション   | 説明
--------|------------
:only   | 実行するアクション
:except | 実行しないアクション
:if     | 実行する条件を指定
:unless | 実行されない条件を指定

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/callbacks.rb#L122)