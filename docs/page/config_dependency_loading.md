---
layout: page
---
### 説明
「false」を設定すると、設定のオートロードを無効
config.cache_classesが「true」のときにのみ有効

### 使い方
    config.dependency_loading

### デフォルトの設定

環境          | 設定
----------- | -----
development | false
test        | false
production  | true

### 例
    config.dependency_loading = true