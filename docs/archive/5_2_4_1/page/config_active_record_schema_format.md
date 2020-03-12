---
layout: archive_page
---
### 説明
データベーススキーマの出力形式を変更  
デフォルトは、「:ruby」

### 使い方
    config.active_record.schema_format = 形式

### 形式

形式    | 説明
----- | ------
:ruby | Ruby形式
:sql  | SQL形式

### 例
    config.active_record.schema_format = :sql