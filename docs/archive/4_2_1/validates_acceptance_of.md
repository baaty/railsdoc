---
layout: page
---
### 説明
チェックボックスにチェックが入っているか検証

### 使い方
    validates_acceptance_of(検証するフィールド名 [, ...])

### オプション

オプション      | 説明                                                        | 初期値
---------- | --------------------------------------------------------- | ----------------
:message   | 検証が失敗したときに表示するメッセージ                                       | must be accepted
:allow_nil | trueならば、nilの検証はスキップ                                       | false
:accept    | フォームで受付可能なMIMEタイプ                                         | 1
:on        | 保存されるタイミングを設定                                             |
:if        | 検証する条件を指定                                                 |
:unless    | 検証しない条件を指定                                                |
:strict    | 保護された属性を更新するときにActiveModel::MassAssignmentSecurity::Error |

### 例
    class Person < ActiveRecord::Base
      validates_acceptance_of :terms_of_service
      validates_acceptance_of :eula, message: 'must be abided'
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/acceptance.rb#L50)