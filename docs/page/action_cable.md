---
layout: page
---

### アクションケーブル(Action Cable)とは

WebSocket通信を実現するためのフレームワーク

### 例

    class ChatChannel < ApplicationCable::Channel
        def subscribed
            @room = Chat::Room[params[:room_number]]
        end
        def speak(data)
            @room.speak data, user: current_user
        end
    end