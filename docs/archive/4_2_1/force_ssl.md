---
layout: page
---
### 説明
特定のコントローラをHTTPSリクエストに強制

### 使い方
    force_ssl([オプション])

### オプション

オプション     | 説明
--------- | ----------------------------------------------------------------
host      | Redirect to a different host name
subdomain | Redirect to a different subdomain
domain    | Redirect to a different domain
port      | Redirect to a non-standard port
path      | Redirect to a different path
status    | Redirect with a custom status (default is 301 Moved Permanently)
flash     | Set a flash message when redirecting
alert     | Set an alert message when redirecting
notice    | Set a notice message when redirecting
only      | The callback should be run only for this action
except    | The callback should be run for all actions except this action
if        |  symbol naming an instance method or a proc; the callback
unless    | A symbol naming an instance method or a proc; the callback

### 例
    class AccountsController < ApplicationController
      force_ssl if: :ssl_configured?

      def ssl_configured?
        !Rails.env.development?
      end
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ea7fc2e7c0aba43b0c54309d292d982e52ee1b3d/actionpack/lib/action_controller/metal/force_ssl.rb#L62)