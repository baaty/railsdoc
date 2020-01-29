---
layout: page
---
### 説明
起動時のみロードするコンテンツを配列に含める

### 使い方
    config.autoload_once_path += %W(#{config.root}/ディレクトリ名)]

### 例
    config.autoload_once_path += %W(#{config.root}/lib)