---
layout: page
---
### 説明
データベースの処理の際に使うタイムゾーンを指定
「:utc」を設定すると、データベースに保存したりする時刻がUTC
デフォルトでは、「:local」

### 使い方
    config.active_record.default_timezone = ( :local | :utc )

### 例
    config.active_record.default_timezone = :utc