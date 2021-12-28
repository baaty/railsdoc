---
layout: page
---

### 説明

パフォーマンスの最適化を比較するためのベンチマークを生成

### 使い方

    $ rails generate benchmark ファイル名

コマンド実行後に「script/benchmarks/opt_compare.rb」が作成され、「ruby script/benchmarks/opt_compare.rb」で実行

### 例

    $ rails generate benchmark opt_compare
