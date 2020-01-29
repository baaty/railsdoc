---
layout: page
---
### 説明
値が一意であるか

### 使い方
    validates(検証するフィールド名, :uniqueness => 検証パラメータ)

### オプション

オプション           | 説明                    | 初期値
--------------- | --------------------- | ----
:scope          | 一意性制約を決めるために使用する他のカラム |
:case_sensitive | 大文字と小文字を区別するか         | true

### 例
    validates :username, uniqueness: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/validates.rb#L105)