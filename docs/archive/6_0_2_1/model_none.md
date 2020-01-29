---
layout: page
---
### 説明
空のモデルオブジェクトを取得

### 使い方
    モデル.none()

### 例
    @posts = current_user.visible_posts.where(name: params[:name])
    # the visible_posts method is expected to return a chainable Relation

    def visible_posts
      case role
      when 'Country Manager'
        Post.where(country: country)
      when 'Reviewer'
        Post.published
      when 'Bad User'
        Post.none # returning [] instead breaks the previous code
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/activerecord/lib/active_record/relation/query_methods.rb#L800)