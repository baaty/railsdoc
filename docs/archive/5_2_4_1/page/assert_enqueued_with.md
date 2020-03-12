---
layout: archive_page
---
### 説明
指定した引数でジョブを登録

### 使い方
    assert_enqueued_with([オプション])

### オプション

オプション  | 説明
-------|----
:job   | ジョブ
:args  | ジョブに渡す引数
:at    |
:queue | キュー

### 例
#### 指定した引数でジョブを登録
    MyJob.perform_later(1,2,3)
    assert_enqueued_with(job: MyJob, args: [1,2,3], queue: 'low')

#### ジョブに渡す引数を指定
    MyJob.perform_later(foo: 'bar', other_arg: 'No need to check in the test')
    assert_enqueued_with(job: MyJob, args: expected_args, queue: 'low')

#### ブロックで渡す
    assert_enqueued_with(job: MyJob, args: [1,2,3], queue: 'low') do
      MyJob.perform_later(1,2,3)
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activejob/lib/active_job/test_helper.rb#L300)