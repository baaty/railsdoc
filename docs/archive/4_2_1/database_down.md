---
layout: page
---
### 説明
データベースのカラムをバージョンダウン
Rails3.0以下では、self.upとself.downをセットに記述していたが、Rails3.1ではchangeメソッドのみで両方の処理を実行
Rails3.1以上では、downメソッドはロールバックできない処理の際に主に使用

### 使い方
    def down
    end

### 例
#### 基本的な使い方
    def down
      drop_table :pages
    end