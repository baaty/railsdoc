---
layout: page
---
### 説明
主キーを設定して、複数のレコードを追加

### 使い方
    モデル.concat(モデル)

### 例
    person.pets.concat(Pet.new(name: 'Fancy-Fancy'))
    person.pets.concat(Pet.new(name: 'Spook'), Pet.new(name: 'Choo-Choo')

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0e50b7bdf4c0f789db37e22dc45c52b082f674b4/actionview/lib/action_view/helpers/text_helper.rb#L52)