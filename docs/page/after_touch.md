---
layout: page
---

### 説明

モデルをタッチするたびに実行  
コールバックメソッドの一つ

### 使い方

    モデル.touch(名前.., time: 時間=nil)

### 例

    product.touch
    # updates updated_at/on with current time

    product.touch(time: Time.new(2015, 2, 16, 0, 0, 0))
    # updates updated_at/on with specified time

    product.touch(:designed_at)
    # updates the designed_at attribute and updated_at/on

    product.touch(:started_at, :ended_at)
    # updates started_at, ended_at and updated_at/on attributes
