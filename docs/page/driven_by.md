---
layout: page
---

### 説明

システムテストの設定オプション

### 使い方

    driven_by(ドライバ, using: 使うブラウザ=:chrome, screen_size: スクリーンサイズ=[1400, 1400], options: オプション={})

### 例

    driven_by :cuprite
    driven_by :selenium, screen_size: [800, 800]
    driven_by :selenium, using: :chrome
    driven_by :selenium, using: :headless_chrome
    driven_by :selenium, using: :firefox
    driven_by :selenium, using: :headless_firefox

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_dispatch/system_test_case.rb#L156)
