# fluent-plugin-kinesis-firehose

Fluentd output plugin for Amazon Kinesis Firehose.

[![Gem Version](https://badge.fury.io/rb/fluent-plugin-kinesis-firehose.svg)](http://badge.fury.io/rb/fluent-plugin-kinesis-firehose)
[![Build Status](https://travis-ci.org/winebarrel/fluent-plugin-kinesis-firehose.svg)](https://travis-ci.org/winebarrel/fluent-plugin-kinesis-firehose)

## Installation

Add this line to your application's Gemfile:

```ruby
gem 'fluent-plugin-kinesis-firehose'
```

And then execute:

    $ bundle

Or install it yourself as:

    $ gem install fluent-plugin-kinesis-firehose

## Configuration

```apache
<match kinesis.data>
  type kinesis_firehose

  delivery_stream_name DeliveryStreamName

  #profile ...
  #credentials_path ...
  #aws_key_id ...
  #aws_sec_key ...
  region us-east-1
  #endpoint ...

  #data_key data (default: nil)

  # Put a data_key value if data_key is set
  #   {... "data":"xxx" ...} -> xxx
  # Put a record as JSON if data_key is not set
  #   {... "data":"xxx" ...} -> {... "data":"xxx" ...}

  #append_new_line true

  #include_time_key false
  #include_tag_key false

  flush_interval 1s
</match>
```
