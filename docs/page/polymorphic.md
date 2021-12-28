---
layout: page
---

### 説明

- belongs_to宣言に:polymorphicオプションを指定すると、ポリモーフィック関連になる
- 参照先となるモデルをあらかじめ定義せず、参照元となるオブジェクトごとに指定する関連

### 使い方

- 参照元となるモデルに対応するテーブルに、参照先のＩＤと参照先クラスを指定するカラムをそれぞれ生成
- 参照先のＩＤを保存するカラムは｢belongs_to宣言で渡す関連名\_id」
- 参照先クラスを指定するカラムは｢関連名type」

#### 例

##### ポリモーフィック関連を利用するマイグレーションファイルの生成

    $ rails generate model AttachmentImage attachable_id:integer attachable_type:string

    class CreateAttachmentImage < ActiveRecord::Migration
      def self.up
        create_table :attachment_images do |t|
          t.integer :attachable_id
          t.string :attachable_type

        t.timestamps
      end
    end

##### ボリモーフイツク関連を利用する宣言

    class AttachmentImage < ActiveRecord::Base
      belongs_to :attachable, polymorphic: true
    end

    class Blog < ActiveRecord::Base
      has_many :entries
      has_one :attachment_image, as: :attachable
    end

    class Entry < ActiveRecord::Base
      belongs_to :blog
    end

    def self.down
      drop_table :attachment_images
    end
