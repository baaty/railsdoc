---
layout: page
---
### 説明
ファイルの変更検知の設定  
依存関係のあるファイルに変更があった場合に、クラスを再読み込みするようになる  
config.cache_classesが「true」の場合は無視

### 使い方
    config.reload_classes_only_on_change

### 例
    config.reload_classes_only_on_change = false