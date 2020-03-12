---
layout: archive_page
---
### 説明
「ture」の場合、ファイルシステム内のファイルの更新を検知するためのクラス  
ActiveSupport::FileUpdateCheckerに準拠する必要

### 使い方
    config.file_watcher

### 例
    config.file_watcher = ActiveSupport::EventedFileUpdateChecker