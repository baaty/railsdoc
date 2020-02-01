---
layout: page
---
### 説明
ロケールファイルへのパス
デフォルトは、「config/locales/*.{yml,rb}」

### 使い方
    config.i18n.load_path

### 例
    config.i18n.load_path += Dir[Rails.root.join('config/locales/**/*.yml').to_s]