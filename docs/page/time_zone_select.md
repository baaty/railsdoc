---
layout: page
---

### 説明

タイムゾーンの選択ボックス

### 使い方

    time_zone_select(オブジェクト名, メソッド名, プライオリティゾーン=nil, オプション={}, HTML属性={} or イベント属性={})

    # f.object
    f.time_zone_select(メソッド名, プライオリティゾーン=nil, オプション={}, HTML属性={} or イベント属性={})

### オプション

| オプション     | 説明                               | デフォルト値 |
| -------------- | ---------------------------------- | ------------ |
| :multiple      | 複数選択を有効にするか             |              |
| :disabled      | 無効化                             | false        |
| :include_blank | 先頭に空の要素を追加するか         |              |
| :prompt        | 選択されていない時に表示される文字 |              |

### HTML属性

| HTML属性   | 説明                                 |
| ---------- | ------------------------------------ |
| :accept    | フォームで受付可能なMIMEタイプ       |
| :readonly  | フォームの内容変更禁止               |
| :tabindex  | Tabキーによる入力欄の移動順          |
| :accesskey | フォームに移動するショートカットキー |
| :id        | 要素固有の識別子                     |
| :class     | 要素を分類するクラス名               |
| :title     | 要素の補足情報                       |
| :style     | 要素の補足情報                       |
| :dir       | 表記方向                             |
| :lang      | 基本言語                             |

### イベント属性

| イベント属性 | 説明                                   |
| ------------ | -------------------------------------- |
| :onclick     | クリックされた時                       |
| :ondblclick  | ダブルクリックされた時                 |
| :onmousedown | マウスのボタンが押し下げられた時       |
| :onmouseup   | マウスのボタンが離された時             |
| :onmouseover | カーソルが重なった時                   |
| :onmousemove | カーソルが移動した時                   |
| :onmouseout  | カーソルが離れた時                     |
| :onkeypress  | キーが押されて離された時               |
| :onkeydown   | キーが押し下げられた時                 |
| :onkeyup     | キーが離された時                       |
| :onfocus     | フォーカスされた時                     |
| :onblur      | フォーカスを失った時                   |
| :onchange    | フォーカスを失う際に値が変化していた時 |

### 例

#### タイムゾーンの選択ボックス

    time_zone_select(:user, :time_zone, nil, include_blank: true)
    time_zone_select(:user, :time_zone, nil, default: "Pacific Time (US & Canada)")
    time_zone_select(:user, :time_zone, ActiveSupport::TimeZone.us_zones, default: "Pacific Time (US & Canada)")
    time_zone_select(:user, :time_zone, [ ActiveSupport::TimeZone["Alaska"], ActiveSupport::TimeZone["Hawaii"] ])
    time_zone_select(:user, :time_zone, /Australia/)
    time_zone_select(:user, :time_zone, ActiveSupport::TimeZone.all.sort, model: ActiveSupport::TimeZone)

#### タイムゾーンの選択ボックス(f.object)

    form_for @user do |f|
        f.time_zone_select :time_zone, nil, include_blank: true
        f.submit
    end

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L291)
- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionview/lib/action_view/helpers/form_options_helper.rb#L881)
