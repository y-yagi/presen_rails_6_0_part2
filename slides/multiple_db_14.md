### multiple DB

* 接続先の指定はロールで行う
  * デフォルトの場合、書き込み処理はwriting、読み込み処理はreadingというロールが使用される
  * connects_toでそれぞれのロールで使用するDBを指定する必要がある

```ruby
class ApplicationRecord < ActiveRecord::Base
  self.abstract_class = true
  connects_to database: { writing: :primary, reading: :primary_replica }
end
```
