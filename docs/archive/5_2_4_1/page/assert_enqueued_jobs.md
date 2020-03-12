---
layout: archive_page
---
### 説明
指定した個数のジョブが登録されているか確認

### 使い方
    assert_enqueued_jobs(個数 [, オプション])

### オプション

オプション   | 説明
--------|-------------
:only   | 指定したジョブを確認
:except | 指定したジョブ以外を確認
:queue  | キューを指定

### 例
#### 指定した個数のジョブが登録されているか確認
    assert_enqueued_jobs 0
    HelloJob.perform_later('david')
    assert_enqueued_jobs 1
    HelloJob.perform_later('abdelkader')
    assert_enqueued_jobs 2

#### ブロックで渡す
    assert_enqueued_jobs 1 do
      HelloJob.perform_later('cristian')
    end

#### 指定したジョブを確認
    assert_enqueued_jobs 1, only: LoggingJob do
      LoggingJob.perform_later
      HelloJob.perform_later('jeremy')
    end

#### 指定したジョブ以外を確認
    assert_enqueued_jobs 1, except: HelloJob do
      LoggingJob.perform_later
      HelloJob.perform_later('jeremy')
    end

#### キューを指定
    assert_enqueued_jobs 2, queue: 'default' do
      LoggingJob.perform_later
      HelloJob.perform_later('elfassy')
    end

### ソースコード
* [GitHub](https://github.com/rails/rails/blob/ac30e389ecfa0e26e3d44c1eda8488ddf63b3ecc/activejob/lib/active_job/test_helper.rb#L118)