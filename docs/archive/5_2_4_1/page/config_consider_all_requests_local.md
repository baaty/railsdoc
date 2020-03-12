---
layout: archive_page
---
### 説明
「true」のとき、すべてのエラーをブラウザに表示をするかの設定

### 使い方
    config.consider_all_requests_local = Bool値

### デフォルトの設定

環境          | 設定
----------- | -----
development | true
test        | true
production  | false

### 例
    config.consider_all_requests_local = true