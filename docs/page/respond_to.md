---
layout: page
---
### 説明
リクエストで指定されたフォーマットに合わせて出力

### 使い方
    respond_to do |format|
      format.Mimeタイプ
    end

### 例
    respond_to do |format|
      format.html
      format.js
      format.xml { render xml: @people }
    end

    redirect_to(person_list_url)

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/mime_responds.rb#L201)