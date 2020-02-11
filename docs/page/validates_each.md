---
layout: page
---
### 説明
ブロックに対しての検証

### 使い方
    validates_each(キー名, [,  オプション]

### オプション

オプション        | 説明
-------------|-----
:on          | 検証を実行するタイミング
:allow_nil   | nilの検証をスキップ
:allow_blank | nilや空文字の検証をスキップ
:if          | 検証を行う条件
:unless      | 検証を行わない条件

### 例
    validates_each :first_name, :last_name, allow_blank: true do |record, attr, value|
      record.errors.add attr, 'starts with z.' if value.to_s[0] == ?z
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations.rb#L85)