---
layout: page
---
### 説明
テーブルの主キーのカラムを指定する。デフォルトは、「id」

### 使い方
    config.active_record.primary_key_prefix_type = 主キー名

### 例
    config.active_record.primary_key_prefix_type = :table_name_with_underscore