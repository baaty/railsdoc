---
layout: page
---

### 説明

各値に対して一度だけブロックを実行した結果を新しいActionController::Parametersを参照

### 使い方

    transform_values()

    # 失敗したら例外発生
    transform_values!()

### 例

    params = ActionController::Parameters.new({
    name: "Senjougahara Hitagi",
    oddity: "Heavy stone crab"
    })
    params.to_unsafe_h
    #=> {"name"=>"Senjougahara Hitagi", "oddity" => "Heavy stone crab"}


### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L730)
