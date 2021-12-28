---
layout: page
---

### 説明

アクティブレコード(Active Record)でのエラーを表示するためのHTMLジェネレーター。デフォルトは、

    Proc.new do |html_tag, instance|
      %Q(<div class="field_with_errors">#{html_tag}</div>).html_safe
    end

### 使い方

    config.action_view.field_error_proc

### 例

    config.action_view.field_error_proc = Proc.new { |html_tag, instance|
      "#{html_tag}".html_safe
    }
