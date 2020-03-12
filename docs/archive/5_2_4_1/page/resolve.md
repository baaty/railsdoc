---
layout: archive_page
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
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionpack/lib/action_dispatch/routing/mapper.rb#L2149)