---
layout: archive_page
---
### 説明
汎用的なカラム処理

### 使い方
    モデル.calculate(処理方法, カラム名)

### 処理方法

処理方法 | 説明
---------|-----
:count   | カウント
:sum     | 合計値
:average | 平均値
:minimum | 最小値
:maximum | 最大値

### 例
#### pagesテーブルのカラム数
    Page.calculate(:count, :all)
    # SELECT COUNT(*) FROM "pages"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/calculations.rb#L131)