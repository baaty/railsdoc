---
layout: page
---
### 説明
フラッシュメッセージのタイプを指定  
フラッシュメッセージとは、エラー時などにページ上部に表示されるメッセージ

### 使い方
    add_flash_types(:タイプ名 [, ...])

### 例
#### フラッシュメッセージのタイプを指定
    add_flash_types :warning

#### 複数指定
    add_flash_types :success, :info, :warning, :danger

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/flash.rb#L32)