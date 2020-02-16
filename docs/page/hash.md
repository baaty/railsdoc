---
layout: page
---
### 説明
ハッシュ関係の便利関数

### from_trusted_xml
#### 説明
XMLからハッシュを生成

#### 使い方
    Hash.from_trusted_xml(xml)

#### 例
    Hash.from_trusted_xml(xml)
    # {"hash"=>{"foo"=>1, "bar"=>2}}

### from_xml
#### 説明
XMLからハッシュを生成

#### 使い方
    Hash.from_xml(xml)

#### 例
    Hash.from_xml(xml)
    # {"hash"=>{"foo"=>1, "bar"=>2}}

### assert_valid_keys
#### 説明
指定したキーがあるかバリデーション

#### 使い方
    ハッシュ.assert_valid_keys(キー名, ...)

#### 例
    { name: 'Rob', years: '28' }.assert_valid_keys(:name, :age)
    # raises "ArgumentError: Unknown key: :years. Valid keys are: :name, :age"

    { name: 'Rob', age: '28' }.assert_valid_keys('name', 'age')
    # raises "ArgumentError: Unknown key: :name. Valid keys are: 'name', 'age'"

    { name: 'Rob', age: '28' }.assert_valid_keys(:name, :age)
    # passes, raises nothing

### deep_dup
#### 説明
ハッシュのディープコピー

#### 使い方
    ハッシュ.deep_dup

#### 例
    hash = { a: { b: 'b' } }
    dup  = hash.deep_dup
    dup[:a][:c] = 'c'
    hash[:a][:c] # nil
    dup[:a][:c]  # "c"

### deep_merge
#### 説明
ハッシュのディープコピー

#### 使い方
    ハッシュ.deep_merge(ハッシュ)

#### 例
    h1 = { a: true, b: { c: [1, 2, 3] } }
    h2 = { a: false, b: { x: [3, 4, 5] } }
    h1.deep_merge(h2)
    # { a: false, b: { c: [1, 2, 3], x: [3, 4, 5] } }

### deep_merge!
#### 説明
ハッシュのディープコピー
破壊的メソッド

#### 使い方
    ハッシュ.deep_merge!(ハッシュ)

#### 例
    h1 = { a: true, b: { c: [1, 2, 3] } }
    h2 = { a: false, b: { x: [3, 4, 5] } }
    h1.deep_merge!(h2)
    # { a: false, b: { c: [1, 2, 3], x: [3, 4, 5] } }

### deep_stringify_keys
#### 説明
全てのキーを文字列にしたハッシュに変換

#### 使い方
    ハッシュ.deep_stringify_keys

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_stringify_keys
    # {"person"=>{"name"=>"Rob", "age"=>"28"}}

### deep_stringify_keys!
#### 説明
全てのキーを文字列にしたハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.deep_stringify_keys!

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_stringify_keys!
    # {"person"=>{"name"=>"Rob", "age"=>"28"}}

### deep_symbolize_keys
#### 説明
全てのキーをシンボルにしたハッシュに変換

#### 使い方
    ハッシュ.deep_symbolize_keys

#### 例
    hash = {person: {name: 'Rob', age: '28'}}
    hash.deep_symbolize_keys
    # {:person=>{:name=>"Rob", :age=>"28"}}

### deep_symbolize_keys!
#### 説明
全てのキーをシンボルにしたハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.deep_symbolize_keys!

#### 例
    hash = {person: {name: 'Rob', age: '28'}}
    hash.deep_symbolize_keys!
    # {:person=>{:name=>"Rob", :age=>"28"}}

### deep_transform_keys
#### 説明
ブロック内で変換されたキーを含むハッシュに変換

#### 使い方
    ハッシュ.deep_transform_keys{|key| 処理 }

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_transform_keys{ |key| key.to_s.upcase }
    # {"PERSON"=>{"NAME"=>"Rob", "AGE"=>"28"}}

### deep_transform_keys!
#### 説明
ブロック内で変換されたキーを含むハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.deep_transform_keys!{|key| 処理 }

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_transform_keys!{ |key| key.to_s.upcase }
    # {"PERSON"=>{"NAME"=>"Rob", "AGE"=>"28"}}

