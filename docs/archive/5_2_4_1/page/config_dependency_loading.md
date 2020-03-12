---
layout: archive_page
---
### 説明
「false」を設定すると、設定のオートロードを無効  
config.cache_classesが「true」のときにのみ有効

### 使い方
    config.enable_dependency_loading = Bool値

### デフォルトの設定

環境          | 設定
----------- | -----
development | false
test        | false
production  | true

### 例
    config.enable_dependency_loading = true