---
layout: page
---
### 説明
初期化の最後に実行する処理を追加

主に環境ごとに設定が異なる場合などに使われる

### 使い方
    config.after_initialize do
     処理の内容
    end

### 例
    config.after_initialize do
      ActionView::Base.sanitized_allowed_tags.delete 'div'
    end