---
layout: page
---
### 説明
オートロード対象となるパスを追加

この設定の変更は非推奨

### 使い方
    config.autoload_paths += %W(#{config.root}/ディレクトリ名)

### 例
#### /libファイル以下を自動でロード
    config.autoload_paths += %W(#{config.root}/lib)