---
layout: page
---

### 説明

指定されたブロックで警告が表示されるか

### 使い方

    ActiveSupport::Deprecation.silence

### 例

    ActiveSupport::Deprecation.silence { extend ActiveSupport::Memoizable }
