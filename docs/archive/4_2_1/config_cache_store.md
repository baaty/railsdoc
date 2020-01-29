---
layout: page
---
### 説明
キャッシュストアを設定する

### 使い方
    config.cache_store = キャッシュの種類

### キャッシュの種類

キャッシュの種類         | 説明
---------------- | --
:memory_store    |
:file_store      |
:mem_cache_store |
:null_store      |

### 例
#### memcachedに保存
    config.cache_store = :mem_cache_store