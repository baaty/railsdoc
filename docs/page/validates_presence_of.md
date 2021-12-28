---
layout: page
---

### 説明

値が空でないかをバリデーション

### 使い方

    validates_presence_of(バリデーション対象..)

### オプション

| オプション   | 説明                             |        |
| ------------ | -------------------------------- | ------ |
| :message     | 失敗したときに表示するメッセージ |        |
| :on          | 実行するタイミング               | 保存時 |
| :allow_nil   | nilをスキップ                    | false  |
| :allow_blank | nilや空文字をスキップ            | false  |
| :if          | バリデーションする条件を指定     |        |
| :unless      | バリデーションしない条件を指定   |        |
| :strict      | 失敗した場合に例外を発生         |        |

### 例

    validates_presence_of :first_name

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/presence.rb#L34)
