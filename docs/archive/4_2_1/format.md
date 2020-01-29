---
layout: page
---
### 説明
正規表現パターンに一致しているか

### 使い方
    validates(検証するフィールド名, :format => 検証パラメータ)

### オプション

オプション   | 説明
------- | ---------------------------------------------------------
:on     | 保存されるタイミングを設定
:if     | 検証する条件を指定
:unless | 検証しない条件を指定
:strict | 保護された属性を更新するときにActiveModel::MassAssignmentSecurity::Error

### 例
    validates :email, format: { with: /\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\Z/i, on: :create }

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/validates.rb#L105)