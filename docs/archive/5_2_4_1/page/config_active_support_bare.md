---
layout: archive_page
---
### 説明
Railsの起動時に、全アクティブサポートのロードを有効、または無効  
デフォルトは、「nil」で、その際は全アクティブサポートが呼びこまれる

### 使い方
    config.active_support.bare = Bool値

### 例
    config.active_support.bare = true