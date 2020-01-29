---
layout: page
---
### 説明
空のモデルオブジェクトを取得する

### 使い方
    モデル.none()

### 例
    @posts = current_user.visible_posts.where(name: params[:name])
    # => the visible_posts method is expected to return a chainable Relation

    def visible_posts
      case role
      when 'Country Manager'
        Post.where(country: country)
      when 'Reviewer'
        Post.published
      when 'Bad User'
        Post.none # => returning [] instead breaks the previous code
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/0399b71dab8b270b4e40b2aff99194a8b8f2596c/activerecord/lib/active_record/relation/query_methods.rb#L690)