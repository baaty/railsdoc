---
layout: archive_page
---
### アセットパイプラインとは
JavaScriptやCSSを結合したり圧縮して連結するためのフレームワーク。また、CoffeeScriptやSass、ERBの言語を使ってJavaScriptやCSSを書くことも可能

### 特徴
* JavaScriptやCSSを結合することによって、ブラウザでのリクエスト回数を削減
* JavaScriptやCSSを圧縮
* SassやCoffeeScript、もしくはERBを使って記述可能
* 「/app/assets/」「/lib/assets/」「/vendor/assets/」のディレクトリ
* 「/app/assets/YYY/XXX」に置いたファイルは、「http://localhost:3000/assets/XXX」でアクセスが可能
* /app/assets/」以下のサブディレクトリは、アクセスする際には無視

### URLとファイルパス

| URL                            | パス                                           |
|--------------------------------|----------------------------------------------|
| /assets/application.js<ファイル名> | app/assets/javascripts/application.js        |
| /assets/models/test.js<ファイル名> | app/assets/javascripts/models/test.js.coffee |
| /assets/style.js<ファイル名>       | app/assets/stylesheets/style.js              |
| /assets/lib_test.js            | /lib/assets/lib.js                           |
| /assets/vendort.js             | /vendor/assets/vendort.js                    |

### その他
#### Asset Pipelineのパスの確認法法
    Rails.application.config.assets.paths