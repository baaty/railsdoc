---
layout: page
---
### 説明
ログオブジェクト
ログオブジェクトは、Log4Rインターフェース、またはRubyログオブジェクトクラスとの互換性が必要
「nil」を設定すると無効

### 使い方
    config.active_record.logger = logger

### 例
    config.active_record.logger = Logger.new("log/development_sql.log")