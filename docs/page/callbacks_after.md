---
layout: page
---
### 説明
リクエストの後に実行する処理

### 使い方
    ActionDispatch::Callbacks.after

### 例
    ActionDispatch::Callbacks.after do
      load 'filename_in_lib'
      # or
      Dir.entries("#{Rails.root}/lib").each do |entry|
        load entry if entry =~ /.rb$/
      end
    end

### ソースコード
* [GitHub]()