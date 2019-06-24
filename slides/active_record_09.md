#### [Add the ability to filter out sensitive data in `#inspect`](https://github.com/rails/rails/pull/33756)

* #inspect及び#pretty_printでattributesを出力する際に、特定のattributeの値をfilter出来るようになった
  * filterしたい値はfilter_attributesで指定できる

```ruby
User.first.inspect
#=> "#<User id: 1, name: \"Taro\", secret: \"secret\", created_at: \"2018-09-07 13:01:28\", updated_at: \"2018-09-07 13:01:28\">"

ActiveRecord::Base.filter_attributes = [:secret]

User.first.inspect
#=> "#<User id: 1, name: \"Taro\", secret: [FILTERED], created_at: \"2018-09-07 13:01:28\", updated_at: \"2018-09-07 13:01:28\">"
```

* デフォルトでは、Rails.application.config.filter_parametersに指定されている値がfilter_attributesに指定される
