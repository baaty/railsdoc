---
layout: page
---
### 説明
例外処理をまとめる

### 使い方
    rescue_from(例外 , with: メソッド)

### 例
#### 例外処理をまとめる
    rescue_from User::NotAuthorized, with: :deny_access

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/rescuable.rb#L51)