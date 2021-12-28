---
layout: page
---
### 説明
バリデーションの別クラスにレコードを渡して、より複雑な条件に基づいたエラーを追加

### 使い方
    validates_with(引数)

### 例
    validates_with MyValidator

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activemodel/lib/active_model/validations/with.rb#L137)