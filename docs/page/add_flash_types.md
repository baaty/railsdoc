---
layout: page
---

### 説明

フラッシュメッセージのタイプを指定  
フラッシュメッセージとは、エラー時などにページ上部に表示されるメッセージ

### 使い方

    add_flash_types(タイプ名..)

### 例

#### フラッシュメッセージのタイプを指定

    add_flash_types :warning

#### 複数指定

    add_flash_types :success, :info, :warning, :danger

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/flash.rb#L32)
