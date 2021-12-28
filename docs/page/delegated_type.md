---
layout: page
---

### 説明

親と子のテーブルのレコードの継承関係

### 使い方

    delegated_type(ロール, types: 型=nil, オプション引数)

### オプション

| オプション   | 説明                                 | デフォルト値 |
| ------------ | ------------------------------------ | ------------ |
| :foreign_key | 関連オブジェクトで使用する外部キー名 | :foreign_key |
| :primary_key | 関連オブジェクトの主キー             | id           |

### 例

    class Entry < ApplicationRecord
        delegated_type :entryable, types: %w[ Message Comment ], dependent: :destroy
    end

    Entry#entryable_class #=> +Message+ or +Comment+
    Entry#entryable_name  #=> "message" or "comment"
    Entry.messages        #=> Entry.where(entryable_type: "Message")
    Entry#message?        #=> true when entryable_type == "Message"
    Entry#message         #=> returns the message record, when entryable_type == "Message", otherwise nil
    Entry#message_id      #=> returns entryable_id, when entryable_type == "Message", otherwise nil
    Entry.comments        #=> Entry.where(entryable_type: "Comment")
    Entry#comment?        #=> true when entryable_type == "Comment"
    Entry#comment         #=> returns the comment record, when entryable_type == "Comment", otherwise nil
    Entry#comment_id      #=> returns entryable_id, when entryable_type == "Comment", otherwise nil

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/delegated_type.rb#L206)
