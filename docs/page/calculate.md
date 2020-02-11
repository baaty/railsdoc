---
layout: page
---
### 説明
カラムを処理

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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/calculations.rb#L127)