---
layout: page
---

### 説明

オブジェクトがnilの時やメソッドが定義されていない場合はnilを返す  
メソッドが定義されている場合はそのメソットを呼び出す

### 使い方

    オブジェクト.try(引数.., ブロック引数)

    # 失敗したら例外発生
    オブジェクト.try(引数.., ブロック引数)

### 例

#### メソッドが定義されていない場合やオブジェクトがnilの時にnilを返す

    @person.try(:name)
    # @person.name if @personと同じ

#### tryを重ねる

    @person.try(:spouse).try(:name)

#### nilの場合

    @person.try(:non_existing_method)x
    # nil

#### 失敗したら例外発生

    @person.try!(:name)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/object/try.rb#L7)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/core_ext/object/try.rb#L148)
