---
layout: page
---

### テストメソッド

| メソッド                                                              | 説明                                                                                  |
| --------------------------------------------------------------------- | ------------------------------------------------------------------------------------- |
| assert(式 \[, メッセージ\])                                           | 式が真ならば成功                                                                      |
| assert_equal(変数1, 変数2 \[, メッセージ\])                           | 変数1と変数2が等しければ成功                                                          |
| assert_not_equal(変数1, 変数2 \[, メッセージ\])                       | 変数1と変数2が等しくなければ成功                                                      |
| assert_nil(変数 \[, メッセージ\])                                     | 変数がnilならば成功                                                                   |
| assert_not_nil(変数 \[, メッセージ\])                                 | 変数がnilじゃなければ成功                                                             |
| assert_match(正規表現, 文字列 \[, メッセージ\])                       | 正規表現に文字列がマッチすれば成功                                                    |
| assert_no_match(正規表現, 文字列 \[, メッセージ\])                    | 正規表現に文字列がマッチしなければ成功                                                |
| assert_raise(例外1, 例外2 \[, 例外3...\]) { }                         | ブロックを実行して例外1,2が発生し、その例外がexpected_exception_klassクラスならば成功 |
| assert_nothing_raised(例外1, 例外2 \[, 例外3...\]) { .. }             | ブロックを実行して例外1,2がおきなけらば成功                                           |
| assert_in_delta(expected_float, actual_float, delta, message="")      |                                                                                       |
| flunk(\[メッセージ\])                                                 | 常に失敗。未定義のテストケースなどを暫定的に失敗させたりする場合に利用                |
| assert_difference(expressions, difference = 1, message = nil, 6block) | ブロック実行後にecpressionsの値がdifferenceの分だけ変わっていれば成功                 |
| assert_no_difference(exoressions, message = nil, &block)              | ブロック実行前後でexpressionsの値が変わっていなければ成功                             |
