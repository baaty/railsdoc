---
layout: archive_page
---
### 説明
ブロックに対してのバリデーション

### 使い方
    validates_each(キー名, [,  オプション])

### オプション

オプション        | 説明
-------------|-----
:on          | 実行するタイミング
:allow_nil   | nilをスキップ
:allow_blank | nilや空文字をスキップ
:if          | バリデーションする条件
:unless      | バリデーションしない条件

### 例
    validates_each :first_name, :last_name, allow_blank: true do |record, attr, value|
      record.errors.add attr, 'starts with z.' if value.to_s[0] == ?z
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations.rb#L87)