---
layout: page
---
### 説明
条件を指定して初めの1件を取得し、1件もなければ作成

### 使い方
    モデル.find_or_create_by(条件)

#### 新しいレコードが無効な場合に例外
    モデル.find_or_create_by!(条件)

### 例
#### 存在しないので新しく作成
    User.find_or_create_by(first_name: 'Penélope')
    # <User id: 1, first_name: 'Penélope', last_name: nil>

#### 既に存在する場合は既存のレコードを取得
    User.find_or_create_by(first_name: 'Penélope')
    # <User id: 1, first_name: 'Penélope', last_name: nil>

#### ブロック指定
    User.find_or_create_by(first_name: 'Scarlett') do |user|
      user.last_name = "O'Hara"
    end
    # <User id: 2, first_name: 'Scarlett', last_name: 'Johansson'>

### 補足
* find_or_create_byとの違いは、作成する時に呼ぶメソッドがnewではなくcreate

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L168)