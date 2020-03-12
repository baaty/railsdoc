---
layout: archive_page
---
### 説明
バリデーションの別クラスにレコードを渡して、より複雑な条件に基づいたエラーを追加

### 使い方
    validates_with(引数)

### 例
    validates_with MyValidator

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activemodel/lib/active_model/validations/with.rb#L137)