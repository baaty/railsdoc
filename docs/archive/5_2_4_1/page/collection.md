---
layout: archive_page
---
### 説明
ルーティングにコレクションを追加

### 使い方
    resources XXX do
      collection do
        追加したいルーティング
      end
    end

### 例
#### ブロックで追加
    resources :photos do
      collection do
        get 'search'
      end
    end

#### 単体で追加
    resouces :photos do
      get :search, on: :collection
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/routing/mapper.rb#L1483)