---
layout: page
---

### 説明

EtagとLast-Modifiedからリクエストが古いかチェック

### 使い方

    stale?(オブジェクト=nil, **freshness_kwargs)

### 例

    @article = Article.find(params[:id])
    stale?(etag: @article, last_modified: @article.updated_at)

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/conditional_get.rb#L249)
