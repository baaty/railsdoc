---
layout: page
---

### 説明

SELECT文で使用するヒントを指定

### 使い方

    モデル.optimizer_hints(引数..)

### 例

#### MySQL

    Topic.optimizer_hints("MAX_EXECUTION_TIME(50000)", "NO_INDEX_MERGE(topics)")
    # SELECT /*+ MAX_EXECUTION_TIME(50000) NO_INDEX_MERGE(topics) */ `topics`.* FROM `topics`

#### PostgreSQL

    Topic.optimizer_hints("SeqScan(topics)", "Parallel(topics 8)")
    # SELECT /*+ SeqScan(topics) Parallel(topics 8) */ "topics".* FROM "topics"

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef277571d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L1142)
