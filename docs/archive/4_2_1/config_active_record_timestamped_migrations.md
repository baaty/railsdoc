---
layout: page
---
### 説明
マイグレーションファイルの識別子を設定する。falseを設定すると、タイムスタンプの代わりに昇降の整数を使用

### 使い方
    config.active_record.timestamped_migrations = "識別子"

### 例
    config.active_record.timestamped_migrations = false