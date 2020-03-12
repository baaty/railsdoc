---
layout: archive_page
---
### 説明
単一のアクションに対して、モデル・ビュー・コントローラを結合してテスト

    requite File.dirname(__FILE__) + '/../test_helper'

    class EntriesControllerTest < ActionController::TestCase
      def test_truth
        assert true
      end
    end

### 流れ
#### テスト環境をセットアップ
    requite File.dirname(__FILE__) + '/../test_helper'

#### コントローラを指定
    requite File.dirname(__FILE__) + '/../test_helper'

    class ShopsControllerTest < Test::Unit**testCase
      def setup
        @controller = ShopsController.new
        @request = ActionController::TestRequest.new
        @response = ActionController:TestResponse.new
      end
    end

#### リクエストを送信
    def test_should_get_index
      get :index
    end

#### アクションの実行結果を確認
##### レスポンスが成功したかをバリデーション
    assert_response :success

##### アクション内で設定されたインスタンス変数をバリデーション
    assigns

##### 出力結果のHTMLをバリデーション
    assert_select

### テストメソッド
#### リクエスト送信のためのメソッド

メソッド                                                                      | 説明
------------------------------------------------------------------------- | --------------------------
get(action, parameters)                                                   | アクションに対して、GETリクエストを送信
post(action, parameters)                                                  | アクションに対して、POSTリクエストを送信
xhr(request_method, action, parameters = nil, session = nil, flash = nil) | アクションに対して、XMLHTTPRequestを送

#### 状態設定・取得のためのメソッド

メソッド             | 説明
-------------------- | --------------------------------------
assigns(key = nil) | アクションを実行した結果、インスタンス変数に代入されたオブジェクトを取得
session            | ファンクショナルテストで使用されるセッションへのアクセサ
flash              | コントローラ内で使用するflashへのアクセサ

#### バリデーションのためのメソッド

メソッド                                              | 説明
------------------------------------------------- | ---------------------------------------
assert_response(type, message = nil)              | アクション実行結果のレスポンスコードをバリデーション
assert_redirected_to(options = {}, message = nil) | リダイレクトを返すアクションに対して、そのリダイレクト先がどうなっているかバリデーション
assert_template(expected, message = nil)          | そのアクションで指定されたテンプレートが描写されているかをバリデーション
assert_select(selector, equality?, message?)      | アクション実行の結果として描写されるHTMLの内容をバリデーション