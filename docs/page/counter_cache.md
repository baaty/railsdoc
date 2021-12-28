---
layout: page
---

### 説明

子モデルの数を親モデルのカラムに保存

### 概要

- デフォルトを0
- カラム名は、子モデルのテーブル名\_countがおすすめ

### 使い方

    belongs_to(:親モデル, counter_cache: 親モデルのカラム)

### 例

    def self.up
      add_column :entries, :comments_count, :integer, default: 0
    end

    belongs_to :entry, counter_cache: :comments_count
