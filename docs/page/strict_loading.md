---
layout: page
---

### 説明

返されたリレーションをstrict_loadingモードに設定

### 使い方

    モデル.strict_loading(値=true)

    # 失敗したら例外発生
    モデル.strict_loading!(値=true)

### 例

    user = User.strict_loading.first
    user.comments.to_a
    => ActiveRecord::StrictLoadingViolationError

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/relation/query_methods.rb#L981)
