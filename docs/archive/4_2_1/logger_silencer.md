---
layout: page
---
### 説明
サイレンサー(バックトレースを完全に取り除く)のブロックを有効にするか、無効にするか
「false」を設定する場合、silence loggingのブロックを無効にする。デフォルトは、「true」

### 使い方
    ActiveSupport::Logger.silencer = ( true | false )

### 例
    ActiveSupport::Logger.silencer = false