---
layout: page
---

### 説明

チェックボックスにチェックが入っているかバリデーション

### 使い方

    validates_acceptance_of(フィールド名..)

### オプション

| オプション   | 説明                             | 初期値           |
| ------------ | -------------------------------- | ---------------- |
| :message     | 失敗したときに表示するメッセージ | must be accepted |
| :accept      | 同意済みとみなす値を設定         | 1                |
| :on          | 実行するタイミング               | 保存時           |
| :allow_nil   | nilをスキップ                    | false            |
| :allow_blank | nilや空文字をスキップ            | false            |
| :if          | バリデーションする条件を指定     |                  |
| :unless      | バリデーションしない条件を指定   |                  |
| :strict      | 失敗した場合に例外を発生         |                  |

### 例

    class Person < ActiveRecord::Base
      validates_acceptance_of :terms_of_service
      validates_acceptance_of :eula, message: 'must be abided'
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/acceptance.rb#L50)
