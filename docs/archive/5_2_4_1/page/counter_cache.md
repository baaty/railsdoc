---
layout: archive_page
---
### 説明
子モデルの数を親モデルのカラムに保存

### 概要
* デフォルトを0
* カラム名は、子モデルのテーブル名_countがおすすめ

### 使い方
    belongs_to(:親モデル, counter_cache: 親モデルのカラム)

### 例
#### Commentの登録や削除で、comments_countが自動更新
    def self.up
      add_column :entries, :comments_count, :integer, default: 0
    end

    belongs_to :entry, counter_cache: :comments_count