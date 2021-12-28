---
layout: page
---

### 説明

分割してレコードを取得して処理  
デフォルトで1000件ずつ処理

### 使い方

    モデル.in_batches(of: バッチのサイズ=1000, start: 開始する主キーの値=nil, finish: 終了する主キーの値=nil, load: リレーションをロードするか=false, error_on_ignore: エラーを発生させるか=nil, order: 主キーの順序=:asc)

### オプション

| オプション       | 説明                       | デフォルト値 |
| ---------------- | -------------------------- | ------------ |
| :of              | バッチのサイズ             | 1000         |
| :load            | リレーションをロードするか | false        |
| :start           | 処理開始位置               |              |
| :finish          | 終了するときのキー         |              |
| :error_on_ignore | 例外を発生させる           |              |
| :order           | 主キーの順序を指定         | :asc         |

### 例

#### 分割してレコードを取得して処理

    Person.where("age > 21").in_batches do |relation|
      relation.delete_all
      sleep(10) # 削除クエリの調整
    end

### 補足

- 処理する順序は指定できない
- find_eachとの違いは配列で値を受けとること
- 順番に処理したい場合は、find_eachを使用

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/batches.rb#L204)
