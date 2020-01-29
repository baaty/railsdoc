---
layout: page
---
### 説明
アクセスのたびにアプリケーションクラスのリロードするかの設定を行います

### 使い方
#### リロードしない
    cache_classes = true

#### リロードする
    cache_classes = false

### デフォルトの設定

環境          | 設定
----------- | ---------------------
development | cache_classes = false
test        | cache_classes = false
production  | cache_classes = true