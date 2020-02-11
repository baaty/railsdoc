---
layout: page
---
### 説明
関連しているモデルも検証  
関連付けが無い場合は検証は成功

### 使い方
    validates_associated(検証対象 [, ...])

### オプション

オプション        | 説明                      | デフォルト値
-------------|-------------------------|-------
:message     | 検証が失敗したときに表示するメッセージ |
:on          | 検証を実行するタイミング         | 保存時
:allow_nil   | nilの検証をスキップ     | false
:allow_blank | nilや空文字の検証をスキップ      | false
:if          | 検証する条件を指定           |
:unless      | 検証しない条件を指定          |
:strict      | 検証に失敗した場合に例外を発生 |

### 例
#### 関連しているモデルも検証
    class Book < ActiveRecord::Base
      has_many :pages
      belongs_to :library
      validates_associated :pages, :library
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2bb0abbec0e4abe843131f188129a1189b1bf714/activerecord/lib/active_record/validations/associated.rb#L46)