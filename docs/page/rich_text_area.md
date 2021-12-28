---
layout: page
---

### 説明

リッチテキストコンテンツエリア

### 使い方

    rich_text_area(要素名, メソッド名, オプション={})

    # f.object
    f.rich_text_area(メソッド名, オプション={})

### オプション

| オプション | 説明                                | デフォルト値 |
| ---------- | ----------------------------------- | ------------ |
| :class     | デフォルトのスタイルが適用          | trix-content |
| :value     | HTMLのinputタグにデフォルト値を追加 |              |

### 例

    form_with(model: @message) do |form|
        form.rich_text_area :content
    end
    #=> <input type="hidden" name="message[content]" id="message_content_trix_input_message_1"><trix-editor id="content" input="message_content_trix_input_message_1" class="trix-content" ...></trix-editor>

    form_with(model: @message) do |form|
        form.rich_text_area :content, value: "<h1>Default message</h1>"
    end
    #=> <input type="hidden" name="message[content]" id="message_content_trix_input_message_1" value="<h1>Default message</h1>"><trix-editor id="content" input="message_content_trix_input_message_1" class="trix-content" ...></trix-editor>

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actiontext/app/helpers/action_text/tag_helper.rb#L87)
