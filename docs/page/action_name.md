---
layout: page
---
### 説明
アクション名を取得

### 使い方
#### コントローラから取得
    action_name

#### ビューから取得
    controller.action_name

### 例
#### ビューでアクション名によって処理を変更
    case controller.action_name
    when "new"
      puts "新規作成"
    else
      puts ""
    end

#### コントローラでアクション名によって処理を変更
    case action_name
    when "new"
      puts "新規作成"
    else
      puts ""
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/abstract_controller/base.rb#L25)