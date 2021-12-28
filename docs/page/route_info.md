---
layout: page
---

### 説明

URLとアプリケーションのパラメータを結びつける仕組み

### 説明

- 設定ファイルは、「config/routes.rb」
- 優先順位は、上から順

### デフォルトの設定

    match ':controller(/:action(/:id(.:format)))'

- http&#x3A;// ホスト名:ポート番号/:controller/:action/:id
- params[:id]でパラメータidの値を取得
