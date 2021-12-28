---
layout: page
---

### 説明

システムテストとは、ブラウザ上で行うアプリケーションのテスト  
実際のブラウザを使用するためJavaScriptを簡単にテストすることができる

### 例

    require "application_system_test_case"
    class Users::CreateTest < ApplicationSystemTestCase
        test "adding a new user" do
            visit users_path
            click_on 'New User'

            fill_in 'Name', with: 'Arya'
            click_on 'Create User'

            assert_text 'Arya'
        end
    end