---
layout: page
---
### 説明
値が空でないかを検証

### 使い方
    validates_presence_of(検証対象 [, ...])

### オプション

オプション    | 説明
-------- | ---------------------------------------------------------
:message | 検証が失敗したときに表示するメッセージ
:on      | 保存されるタイミングを設定
:if      | 検証する条件を指定
:unless  | 検証しない条件を指定
:strict  | 保護された属性を更新するときにActiveModel::MassAssignmentSecurity::Error

### 例

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/presence.rb#L34)