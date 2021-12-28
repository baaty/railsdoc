---
layout: page
---

### 説明

キャッシュストアの設定  
デフォルトは、「Rails file store」

### 使い方

    config.cache_store

### 例

    config.cache_store = [ :file_store, "/tmp/rails-cache/assets/#{Rails.env}/" ]
