---
layout: page
---
### 説明
特定の条件に一致するレコードをまとめて削除

### 使い方
    モデル.destroy_all([検索条件])

### 例
#### 条件を指定して削除
    Person.destroy_all("last_login < '2004-04-04'")

    Person.destroy_all(status: "inactive")

    Person.where(age: 0..18).destroy_all

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/39c1d2e1840674f2a58dc1ba610fd64a37e950fd/activerecord/lib/active_record/associations/collection_proxy.rb#L469)