---
layout: page
---

### 説明

アクションのパラメータのエンコーディングを指定

### 使い方

    param_encoding(アクション名, パラメータ, エンコードの種類)

### 例

    param_encoding :show, :file_path, Encoding::ASCII_8BIT

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/parameter_encoding.rb#L77)
