---
layout: page
---
### 説明
検索件数を取得

### 使い方
    モデル.count(カラム名 [, オプション})

### 例
#### テーブルの行数を計算
    User.count
    # SELECT count(*) AS count_all FROM users

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/6c8cf21584ced73ade45529d11463c74b5a0c58f/activemodel/lib/active_model/errors.rb#L208)