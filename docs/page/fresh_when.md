---
layout: page
---

### 説明

レスポンスにetagとlast_modifiedを設定してリクエストが新しい場合は「304 Not Modified」レスポンスを表示

### 使い方

    fresh_when(オブジェクト), etag: ETag=nil, weak_etag: 弱いETag=nil, strong_etag: 強いETag=nil, last_modified: 最終更新日のバリデータを設定=nil, public: キャッシュ可能にしたいか=false, cache_control: Cache-Controlヘッダー={}, template: テンプレート=nil)

### 例

#### リクエストが新しい場合は「304 Not Modified」レスポンスを表示

    @article = Article.find(params[:id])
    fresh_when(@article)

#### last_modifiedを指定

    @article = Article.find(params[:id])
    fresh_when(etag: @article, last_modified: @article.updated_at, public: true)

#### cache_controlを指定

    @article = Article.find(params[:id])
    fresh_when(@article, public: true, cache_control: { no_cache: true })

#### templateを指定

    @article = Article.find(params[:id])
    fresh_when(@article, template: 'widgets/show')

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/conditional_get.rb#L117)
