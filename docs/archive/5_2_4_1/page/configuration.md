---
layout: archive_page
---
### ファイル名の規約

ディレクトリ             | ファイル                       | クラス名          | 親クラス
------------------ | -------------------------- | ------------- | -----------------------
app/controllers/   | xxxs_controller.rb         | XxxController | ApplicationController
app/models/        | xxx.rb                     | Xxx           | ActiveRecord::Base
app/views/xxxs/    | yyy.html.erb               |               |
app/views/layouts/ | xxx.html.erb               |               |
app/helpers/       | xxxs_helper.rb             |               |
db/migrate/        | YYYYMMDDhhmiss_mmm_xxxs.rb | MmmXxxs       | ActiveRecord::Migration
test/fixtures/     | xxx.yml                    |               |

* xxx : コントローラ名、モデル名
* yyy : アクション名
* mmm: マイグレーション名
* YYYYMMDDhhmiss は作成日時が入る

### テーブル定義についての規約
#### テーブル名とクラス名
* テーブル名は複数形
* 単語の区切りはアンダーバー(_)
* 対応するクラス名は単語の先頭を大文字にして _ を取り除いたもの

#### キーのカラム名
* 主キーのカラム名は「id」
* 外部キーのカラム名は「テーブル名の単数_id」

#### 日付関連のカラム名
* DATE型のカラムには名前を「受動態_on」
* TIMESTAMP型のカラムには名前を「受動態_at」
* 更新日時、作成日時は「updated_at」「created_at」

#### 結合テーブル
* 関連させたいテーブル名をくっつけた名前
* カラム「id」を作らずに、関連させる2つのキーのセットを主キー