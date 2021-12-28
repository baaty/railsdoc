---
layout: page
---
### 説明
データベースのユニーク制約を使って作成、できなければ初めの1件を取得  
find_or_create_byでは作成されるまでに別プロセスによって作成されている可能性があったので、その問題を解決した処理  
create_or_find_by!はエラーの時に例外が発生

### 使い方
    create_or_find_by(属性)

#### ブロック指定
    create_or_find_by(属性) do
    end

### 例
#### データベースのユニーク制約を使って作成、できなければ初めの1件を取得  
    User.create_or_find_by(first_name: 'Penélope')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L209)