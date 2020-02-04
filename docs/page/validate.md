---
layout: page
---
### 説明
検証を定義

### 使い方
    validate(検証メソッド名 [, ...])

### オプション

オプション        | 説明                      | デフォルト値
-------------|-------------------------|-------
:on          | 保存されるタイミングを設定         |
:allow_nil   | trueならば、nilの検証はスキップ     | false
:allow_blank | trueならば、空の検証はスキップ      | false
:if          | 検証する条件を指定           |
:unless      | 検証しない条件を指定          |
:strict      | 検証に失敗した場合に例外を発生 |

### 例
#### 検証を定義
    class Comment
      include ActiveModel::Validations

      validate :must_be_friends

      def must_be_friends
        errors.add(:base, 'Must be friends to leave a comment') unless commenter.friend_of?(commentee)
      end
    end

#### ブロック
    class Comment
      include ActiveModel::Validations

      validate do |comment|
        comment.must_be_friends
      end

      def must_be_friends
        errors.add(:base, 'Must be friends to leave a comment') unless commenter.friend_of?(commentee)
      end
    end

### ソースコード
* [GitHub]()