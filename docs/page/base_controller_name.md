---
layout: page
---
### 説明
コントローラのクラス名を取得

### 使い方
    ActionController::Base.controller_name

### 例
#### 基本形(オプションなし)
    EntriesController.controller_name
    # "entries"

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/metal.rb#L129)