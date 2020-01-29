---
layout: page
---
### 説明
関連しているモデルも検証

### 使い方
    validates_associated(検証対象 [, ...])

### オプション

オプション | 説明
-------- | -------------------
:message | 検証が失敗したときに表示するメッセージ
:on      | 保存されるタイミングを設定
:if      | 検証する条件を指定
:unless  | 検証しない条件を指定

### 例
    class Book < ActiveRecord::Base
      has_many :pages
      belongs_to :library
      validates_associated :pages, :library
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2bb0abbec0e4abe843131f188129a1189b1bf714/activerecord/lib/active_record/validations/associated.rb#L46)