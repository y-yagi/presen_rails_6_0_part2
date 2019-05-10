### multiple DB

```ruby
class Monkey < ApplicationRecord
  connects_to database: { wr: :animals }
end
```

```ruby
ActiveRecord::Base.connected_to(role: :wr) { Monkey.first }
```
