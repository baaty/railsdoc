---
layout: archive_page
---
### 説明
分割してレコードを取得して処理  
デフォルトで1000件ずつ処理

### 使い方
    モデル.in_batches([オプション]) do |i|
      処理内容
    end

### オプション

オプション            | 説明         | デフォルト値
-----------------|--------------|-------
:of              | 同時処理数   | 1000
:load            | ロードするか       | false
:start           | 処理開始位置 |
:finish          | 終了するときのキー  |
:error_on_ignore | 例外を発生させる |

### 例
#### 分割してレコードを取得して処理
    Person.where("age > 21").in_batches do |relation|
      relation.delete_all
      sleep(10) # Throttle the delete queries
    end

#### 分割して取得して削除
    Person.in_batches.delete_all

#### 分割して取得して更新
    Person.in_batches.update_all(awesome: true)

### 補足
* find_in_batchesとの違いはActiveRecord::Relationで値を返す

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/batches.rb#L201)