---
layout: archive_page
---
### 説明
アクションの前後に処理を追加  
around_actionより後に処理

### 使い方
    append_around_action(コールバック名 [, オプション])

### オプション

オプション   | 説明
--------|------------
:only   | 実行するアクション
:except | 実行しないアクション
:if     | 実行する条件を指定
:unless | 実行されない条件を指定

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/abstract_controller/callbacks.rb#L184)