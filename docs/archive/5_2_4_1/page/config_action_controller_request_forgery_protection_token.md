---
layout: archive_page
---
### 説明
RequestForgeryのトークンパラメータを設定  
デフォルトは、「:authenticity_token」

### 使い方
    config.action_controller.request_forgery_protection_token

### 例
    config.action_controller.request_forgery_protection_token = '_xsrf_token_here'