---
layout: page
---
### 説明
ミドルウェアスタックを入れ替える

### 使い方
    config.middleware.swap

### 例
    config.middleware.swap ActionController::Failsafe, Lifo::Failsafe