---
layout: archive_page
---
### 使い方
    #coding: utf-8
    require 'test_helper'
    class ArticleTest < ActiveSupport::TestCase
    test テスト名 do
    テストコード
    end

### 例
    class ShopTest < ActiveSupport::TestCase
      def test_instanciate_from_cvs_string
        shop = Ship.parse("コーヒー, aaa")
        assert_not_nil shop
        assert_equal "コーヒー", shop.name
        assert_equal "aaa", shop.tel
      end
    end

    class Shop < ActiveRecord::Base
      def self.parse(cvs_str)
      end
    end

    def self.parse(cvs_str)
      params = cvs_str.split(/\s*, \s*/)
      Shop.new(name: params[0], tel: params[1])
    end