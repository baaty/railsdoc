---
layout: page
---

### 説明

条件を指定して最初の1件を取得  
存在しない場合はnil

### 使い方

    モデル.find_by(条件..)

    # 失敗したら例外発生
    モデル.find_by!(条件..)

### 例

#### category_idが1の最初の値を取得

    Page.find_by category_id: 1
    # SQL: SELECT "pages".* FROM "pages" WHERE "pages"."category_id" = 1 LIMIT 1

#### category_idの1が存在しない場合

    Page.find_by category_id: 1
    # nil

#### 複数条件を指定

    Page.find_by category_id: 1, user_if: 1

#### whereで書き換える

    # Page.find_by category_id: 1
    Page.where(category_id: 1).take

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/finder_methods.rb#L80)
