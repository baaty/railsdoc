---
layout: page
---

### 説明

データベースのユニーク制約を使って作成、できなければ初めの1件を取得  
find_or_create_byでは作成されるまでに別プロセスによって作成されている可能性があったので、その問題を解決した処理  
create_or_find_by!はエラーの時に例外が発生

### 使い方

    create_or_find_by(属性, ブロック引数)

    # 失敗したら例外発生
    f.create_or_find_by(属性, ブロック引数)

### 例

#### データベースのユニーク制約を使って作成、できなければ初めの1件を取得

    User.create_or_find_by(first_name: 'Penélope')

#### 失敗したら例外発生

    User.create_or_find_by!(first_name: 'Penélope')

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation.rb#L209)
