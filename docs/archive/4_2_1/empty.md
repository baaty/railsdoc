---
layout: page
---
### 説明
条件式を評価し，true（真）かnilやfalse（偽）を判定

### 使い方
#### nil?
    変数.nil?

Rubyの標準メソッド。nilの場合のみtrueを返し、それ以外はfalseを返す

#### empty?
    変数.empty?

Rubyの標準メソッド。空の文字列や空の配列の場合にtrueを返す。nilに対して呼び出すとNoMethodErrorが発生

#### blank?
    変数.blank?

nil? + empty? のようなメソッド。nilまたは空のオブジェクトをチェック
nil, "", " "(半角スペースのみ), [](空の配列), {}(空のハッシュ) のときにfalseを返します
Railsで拡張されたメソッドで、Rubyのみでは使えないのでご注意ください

#### present?
    変数.present?

!blank? を実行するメソッド。if 変数.present?とunless 変数.blank?は同じ意味
nil, "", " "(半角スペースのみ), [](空の配列), {}(空のハッシュ) のときにfalseを返します
Railsで拡張されたメソッドで、Rubyのみでは使えないのでご注意ください

### 例
    @pages = Page.all
    if @pages.present?
    ...
    else
    puts "no pages"
    end