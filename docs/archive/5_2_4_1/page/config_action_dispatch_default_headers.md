---
layout: archive_page
---
### 説明
デフォルトで設定されたHTMLヘッダを持つハッシュ。デフォルトで下記の設定が定義されている

    config.action_dispatch.default_headers = {
      X-Frame-Options: 'SAMEORIGIN',
      X-XSS-Protection: '1; mode=block',
      X-Content-Type-Options: 'nosniff'
    }

### 使い方
    config.action_dispatch.default_headers

### 例
    config.action_dispatch.default_headers = {
      X-Frame-Options: 'DENY',
      X-XSS-Protection: '0',
      X-Content-Type-Options: 'nosniff',
      X-UA-Compatible: 'IE=EmulateIE7'
    }