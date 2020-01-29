---
layout: page
---
### 説明
アクションの実行前にチェック

### 使い方
    verify オプション

### オプション

オプション        | 説明
------------ | ------------------------
:params      | パラメータがあるかどうか
:session     | セッションにキーがあるかどうか
:flash       | フラッシュの中に指摘したキーのデータあるかどうか
:method      | HTTPのメソッドが指定したものかどうか
:xhr         | アクションがAjaxから呼ばれたかどうか
:add_flash   | フラッシュにデータを追加
:add_headers | HTTPのヘッダに「カラム名:値」を追加
:redirect_to | 別のアクションにリダイレクト
:render      | 別のアクションのテンプレートでレンダリング
:only        | 適用するアクション
:except      | 適応しないアクション

### 例
#### セッションにuser_idがない場合は、indexにリダイレクト
    verify :session => "user_id", :redirect_to { :action => "index" }

#### POSTでアクセスしていない場合は、indexにリダイレクト
    verify :method => :post, :redirect_to { :action => "index" }

#### create, update, deleteアクション以外は、indexにリダイレクト
    verify :only => [:create, :update, :delete], :redirect_to { :action => "index" }