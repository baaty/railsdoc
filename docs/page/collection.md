---
layout: page
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
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L1506)