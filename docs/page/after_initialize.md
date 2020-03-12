---
layout: page
---
### 説明
モデルが作成される時に実行

### 使い方
    after_initialize do |x|
      実行したい処理
    end

### 例
#### モデルが作成される時に実行
    after_initialize do |user|
      puts "初期化"
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/railties/lib/rails/railtie/configuration.rb#L70)