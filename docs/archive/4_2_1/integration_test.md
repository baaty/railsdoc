---
layout: page
---
### 説明
複数のアクションやコントローラにまたがる挙動を検証するためのテスト

### テストを生成
    $ rails generate integration_test テスト名

### 流れ
1.  テスト環境をセットアップ
2.  リクエストとその検証、というペアを複数回記述

### テストを記述
* /shops/listに店の一覧がある
    * 新規追加画面に店を追加するためのフォームがある
* /shops/newに店を追加するためのフォームがある
    * フォームのアクションは/shops/createである
    * shopの店名を入力するためのフォームがある
* shop[name]を指定し、/shops/createにPOSTリクエストを送る
* shopの件数が増えていることを検証
    class CreateNewShopFinallyShowThemAllTest < AxtionController::IntegrationTest
      fixtures :users, :shops

      def test_create_new_shop_and_show_thwm_all
        shops_count_before_create = Shop.count

        get "/shops/list"
        assert_response :success
        assert_select "table > tr", :count => (shops_count_before_create + 1)
        assert_select "a[href=?]", %r!/shops/new!

        get "/shops/new"
        assert_response :success
        assert_select "form[action=?]", %r!/shops/create!
        assert_select "form input[name='shop[name]']"

        post_via_redirect "/shops/create", :shops => { :name => "new_shop" }
        assert_response :seccess
        assert_template "shops/list"

        assert_equal (shops_count_before_create +1), Shop.count
      end
    end