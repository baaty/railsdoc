---
layout: page
---

### 説明

キャッシュストアで使用するロガーの設定

### 使い方

    ActiveSupport::Cache::Store.logger

### 例

    ActiveSupport::Cache::Store.logger = Logger.new(STDOUT)
