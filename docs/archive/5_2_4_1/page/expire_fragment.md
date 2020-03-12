---
layout: archive_page
---
### 説明
フラグメントキャッシュを破棄

### 使い方
    expire_fragment(キャッシュキー [,  オプション])

### キャッシュキー
キャッシュキーは次の3つの形式
* 文字列
* ハッシュ
* 正規表現

### 例
#### 文字列
    expire_fragment "detail"

#### ハッシュ
    expire_fragment :controller => 'posts', :action => 'show', :id => post.id

#### 正規表現
    expire_fragment %r{/*/user/home}

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/abstract_controller/caching/fragments.rb#L148)