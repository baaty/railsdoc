---
layout: page
---

### 説明

キャッシュストアを設定

### 使い方

    config.cache_store = キャッシュの種類

### キャッシュの種類

| キャッシュの種類         | 説明        |
| ---------------- | --------- |
| :memory_store    | プロセス内のメモリ |
| :file_store      | ファイルシステム  |
| :mem_cache_store | memcached |
| :null_store      | キャッスをしない  |

### 例

#### memcachedに保存

    config.cache_store = :mem_cache_store
