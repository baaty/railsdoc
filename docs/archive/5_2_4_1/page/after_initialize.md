---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/railties/lib/rails/railtie/configuration.rb#L70)