---
layout: page
---
### 説明
条件を指定して初めの1件を取得し、1件もなければ作成

### 使い方
    モデル.find_or_initialize_by(条件)

#### 新しいレコードが無効な場合に例外
    モデル.find_or_initialize_by!(条件)

### 例
#### 存在しないので新しく作成
    User.find_or_initialize_by(first_name: 'Penélope')

#### 既に存在する場合は既存のレコードを取得
    User.find_or_initialize_by(first_name: 'Penélope')

#### ブロック指定
    User.find_or_initialize_by(first_name: 'Scarlett') do |user|
      user.last_name = "O'Hara"
    end

### 補足
* find_or_create_byとの違いは、作成する時に呼ぶメソッドがcreateではなくnew

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation.rb#L226)