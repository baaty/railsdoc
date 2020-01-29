---
layout: page
---
### 説明
2つのフィールドが等しいか検証

### 使い方
    validates_confirmation_of(検証するフィールド名 [, ...])

### オプション

オプション | 説明                                                                | 初期値
-------- | ------------------------------------------------------------------- | ----------------
:message | 検証が失敗したときに表示するメッセージ                                    | must be accepted
:on      | 保存されるタイミングを設定                                              |
:if      | 検証する条件を指定                                                     |
:unless  | 検証しない条件を指定                                                   |
:strict  | 保護された属性を更新するときにActiveModel::MassAssignmentSecurity::Error |

### 例
    Model:
      class Person < ActiveRecord::Base
        validates_confirmation_of :user_name, :password
        validates_confirmation_of :email_address,
                                  message: 'should match confirmation'
      end

    View:
      <%= password_field "person", "password" %>
      <%= password_field "person", "password_confirmation" %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0df1f914104073b70f8d8976d0d5adc3b2a1e44e/activemodel/lib/active_model/validations/exclusion.rb#L41)