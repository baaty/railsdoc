---
layout: archive_page
---
### 説明
関連しているモデルもバリデーション  
関連付けが無い場合はバリデーションは成功

### 使い方
    validates_associated(バリデーション対象 [, ...])

### オプション

オプション        | 説明                      | デフォルト値
-------------|-------------------------|-------
:message     | 失敗したときに表示するメッセージ |
:on          | 実行するタイミング         | 保存時
:allow_nil   | nilをスキップ     | false
:allow_blank | nilや空文字をスキップ      | false
:if          | バリデーションする条件を指定           |
:unless      | バリデーションしない条件を指定          |
:strict      | 失敗した場合に例外を発生 |

### 例
#### 関連しているモデルもバリデーション
    class Book < ActiveRecord::Base
      has_many :pages
      belongs_to :library
      validates_associated :pages, :library
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/validations/associated.rb#L55)