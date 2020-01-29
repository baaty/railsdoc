---
layout: page
---
### 説明
フラッシュタイプの指定

### 使い方
    # in application_controller.rb
    class ApplicationController < ActionController::Base
      add_flash_types :タイプ名
    end

    # controller
    redirect_to xxx, タイプ名: "メッセージ"

    # view
    <%= タイプ名 %>

### 例
    # in application_controller.rb
    class ApplicationController < ActionController::Base
      add_flash_types :warning
    end

    # controller
    redirect_to user_path(@user), warning: "Incomplete profile"

    # view
    <%= warning %>

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/1413ee991ccfc76b24f29eb03c9cff82e588e5d7/actionpack/lib/action_controller/metal/flash.rb#L31)