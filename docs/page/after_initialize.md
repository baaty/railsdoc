---
layout: page
---

### 説明

モデルが作成される時に実行

### 使い方

    after_initialize do(ブロック引数)

### 例

    after_initialize do |user|
      puts "初期化"
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/railties/lib/rails/railtie/configuration.rb#L70)
