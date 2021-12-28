---
layout: page
---

### 説明

キャッシュのポリシーを設定

### 使い方

    expires_in(有効期限, オプション={})

### オプション

| オプション              | 説明                                                                          |
| ----------------------- | ----------------------------------------------------------------------------- |
| :no-cache               | キャッシュを無効化                                                            |
| :no-store               | 返されたデータをキャッシュに記録しない                                        |
| :max-age                | キャッシュの有効性の再確認をせずに、データに保持できる最大期間                |
| :max-stale              | 有効期限の切れたデータを許可する                                              |
| :min-fresh              | 最新のデータを取得する                                                        |
| :no-transform           | メディアタイプを変更しない                                                    |
| :only-if-cached         | キャッシュからデータを取得                                                    |
| :cache-extension        | トークンを使って拡張                                                          |
| :public                 | キャッシュされたデータを複数ユーザで共有                                      |
| :private                | キャッシュされたデータを共有しない                                            |
| :must-revalidate        | キャッシュの有効期間を必ず問い合わせる                                        |
| :proxy-revalidate       | プロキシサーバにキャッシュの有効性を確認                                      |
| :s-maxage               | 基本的な機能は、max-ageと同じ。ただし、こちらは共有キャッシュにだけ適用される |
| :stale_while_revalidate | stale_while_revalidate                                                        |
| :stale_if_error         | stale_if_error                                                                |

### 例

#### キャッシュの有効期限を20分

    expires_in 20.minutes

#### キャッシュを共有

    expires_in 20.minutes, public: true

### ソースコード

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/actionpack/lib/action_controller/metal/conditional_get.rb#L276)
