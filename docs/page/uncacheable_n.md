---
layout: page
---

### 説明

キャッシュブロック内から呼び出された場合にUncacheableFragmentErrorが発生

### 使い方

    uncacheable!()

### 例

    def project_name_with_time(project)
      uncacheable!
      "#{project.name} - #{Time.now}"
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/cache_helper.rb#L205)
