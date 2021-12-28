---
layout: page
---

### 説明

指定した個数のジョブが登録されているか確認

### 使い方

    assert_enqueued_jobs(個数, only: 特定のジョブが何回エンキューされた=nil, except: 特定のクラスを除くジョブが何回キューイングされたか=nil, queue: 特定のキューにジョブがエンキューされた回数をアサート=nil, ブロック引数)

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

- [GitHub](https://github.com/rails/rails/blob/984c3ef2775781d47efa9f541ce570daa2434a80/activejob/lib/active_job/test_helper.rb#L123)
