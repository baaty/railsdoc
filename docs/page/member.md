---
layout: page
---

### 説明

メンバールーティング(デフォルトで作成されるRESTfullなルーティング)を追加

### 使い方

    member(ブロック引数)

### 例

#### ブロックで追加

    resources :photos do
      member do
        get 'preview'
      end
    end

#### 単体で追加

    resouces :photos do
      get :preview, on: :member
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L1521)
