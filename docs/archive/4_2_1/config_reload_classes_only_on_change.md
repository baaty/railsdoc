---
layout: page
---
### 説明
ファイルの変更検知の設定をする
依存関係のあるファイルに変更があった場合に、クラスを再読み込みするようになる
config.cache_classesが「true」の場合は、無視される

### 使い方
    config.reload_classes_only_on_change = ( true | false )

### 例
    config.reload_classes_only_on_change = false