---
layout: page
---
### 説明
取得するカラムを指定

### 使い方
    モデル.select(取得するカラム)

    モデル.select(ブロック)

### 例
#### usersテーブルのnameカラムのみ取得
    User.select("name, sex")
    # SELECT name, sex FROM users

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/71c7fd101324046995d8f7e51e78475c0e37ec1a/actionview/lib/action_view/helpers/form_options_helper.rb#L776)