---
layout: page
---
### 説明
データベースのカラムをバージョンダウン
ロールバックできない処理の際に主に使用

### 使い方
    def down
    end

### 例
#### 基本的な使い方
    def down
      drop_table :pages
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/migration.rb#L794)