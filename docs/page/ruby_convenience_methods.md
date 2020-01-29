---
layout: page
---
### 配列
#### 配列をランダムに取り出す
    [:aaa, :bbb, :ccc].rand

#### 配列を分割
    [1, 2, 3, 4, 5].split(3)

#### 配列をグループ化
    %w(1 2 3 4 5).in_groups_of(4){ |g| p g }

#### 特定のキーからハッシュを作る
    User.find(:all).index_by(&:login)

### ハッシュ
#### ハッシュの差を取得
    {one: 1, two: 2, three: 3 }.diff(one: 0, two: 2, four: 4)

#### ハッシュから特定の値を取り除く
    hash.except(:controller, :action)

#### ハッシュから特定の値だけど取り出す
    hash.slice(:title, :body)

#### 元のハッシュの内容を優先してマージ
    hash.reverse_merge(template: "entries/list")