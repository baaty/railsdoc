---
layout: page
---

### 説明

コントローラのアクション内で呼び出し可能な_renderersに名前を付けてレンダラーを追加

### 使い方

    use_renderers(引数..)

### 例

    class MetalRenderingController < ActionController::Metal
        include AbstractController::Rendering
        include ActionController::Rendering
        include ActionController::Renderers
        use_renderers :json
        def show
            render json: record
        end
    end

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/renderers.rb#L129)
