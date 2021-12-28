---
layout: page
---

### 説明

バリデーションの別クラスにレコードを渡してより複雑な条件に基づいたエラーを追加

### 使い方

    validates_with(引数.., ブロック引数)

### 例

    validates_with MyValidator

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activemodel/lib/active_model/validations/with.rb#L137)
