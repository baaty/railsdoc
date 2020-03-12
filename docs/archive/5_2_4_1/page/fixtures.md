---
layout: archive_page
---
### 説明
事前に用意したテストデータを読み込み、常にDBの内容を一定に保つための仕組みのことを、フィクスチャと呼ぶ

### フィクスチャを用意
    test/fixtures/テーブル名.yml

### 例
    rubyonrails:
      id: 1
      name: Ruby on Rails
      url: http://www.rubyonrails.org

    google:
      id: 2
      ;name: Google
      url: http://www.google.com

### テスト内からフィクスチャを読み込む
    require 'test_helper'

    class WebSiteTest < ActiveSupport::TestCase
      test "web_site_count" do
        assert_equal 2, WebSite.count
      end
    end

### フィクスチャを使用
    require 'test_helper'

    class SiteTest < ActiveSupport::TestCase
      fixtures :sites

      def test_google_fixture
        # フィクスチャ名を指定して使用
        google = sites(:google)
        assert_equal "http://www.google.com", google.url
      end

      def test_google_fixture_from_db
        # findメソッドなどでDBからロードして使用
        google = Site.find(2)

        # フィクスチャ名で取得したものと同じであることをバリデーション
        assert_equal sites(:google), google.url
      end
    end

### フィクスチャからのデータの取得
フィクスチャに含まれているデータはテストの実行時に使うもの

* 開発用データ用のディレクトリの作成
    $ mkdir db/migrate/dev_data
* YAMLファイルの作成
* マイグレーションファイルの作成
    $ ruby script/generate migration <マイグレーション名>
* マイグレーションファイルの編集
    require 'active_recode/fixtures'
    class <クラス名> < ActiveRecode::Migration
      def self.up
        down

        directory = File.join(File.dirname(__FILE__), 'dwv_data')
        Fixtures.create_fixtures(disrectory, "<YAML名>")
      end
      def self.down
        YAML名.delete_all
      end
    end