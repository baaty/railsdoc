---
layout: page
---
### 説明
データベースに初期データを投入

### 使い方
    $ rake db:seed

### 書き方
#### １件ずつ記述
    # db/seeds.rb
    Category.create(:name => "Railsの基礎知識", :position => 1)
    Category.create(:name => "Rubyの基礎知識", :position => 2)

#### まとめて記述
    # db/seeds.rb
    5.times do |i|
         Page.create(:name => "テスト #{i}", :category_id => 1)
    end