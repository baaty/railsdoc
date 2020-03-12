---
layout: archive_page
---
### 説明
表示させるviewファイルを指定して表示

### 使い方
    render(表示方法 [, オプション])

### 表示方法

表示方法  | 説明
----------|-----------------------------------------
:action   | 他のアクションのテンプレートを表示
:partial  | 部分テンプレートを呼び出して表示
:template | テンプレートを指定して表示
:text     | 任意のテキストを指定して表示
:xml      | 指定したテキストを表示し、コンテンツタイプをapplication/xmlに設定
:json     | 指定したテキストを表示し、コンテンツタイプをtext/x-jsonに設定
:update   | ブロックで処理を行い表示
:file     | ファイルを指定して表示
:inline   | ビューとするソースコードを直接指定
:plain    | 平文テキストを表示
:html     | HTML文字列を表示
:js       | JavaScriptを表示
:body     | 生のコンテンツを表示

### オプション

オプション         | 説明
--------------|----------------
:content_type | content-typeを変更
:layout       | レイアウトを指定
:location     | HTTPのLocationヘッダーを設定
:status       | ステータスコードを制御
:formats      | フォーマット指定

### 注意点
* 同じアクション内でrenderメソッドを複数呼び出すと、エラーになるので、and returnを付ける


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

##### templateを省略
    render "user/show"

### render :file
#### 説明
アプリケーション外のテンプレートを表示  
「/」で始まる場合はファイル出力と認識するので、fileオプションは省略可能

#### 使い方
    render file: ファイルパス

#### 例
##### 「/common/template/index」を表示
    render file: "/common/template/index"

##### fileを省略
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

#### 例
##### 404コード
    render nothing: true, status: 404

### render :plain
#### 説明
平文テキストを表示

#### 使い方
    render plain: 文字列

#### 例
##### OK
    render plain: "OK

### render :html
#### 説明
平文テキストを表示

#### 使い方
    render html: 文字列

#### 例
##### Not Found
    render html: helpers.tag.strong('Not Found')

### render :js
#### 説明
JavaScriptを表示

#### 使い方
    render js: 文字列

#### 例
##### JavaScriptを表示
    render js: "alert('Hello Rails');"

### render :body
#### 説明
生のコンテンツを表示

#### 使い方
    render body: 文字列

#### 例
##### JavaScriptを表示
    render body: "raw"

### その他
#### renderを複数使用
##### 説明
renderを複数回呼び出すとエラーになるため、条件分岐した後「and return」で明示的に終了させる

##### 使い方
    render オプション and return

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/actionview/lib/action_view/helpers/rendering_helper.rb#L27)