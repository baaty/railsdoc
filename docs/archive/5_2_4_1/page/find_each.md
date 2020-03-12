---
layout: archive_page
---
### 説明
分割してレコードを取得して1件ずつ処理  
デフォルトでは1000件ずつ処理
大きなデータをもつモデルなどを処理する時に使う

### 使い方
    モデル.find_each([オプション]) do |i|
      処理内容
    end

### オプション

オプション            | 説明         | デフォルト値
-----------------|------------|-------
:batch_size      | 同時処理数   | 1000
:start           | 処理開始位置 |
:finish          | 終了するときのキー  |
:error_on_ignore | 例外を発生させる |

### 例
#### category_idが1の値をeachする
    Person.find_each do |person|
      person.do_awesome_stuff
    end

#### 同時処理数を10
    Post.find_each(:batch_size => 10) do |post|
    end

#### 開始位置を指定
    Person.find_each(start: 2000, batch_size: 2000) do |person|
    end

### 補足
* find_in_batchesとの違いは1件ずつ処理すること

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation/batches.rb#L67)