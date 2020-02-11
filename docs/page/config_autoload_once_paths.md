---
layout: page
---
### 説明
起動時のみロードするコンテンツを配列に含める

デフォルト値は空の配列

### 使い方
    config.autoload_once_paths += %W(#{config.root}/ディレクトリ名)]

### 例
    config.autoload_once_paths += %W(#{config.root}/lib)