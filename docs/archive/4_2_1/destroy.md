---
layout: page
---
### 説明
親モデルを削除するときに子モデルを自動的に削除

### 使い方
    has_many :モデル名, :dependent => :destroy

### 例
    has_many :members, :dependent => :destroy