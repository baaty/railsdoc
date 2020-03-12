---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/migration.rb#L780)