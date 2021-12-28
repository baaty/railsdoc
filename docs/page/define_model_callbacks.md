---
layout: page
---

### 説明

デフォルトのコールバックを上書き

### 使い方

    define_model_callbacks(アクション名: only: タイプ)

### タイプ

| タイプ  | 説明 |
| ------- | ---- |
| :after  | 後   |
| :before | 前   |
| :around | 前後 |

### 例

    define_model_callbacks :initializer, only: :after

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/callbacks.rb#L109)
