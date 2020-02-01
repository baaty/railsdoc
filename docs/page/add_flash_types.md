---
layout: page
---
### 説明
エラー時などにページ上部に表示されるメッセージ(フラッシュメッセージ)のタイプを指定

### 使い方
    add_flash_types(:タイプ名)

### 例
#### フラッシュメッセージのタイプを指定
      add_flash_types :warning

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal/flash.rb#L32)