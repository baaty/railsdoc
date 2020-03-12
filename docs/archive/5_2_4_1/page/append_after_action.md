---
layout: archive_page
---
### 説明
アクションの後に処理を追加  
after_actionより後に処理

### 使い方
    append_after_action(コールバック名 [, オプション])

### オプション

オプション   | 説明
--------|------------
:only   | 実行するアクション
:except | 実行しないアクション
:if     | 実行する条件を指定
:unless | 実行されない条件を指定

### 例
#### アクションの後に処理を追加
    append_after_action :verify_same_origin_request
    def verify_same_origin_request
      if marked_for_same_origin_verification? && non_xhr_javascript_response?
        logger.warn CROSS_ORIGIN_JAVASCRIPT_WARNING if logger
        raise ActionController::InvalidCrossOriginRequest, CROSS_ORIGIN_JAVASCRIPT_WARNING
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/abstract_controller/callbacks.rb#L156)