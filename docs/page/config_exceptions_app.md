---
layout: page
---

### 説明

例外発生時にShowException middlewareから呼ばれる例外処理アプリケーションを設定  
デフォルトは、「ActionDispatch::PublicExceptions.new(Rails.public_path)」

### 使い方

    config.exceptions_app

### 例

    config.exceptions_app = self.routes
