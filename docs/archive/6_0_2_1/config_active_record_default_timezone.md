---
layout: page
---
### 説明
データベースの処理の際に使うタイムゾーンを指定する。「:utc」を設定すると、データベースに保存したりする時刻がUTCとなる。デフォルトでは、「:local」が設定されている

### 使い方
    config.active_record.default_timezone = ( :local | :utc )

### 例
    config.active_record.default_timezone = :utc