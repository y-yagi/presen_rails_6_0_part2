### multiple DB

* connected_toで接続先を指定出来る
  * 未指定の場合は最初に定義された接続先

```ruby
User.first
# => `primary` DBにアクセス

ActiveRecord::Base.connected_to(database: :animals) { Monkey.first }
# => `animals` DBにアクセス
```
