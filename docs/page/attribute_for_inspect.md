---
layout: page
---

### 説明

属性の値に似た文字列を取得  
50文字以降は省略  
日時などは:db形式で返却

### 使い方

    モデル.attribute_for_inspect(属性名)

### 例

#### 属性の値に似た文字列を取得

    person.attribute_for_inspect(:name)
    # "\"David Heinemeier Hansson David Heinemeier Hansson D...\""

#### 日時を取得

    person.attribute_for_inspect(:created_at)
    #=> "\"2012-10-22 00:15:07\""

#### 配列を取得

    person.attribute_for_inspect(:tag_ids)
    #=> "[1, 2, 3, 4, 5, 6, 7, 8, 9, 10, 11]"

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods.rb#L283)
