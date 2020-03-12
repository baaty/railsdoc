---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activerecord/lib/active_record/relation.rb#L176)