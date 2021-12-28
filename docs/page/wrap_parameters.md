---
layout: page
---

### 説明

ParamsWrapperが属性名を決定するために使用するモデルを設定

### 使い方

    wrap_parameters(属性やモデルなど, オプション={})

### オプション

| 名前     | 説明                                           |
| -------- | ---------------------------------------------- |
| :format  | 有効になるフォーマットのリスト                 |
| :include | ハッシュにラップする属性名のリスト             |
| :exclude | ネストされたハッシュから除外する属性名のリスト |

### 例

#### XMLフォーマットのパラメータラッパーを有効

    wrap_parameters format: :xml

#### ハッシュにラップ

    wrap_parameters :person

#### include指定

    wrap_parameters include: [:username, :title]

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/params_wrapper.rb#L220)
