---
layout: page
---

### 説明

ETagを生成

### 使い方

    etag(情報)

### 例

    class InvoicesController < ApplicationController
        etag { current_user&.id }
        def show
            # Etag will differ even for the same invoice when it's viewed by a different current_user
            @invoice = Invoice.find(params[:id])
            fresh_when etag: @invoice
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/conditional_get.rb#L31)
