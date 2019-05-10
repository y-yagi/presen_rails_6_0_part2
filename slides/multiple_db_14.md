### multiple DB

* マスター / レプリカの指定はロールで行う
  * 先に説明した通り、デフォルトの場合、マスターはwriting、レプリカはreadingというロール

```ruby
class ApplicationRecord < ActiveRecord::Base
  self.abstract_class = true
  connects_to database: { writing: :primary, reading: :primary_replica }
end
```
