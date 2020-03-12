---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_controller/metal/mime_responds.rb#L193)