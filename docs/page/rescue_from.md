---
layout: page
---

### 説明

例外処理をまとめる

### 使い方

    rescue_from(例外.., with: メソッド=nil, ブロック引数)

### 例

#### 例外処理をまとめる

    rescue_from User::NotAuthorized, with: :deny_access

#### ブロック

    rescue_from ActiveRecord::RecordNotFound do |exception|
      render json: { error: '404 not found' }, status: 404
    end

#### 

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activesupport/lib/active_support/rescuable.rb#L51)
