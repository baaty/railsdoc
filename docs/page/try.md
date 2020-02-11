---
layout: page
---
### try
#### 説明
オブジェクトがnilの時やメソッドが定義されていない場合はnilを返す  
メソッドが定義されている場合はそのメソットを呼び出す

#### 使い方
    オブジェクト.try(メソッド)

#### 例
##### メソッドが定義されていない場合やオブジェクトがnilの時にnilを返す
    @person.try(:name)
    # @person.name if @personと同じ

##### tryを重ねる
    @person.try(:spouse).try(:name)

##### nilの場合
    @person.try(:non_existing_method)x
    # nil

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/object/try.rb#L101)

### try!
#### 説明
オブジェクトがnilの時にnilを返し、メソッドが定義されている場合はそのメソットを呼び出す  
メソッドが定義されていない場合は例外が発生  
Rubyのぼっち演算子と同じ処理で、ぼっち演算子の方が高速なので、ぼっち演算子がおすすめ

#### 使い方
    オブジェクト.try(メソッド)

#### 例
##### メソッドが定義されている場合はそのメソットを呼び出す
    @person.try!(:name)

##### tryを重ねる
    @person.try!(:spouse).try(:name)!

##### nilの場合
    @person.try!(:non_existing_method)x
    # nil

#### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activesupport/lib/active_support/core_ext/object/try.rb#L113)

### &.
#### 説明
オブジェクトがnilの時にnilを返し、メソッドが定義されている場合はそのメソットを呼び出す  
メソッドが定義されていない場合は例外が発生  
基本的にはtry!と同じ  
Ruby2.3以降に追加されたRubyのメソッド

#### 使い方
    nil.try(:name) # => nil

#### 例
##### メソッドが定義されている場合はそのメソットを呼び出す
    @person&.name