---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_controller/metal/flash.rb#L32)