### deep_transform_values
#### 説明
ブロック内で変換された値を含むハッシュに変換

#### 使い方
    ハッシュ.deep_transform_values{|key| 処理 }

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_transform_values{ |value| value.to_s.upcase }
    # {person: {name: "ROB", age: "28"}}

### deep_transform_values!
#### 説明
ブロック内で変換された値を含むハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.deep_transform_values!{|key| 処理 }

#### 例
    hash = { person: { name: 'Rob', age: '28' } }
    hash.deep_transform_values!{ |value| value.to_s.upcase }
    # {person: {name: "ROB", age: "28"}}

### except
#### 説明
指定されたキーを除外したハッシュに変換

#### 使い方
    ハッシュ.except(キー名, ...)

#### 例
    { a: true, b: false, c: nil }.except(:c)
    # { a: true, b: false }

    { a: true, b: false, c: nil }.except(:a, :b)
    # { c: nil }

### except!
#### 説明
指定されたキーを除外したハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.except!(キー名, ...)

#### 例
    { a: true, b: false, c: nil }.except!(:c)
    # { a: true, b: false }

    { a: true, b: false, c: nil }.except!(:a, :b)
    # { c: nil }

### reverse_merge
#### 説明
逆順でマージ

#### 使い方
    ハッシュ.reverse_merge(ハッシュ)

#### 例
    options.reverse_merge(size: 25, velocity: 10)

### reverse_merge!
#### 説明
逆順でマージ
破壊的メソッド

#### 使い方
    ハッシュ.reverse_merge!(ハッシュ)

#### 例
    options.reverse_merge!(size: 25, velocity: 10)

### slice!
#### 説明
指定されたキーのみのハッシュに変換。戻り値として、削除されたハッシュを返す
破壊的メソッド

#### 使い方
    ハッシュ.slice!(キー名)

#### 例
    hash = { a: 1, b: 2, c: 3, d: 4 }
    hash.slice!(:a, :b)  # {:c=>3, :d=>4}
    hash                 # {:a=>1, :b=>2}

### stringify_keys
#### 説明
全てのキーを文字列にしたハッシュに変換

#### 使い方
    ハッシュ.stringify_keys

#### 例
    hash = { name: 'Rob', age: '28' }
    hash.stringify_keys
    # {"name"=>"Rob", "age"=>"28"}

### stringify_keys!
#### 説明
全てのキーを文字列にしたハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.stringify_keys!

#### 例
    hash = { name: 'Rob', age: '28' }
    hash.stringify_keys!
    # {"name"=>"Rob", "age"=>"28"}

### symbolize_keys
#### 説明
全てのキーをシンボルにしたハッシュに変換

#### 使い方
    ハッシュ.symbolize_keys

#### 例
    hash = {name: 'Rob', age: '28'}
    hash.symbolize_keys
    # {:name=>"Rob", :age=>"28"}

### symbolize_keys!
#### 説明
全てのキーをシンボルにしたハッシュに変換
破壊的メソッド

#### 使い方
    ハッシュ.symbolize_keys!

#### 例
    hash = {name: 'Rob', age: '28'}
    hash.symbolize_keys!
    # {:name=>"Rob", :age=>"28"}

### to_query
#### 説明
URLとして使える文字列に変換

#### 使い方
    ハッシュ.to_query([名前空間名]))

#### 例
    {name: 'David', nationality: 'Danish'}.to_query
    # "name=David&nationality=Danish"

    {name: 'David', nationality: 'Danish'}.to_query('user')
    # "user%5Bname%5D=David&user%5Bnationality%5D=Danish"

### to_xml
#### 説明
XMLに変換

#### 使い方
    ハッシュ.to_xml([オプション]))

#### 例
    { foo: 1, bar: 2 }.to_xml
    # <?xml version="1.0" encoding="UTF-8"?>
    # <hash>
    #   <foo type="integer">1</foo>
    #   <bar type="integer">2</bar>
    # </hash>