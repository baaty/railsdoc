---
layout: page
---

### 説明

URLのidの部分にid以外のものを指定

### 使い方

    to_param()

### 例

    class User < ActiveRecord::Base
      def to_param  # overridden
        name
      end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/integration.rb#L57)
