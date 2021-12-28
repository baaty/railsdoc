---
layout: page
---

### 説明

サイレンサー(バックトレースを完全に取り除く)のブロックを有効にするか  
「false」を設定する場合、silence loggingのブロックを無効  
デフォルトは、「true」

### 使い方

    ActiveSupport::Logger.silencer

### 例

    ActiveSupport::Logger.silencer = false
