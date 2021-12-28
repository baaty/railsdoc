---
layout: page
---

### 説明

ストリームにブロードキャストされたメッセージの数を確認

### 使い方

    assert_broadcasts(ストリーム, メッセージ数, ブロック引数)

### 例

#### ブロードキャストされたメッセージの数を確認

    assert_broadcasts 'messages', 0
    ActionCable.server.broadcast 'messages', { text: 'hello' }
    assert_broadcasts 'messages', 1
    ActionCable.server.broadcast 'messages', { text: 'world' }
    assert_broadcasts 'messages', 2

#### ブロック指定

    assert_broadcasts('messages', 1) do
        ActionCable.server.broadcast 'messages', { text: 'hello' }
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actioncable/lib/action_cable/test_helper.rb#L45)
