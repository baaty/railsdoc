---
layout: page
---
### 説明
正規表現パターンに一致しているか検証

### 使い方
    validates_format_of(検証するフィールド名 [, ...])

### オプション

オプション     | 説明                                                               | 初期値
------------ | ----------------------------------------------------------------- | ----------------
:message     | 検証が失敗したときに表示するメッセージ                                   | must be accepted
:allow_nil   | trueならば、nilの検証はスキップ                                        | false
:allow_blank | trueならば、空の検証はスキップ                                          | false
:with        | 正規表現パターン                                                      |
:without     | 正規表現パターン                                                      |
:multiline   | 行の先頭または、末尾                                                   |
:on          | 保存されるタイミングを設定                                              |
:if          | 検証する条件を指定                                                     |
:unless      | 検証しない条件を指定                                                   |
:strict      | 保護された属性を更新するときにActiveModel::MassAssignmentSecurity::Error |

### 例
    class Person < ActiveRecord::Base
      validates_format_of :email, with: /\A([^@\s]+)@((?:[-a-z0-9]+\.)+[a-z]{2,})\z/, on: :create
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/c551178f1b210c6becdf9612814e1c33fbcca2a5/activemodel/lib/active_model/validations/format.rb#L108)