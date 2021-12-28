---
layout: page
---

### 説明

指定された長さ以降の空白に改行を入れて出力

### 使い方

    word_wrap(テキスト, line_width: 幅=80, break_sequence: 改行='\\n')

### オプション

| オプション      | 説明                                 |
| --------------- | ------------------------------------ |
| :line_width     | 改行する文字の長さ(デフォルト値: 80) |
| :break_sequence | 改行コード(デフォルト値: \\n)        |

### 例

#### 指定された長さ以降の空白に改行を入れて出力

    word_wrap('Once upon a time')
    # Once upon a time

#### 80文字以上で改行

    word_wrap('Once upon a time, in a kingdom called Far Far Away, a king fell ill, and finding a successor to the throne turned out to be more trouble than anyone could have imagined...')
    # Once upon a time, in a kingdom called Far Far Away, a king fell ill, and finding\na successor to the throne turned out to be more trouble than anyone could have\nimagined...

#### 改行する文字の長さを変更

    word_wrap('Once upon a time', line_width: 8)
    # Once\nupon a\ntime

#### 改行コードを変更

    word_wrap('Once upon a time', line_width: 1, break_sequence: "\r\n")
    # Once\r\nupon\r\na\r\ntime

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/text_helper.rb#L264)
