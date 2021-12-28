---
layout: page
---

### 説明

ブロックに対してのバリデーション

### 使い方

    validates_each(キー名.., ブロック引数)

### オプション

| オプション   | 説明                     |
| ----------- | ------------------------ |
| :on          | 実行するタイミング       |
| :allow_nil   | nilをスキップ            |
| :allow_blank | nilや空文字をスキップ    |
| :if          | バリデーションする条件   |
| :unless      | バリデーションしない条件 |

### 例

    validates_each :first_name, :last_name, allow_blank: true do |record, attr, value|
      record.errors.add attr, 'starts with z.' if value.to_s[0] == ?z
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations.rb#L85)
