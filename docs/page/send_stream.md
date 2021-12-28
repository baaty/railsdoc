---
layout: page
---

### 説明

ストリームをブラウザに送信

### 使い方

    send_stream(filename: ファイル名, disposition: インラインで表示するかダウンロードするか='attachment', type: HTTPコンテンツタイプ=nil)

### 例

    send_stream(filename: "subscribers.csv") do |stream|
        stream.write "email_address,updated_at\n"
        @subscribers.find_each do |subscriber|
            stream.write "#{subscriber.email_address},#{subscriber.updated_at}\n"
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/live.rb#L320)
