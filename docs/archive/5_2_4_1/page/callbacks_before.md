---
layout: archive_page
---
### 説明
リクエストの前に実行する処理

### 使い方
    ActionDispatch::Callbacks.before

### 例
     ActionDispatch::Callbacks.before do
      if Object.const_defined?(:Example)
        if Example.const_defined?(:MyClass)
          Example.send(:remove_const, :MyClass)
         end
      end

      require 'example/my_class'
    end