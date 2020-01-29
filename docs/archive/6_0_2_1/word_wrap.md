---
layout: page
---
### 説明
指定された長さ以降の空白に改行を入れて出力

### 使い方
    word_wrap(text, [line_width=80, break_sequence="\n"])
    truncate(文字列 [, オプション])

### 例
    word_wrap('Once upon a time')
    # Once upon a time

    word_wrap('Once upon a time, in a kingdom called Far Far Away, a king fell ill, and finding a successor to the throne turned out to be more trouble than anyone could have imagined...')
    # Once upon a time, in a kingdom called Far Far Away, a king fell ill, and finding\na successor to the throne turned out to be more trouble than anyone could have\nimagined...

    word_wrap('Once upon a time', line_width: 8)
    # Once\nupon a\ntime

    word_wrap('Once upon a time', line_width: 1)
    # Once\nupon\na\ntime

    word_wrap('Once upon a time', line_width: 1, break_sequence: "\r\n")
    # Once\r\nupon\r\na\r\ntime

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionview/lib/action_view/helpers/text_helper.rb#L260)