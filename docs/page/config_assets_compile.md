---
layout: page
---
### 説明
「true」の場合は、public/assetsのなかに必要なファイルを見つからなかった時に、app/assetsなどからファイルを探しコンパイル

### 使い方
    config.assets.compile

### デフォルトの設定

環境          | 設定
----------- | -----
development | false
test        | false
production  | true

### 例
    config.assets.compile = true