---
layout: page
---
### 説明
モデルオブジェクトを生成
保存はまだされていないため、saveメソッドなどを使って保存
生成と同時に保存したい場合は、createメソッドを使用

### 使い方
    モデル.new([属性])

### 例
#### モデルオブジェクトを生成
    user = User.new

#### 属性を設定してモデルオブジェクトを生成
    user = User.new(:name => "tarou")

#### 属性を設定してモデルオブジェクトを生成(Ruby1.9以上)
    user = User.new(name: "tarou")