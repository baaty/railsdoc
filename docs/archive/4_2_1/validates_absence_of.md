---
layout: page
---
### 説明
空白であることを検証

### 使い方
    validates_absence_of(検証するフィールド名 [, ...])

### オプション

オプション    | 説明                  | 初期値
-------- | ------------------- | ----------------
:message | 検証が失敗したときに表示するメッセージ | must be accepted

### 例
    class Person < ActiveRecord::Base
      validates_acceptance_of :terms_of_service
      validates_acceptance_of :eula, message: 'must be abided'
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/absence.rb#L26)