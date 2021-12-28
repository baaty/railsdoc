---
layout: page
---

### 説明

指定したメッセージがストリームに送信されているか確認

### 使い方

    assert_broadcast_on(ストリーム, メッセージ, ブロック引数)

### 例

#### ストリームに送信されているか確認

    ActionCable.server.broadcast 'messages', text: 'hello'
    assert_broadcast_on('messages', text: 'hello')

#### ブロック指定

    assert_broadcast_on('messages', text: 'hello') do
      ActionCable.server.broadcast 'messages', text: 'hello'
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actioncable/lib/action_cable/test_helper.rb#L97)
