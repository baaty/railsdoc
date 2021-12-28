---
layout: page
---

### 説明

正規表現パターンに一致しているかバリデーション

### 使い方

    validates_format_of(フィールド名..)

### オプション

| オプション   | 説明                             | 初期値           |
| ------------ | -------------------------------- | ---------------- |
| :message     | 失敗したときに表示するメッセージ | must be accepted |
| :with        | 正規表現パターン                 |                  |
| :without     | 正規表現パターン                 |                  |
| :multiline   | 行の先頭または、末尾             |                  |
| :on          | 実行するタイミング               | 保存時           |
| :allow_nil   | nilをスキップ                    | false            |
| :allow_blank | nilや空文字をスキップ            | false            |
| :if          | バリデーションする条件を指定     |                  |
| :unless      | バリデーションしない条件を指定   |                  |
| :strict      | 失敗した場合に例外を発生         |                  |

### 例

    validates_format_of :email, with: /\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\z/, on: :create

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/format.rb#L108)
