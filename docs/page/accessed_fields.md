---
layout: page
---

### 説明

モデルから読み込まれたすべてのデータベース・フィールドの名前を取得  
開発するときにどのフィールドを選択する必要があるかを判断するのに役立つ

### 使い方

    モデル.accessed_fields()

### 例

    class PostsController < ActionController::Base
        after_action :print_accessed_fields, only: :index

        def index
            @posts = Post.all
        end

        private

        def print_accessed_fields
            p @posts.first.accessed_fields
        end
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activerecord/lib/active_record/attribute_methods.rb#L376)
