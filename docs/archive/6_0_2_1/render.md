---
layout: page
---
### 説明
* 指定したRHTML
* 対応しているテンプレートを呼ぶ際は、このメソッドを呼ぶ必要はない

### 注意点
* 同じアクション内でrenderメソッドを複数呼び出すと、エラーになるので、and returnを付ける

### 使い方
    render(オプション)

#### オプション

オプション  | 説明
--------- | -----------------------------------------
:action   | 他のアクションのテンプレートを表示
:partial  | 部分テンプレートを呼び出して表示
:template | テンプレートを指定して表示
:layout   | レイアウトを指定
:file     | ファイルを指定して表示
:text     | 任意のテキストを指定して表示
:xml      | 指定されたテキストを表示し、コンテンツタイプをapplication/xmlに設定
:json     | 指定されたテキストを表示し、コンテンツタイプをtext/x-jsonに設定
:update   |  ブロックで処理を行い表示
:inline   | ビューとするソースコードを直接指定
:nothing  | 何も表示しない
:status   | ステータスコードを制御

### render :action
#### 説明
他のアクションのテンプレートを表示

#### 使い方
    render(action: "アクション名" [, layout: レイアウト名])

#### 例
##### 「_new.html.erb」を表示
    render action: "new"

##### 他のレイアウトを使用
    render action: "new", layout: "user"

##### レイアウトは使用しない
    render action: "new", layout: false

### render :template
#### 説明
他のコントローラのテンプレートを表示

#### 使い方
    render template: コントローラ名/アクション名

#### 例
##### 他のコントローラのテンプレートを表示
    render template: "user/show"

### render :file
#### 説明
アプリケーション外のテンプレートを表示

#### 使い方
    render file: ファイルパス

#### 例
##### 「/common/template/index」を表示
    render file: "/common/template/index"

### render :text
#### 説明
文字列を直接表示

#### 使い方
    render text: "文字列"

#### 例
##### レイアウトを適用
    render text: "文字例", layout: true

##### エラーメッセージの表示
    render text: "文字例", status: 500

##### 「hello world!」を表示
    render text: "hello world!"

##### 文字列とstatusコード500を返す
    render text: "Explosion!", status: 500

##### レイアウトを使用して文字列を表示
    render text: "Hi there!", layout: true

### render :partial
#### 説明
部分テンプレート

#### 使い方
    render partial: "部分テンプレート名"

#### 例
##### _page.rhtmnlを使って表示
    render partial: "page"

##### 部分テンプレートを繰り返し表示
    render partial: "user", collections: @users

##### 部分テンプレートにローカル変数を渡す
    render partial: "user", locals: { val1: xxx, val2: xxx }

### render :inline
#### 説明
アプリケーション外のテンプレートを表示

#### 使い方
    render inline: テンプレート文字列

#### 例
##### 現在の時刻を表示
    render inline: "<%= Time.now %>"

### render :layout
#### 説明
レイアウトを指定

#### 使い方
    render layout: レイアウト名 [, オプション]

#### オプション

オプション   | 説明
------- | ----------------------
:only   | 指定されたアクションにだけ、レイアウトを適用
:except | 指定されたアクション以外にレイアウトを適用

#### 例
##### pageのレイアウトを使用
    render layout: 'page'

### render :xml
#### 説明
指定されたテキストを表示し、コンテンツタイプをapplication/xmlに設定

#### 使い方
    render xml: モデル or 文字列

#### 例
##### pagesテーブルの内容をXML形式で出力
    @pages = Page.all
    render xml: @pages

### render :json
#### 説明
指定されたテキストを表示し、コンテンツタイプをapplication/xmlに設定

#### 使い方
    render json: モデル or 文字列

#### 例
##### pagesテーブルの内容をJSON形式で出力
    @pages = Page.all
    render json: @pages

### render :nothing
#### 説明
何も出力しない。:statusオプションと組み合わせて、エラーコードを返す時などに使う

#### 使い方
    render nothing: true

#### 例
##### 404コード
    render nothing: true, status: 404

### その他
#### renderを複数使用
##### 説明
renderを複数回呼び出すとエラーになるため、条件分岐した後「and return」で明示的に終了させる

##### 使い方
    render オプション and return

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/f33d52c95217212cbacc8d5e44b5a8e3cdc6f5b3/actionpack/lib/action_controller/renderer.rb#L87)