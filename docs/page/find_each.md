---
layout: page
---
### 説明
分割してレコードを取得して処理
デフォルトでは1000件ずつ処理

### 使い方
    モデル.find_each([オプション]) do |i|
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

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/batches.rb#L67)