---
layout: archive_page
---
### 説明
例外処理をまとめる

### 使い方
    rescue_from(例外 , with: メソッド)

### 例
#### 例外処理をまとめる
    rescue_from User::NotAuthorized, with: :deny_access

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activesupport/lib/active_support/rescuable.rb#L51)