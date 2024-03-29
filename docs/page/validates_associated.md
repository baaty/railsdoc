---
layout: page
---

### 説明

関連しているモデルもバリデーション  
関連付けが無い場合はバリデーションは成功

### 使い方

    validates_associated(バリデーション対象..)

### オプション

| オプション   | 説明                             | デフォルト値 |
| ------------ | -------------------------------- | ------------ |
| :message     | 失敗したときに表示するメッセージ |              |
| :on          | 実行するタイミング               | 保存時       |
| :allow_nil   | nilをスキップ                    | false        |
| :allow_blank | nilや空文字をスキップ            | false        |
| :if          | バリデーションする条件を指定     |              |
| :unless      | バリデーションしない条件を指定   |              |
| :strict      | 失敗した場合に例外を発生         |              |

### 例

    class Book < ActiveRecord::Base
      has_many :pages
      belongs_to :library
      validates_associated :pages, :library
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/validations/associated.rb#L46)
