---
layout: page
---
### 説明
モデルのURLマッピングを定義 
resolveではnamespaceやスコープブロックないでは使用不可

### 使い方
    resolve(名前) do
      定義内容
    end

### 例
#### モデルのURLマッピングを定義 
    resource :basket
    resolve "Basket" do
      [:basket]
    end
    # Basketモデルでlink_toが生成するパスが/baskets/:idではなく/basketに変更

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_dispatch/routing/mapper.rb#L2171)