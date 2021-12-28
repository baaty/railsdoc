---
layout: page
---

### 説明

モデルのURLマッピングを定義
resolveではnamespaceやスコープブロックないでは使用不可

### 使い方

    resolve(名前.., ブロック引数)

### 例

    resource :basket
    resolve "Basket" do
      [:basket]
    end
    # Basketモデルでlink_toが生成するパスが/baskets/:idではなく/basketに変更

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/routing/mapper.rb#L2176)
