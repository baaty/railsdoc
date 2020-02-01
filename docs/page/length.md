---
layout: page
---
### 説明
汎用的な検証

### 使い方
    validates(検証するフィールド名, 検証の種類 [, オプション])

### 検証の種類

種類          | 説明
--------------|-------------------
:acceptance   | チェックボックスがオンになっているか
:confirmation | テキストフィールドが完全に一致するか
:exclusion    | 含まれていないことを検証
:format       | 正規表現と一致するか
:inclusion    | 含まれていることを検証
:length       | 長さを検証
:numericality | 数値のみかどうか
:presence     | 空で無いこと
:absence      | 空であること
:uniqueness   | 重複していないこと

### オプション

オプション        | 説明
-------------|----------------
:on          | 実行のタイミング
:if          | if文
:unless      | ulness文
:allow_nil   | nilの場合にスキップ
:allow_blank | nilや空文字の場合にスキップ
:strict      | 例外が発生するか
:message     | 失敗時のメッセージ

### lengthのオプション

オプション         | 説明
--------------|--------------
:minimum      | この値より小さな値かどうか
:maximum:     | この値より大きな値がどうか
:inまたは:within | 区間以内かどうか
:is           | 値と等かどうか

### numericalityのオプション

オプション                     | 説明
--------------------------|---------------------
:greater_than             | 指定した値よりも大きいか
:greater_than_or_equal_to | 指定した値と等しいか、それよりも大きいか
:equal_to                 | 指定した値と等しいか
:less_than                | 指定した値よりも小さいか
:less_than_or_equal_to    | 指定した値と等しいか、それよりも小さいか
:other_than               | 指定した値以外の値かどうか
:odd                      | 奇数か
:even                     | 偶数か

### 例
#### acceptance
##### チェックボックスがオンになっているか
    validates :form, acceptance: true

##### チェックボックスがオフになっているか
    validates :form, acceptance: false

#### confirmation
##### テキストフィールドが完全に一致するか
    validates :email, confirmation: true

##### テキストフィールドが完全に一致しないか
    validates :email, confirmation: false

#### exclusion
##### 含まれていないか
    validates :subdomain, exclusion: {in: %w(www us ca jp)}

#### format
##### 正規表現と一致するか
    validates :legacy_code, format: {with: /\A[a-zA-Z]+\z/}

#### inclusion
##### 含まれていることを検証
    validates :size, inclusion: {in: %w(small medium large)}

#### length
##### 長さを検証
    validates :name, length: {minimum: 2}

#### numericality
##### 数値のみかどうか
    validates :points, numericality: true

#### presence
##### 空で無いこと
    validates :name, :login, :email, presence: true

#### absence
##### 空であること
    validates :name, :login, :email, absence: true

#### uniqueness
##### 重複していないこと
    validates :email, uniqueness: true

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/validates.rb#L105)