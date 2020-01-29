---
layout: page
---
### 説明
文字列の長さをチェック

### 使い方
    validates(検証するフィールド名, :length => 検証パラメータ)

### オプション

オプション         | 説明
------------- | ----------------------------
:minimun      | 最小の文字列長
:maximun      | 最大の文字列長
:in           | 文字列長の範囲(range型)
:tokenizer    | 文字列の分割方法
:is           | 文字列長
:too_long     | :maximunパラメータに違反した時のエラーメッセージ
:too_short    | :minimunパラメータに違反した時のエラーメッセージ
:wrong_length | :isパラメータに違反した時のエラーメッセージ

### 例
    validates :first_name, length: { maximum: 30 }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/validates.rb#L105)