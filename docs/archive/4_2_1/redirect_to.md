---
layout: page
---
### 説明
指定されたページにリダイレクト

### 使い方
    redirect_to(リダイレクト先のURL [, :status => ステイタスコード, オプション])

### ステータスコード

シンボル                   | コード | 説明
---------------------- | --- | -----------------
:ok                    | 200 | 成功
:created               | 201 | リソースの生成に成功
:moved_permanently     | 301 | リソースが永続的にリダイレクト
:found                 | 302 | リソースが一時的にリダイレクト
:see_other             | 303 | リソースが別の場所にある
:bad_request           | 400 | 不正なリクエスト
:unauthorized          | 401 | 未承認
:forbidden             | 403 | アクセス禁止
:not_found             | 404 | リソースが存在しない
:method_not_allowed    | 405 | HTMLメソッドが許可されていない
:internal_server_error | 500 | 内部サーバエラー

### オプション

オプション                  | 説明
---------------------- | ------------------
:alert => メッセージ        | エラーメッセージを表示
:notice => メッセージ       | 通知用のメッセージを表示
:flash => {パラメータ => 値} | パラメータを使って、一時的に値を保存

### 例
#### 現在のコントローラのshowアクションへのリダイレクト
    redirect_to :action => "show"

#### アクションがshowのid=5へリダイレクト
    redirect_to :action => "show", :id => 5

#### 同一ホストのファイルへリダイレクト
    redirect_to "/images/screenshot.jpg"

#### URLへリダイレクト
    redirect_to "<a href="http://www.rubyonrails.org">http://www.rubyonrails.org</a>"

#### 前のページへリダイレクト
    redirect_to :back

#### statusコード302を返す
    redirect_to :action=>'atom', :status => 302

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/2090615d39c071c9eb25e715275eb79f3f9b6266/actionpack/lib/action_controller/metal/redirecting.rb#L69)