---
layout: page
---
### 説明
使用するコンソールを設定  
consoleブロックで指定するのがよい

### 使い方
    console do
      config.console = クラス名
    end

### 例
    console do
      require "pry"
      config.console = Pry
    end