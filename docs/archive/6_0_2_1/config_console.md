---
layout: page
---
### 説明
使用するコンソールを設定する。ブロックで指定するのがよい

    console do
      # this block is called only when running console,
      # so we can safely require pry here
      require "pry"
      config.console = Pry
    end</p>

    <h4>使い方</h4>
    <pre>config.console do
      設定
    end

### 例
    console do
      require "pry"
      config.console = Pry
    end