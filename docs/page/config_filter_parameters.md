---
layout: page
---

### 説明

パスワードやカードナンバーなどの出力したくないパラメータなどを、出力しないようにする

### 使い方

    config.filter_parameters += [パラメータ]

### 例

    config.filter_parameters += [:password]
