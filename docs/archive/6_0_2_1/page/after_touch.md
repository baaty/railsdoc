---
layout: page
---
### 説明
モデルをタッチするたびに実行  
コールバックメソッドの一つ

### 使い方
    after_touch |x|
      実行したい処理
    end

### 例
#### モデルをタッチするたびに実行
    after_touch do |user|
      puts "タッチ"
    end