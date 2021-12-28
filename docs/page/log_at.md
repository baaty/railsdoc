---
layout: page
---

### 説明

リクエストごとに異なるログレベルを設定

### 使い方

    log_at(ログレベル, オプション引数)

### 例

    # Use the debug log level if a particular cookie is set.
    class ApplicationController < ActionController::Base
        log_at :debug, if: -> { cookies[:debug] }
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/logging.rb#L15)
