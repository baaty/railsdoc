---
layout: archive_page
---
### 説明
分割不可能な複数のレコードの更新を1つの単位にまとめて処理すること

### 特徴
* データベース内の情報の整合性を保つための手段
* 複数のデータベースにまたがる分散トランザクションはサポートしていない
* 使用するにはデータベースがトランザクションをサポートしていることが必要

### 使い方
    ActiveRecord::Base.transaction do
      例外が発生するかもしれない処理
    end
      例外が発生しなかった場合の処理
    resque => e
      例外が発生した場合の処理

    モデル.transaction do
      例外が発生するかもしれない処理
    end
      例外が発生しなかった場合の処理
    resque => e
      例外が発生した場合の処理

* ブロック内のすべての処理が正常に行われた場合に保存
* エラーが発生した場合は、ロードバック

### 例
    def new
      User.transaction do
        a1 = User.new(name: 'tarou')
        a1.save!
        a2 = User.new(name: 'jirou')
        a2.save!
      end
      render text: '更新に成功しました'
      rescue: e
      render text: e.message
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/a953f7f674997517c5b9580335dda3338840aa84/activerecord/lib/active_record/connection_adapters/abstract/database_statements.rb#L204)