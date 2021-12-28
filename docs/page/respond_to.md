---
layout: page
---

### 説明

リクエストで指定されたフォーマットに合わせて出力

### 使い方

    respond_to(mimes..)

### 例

    respond_to do |format|
      format.html
      format.js
      format.xml { render xml: @people }
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/mime_responds.rb#L201)
