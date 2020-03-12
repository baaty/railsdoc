---
layout: archive_page
---
### 説明
条件を指定して最初の1件を取得  
存在しない場合はnil

### 使い方
    モデル.find_by(条件)

#### 取得するレコードが存在しない場合に例外が発生
    モデル.find_by!(条件)

### 例
#### category_idが1の最初の値を取得
    Page.find_by category_id: 1
    # <Page id: 1, category_id: 1>
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/finder_methods.rb#L80)