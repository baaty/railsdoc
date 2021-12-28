---
layout: page
---

### 説明

指定されたフィルタのみ含む新しいActionController::Parametersインスタンスを作成

### 使い方

    permit(フィルター..)

### 例

    params = ActionController::Parameters.new(user: { name: "Francesco", age: 22, role: "admin" })
    permitted = params.require(:user).permit(:name, :age)
    permitted.permitted?      #=> true
    permitted.has_key?(:name) #=> true
    permitted.has_key?(:age)  #=> true
    permitted.has_key?(:role) #=> false

### ソースコード

-   [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/strong_parameters.rb#L615)
