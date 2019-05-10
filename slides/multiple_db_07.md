### multiple DB

モデルで接続先を指定することもできる

```ruby
class Monkey < ApplicationRecord
  connects_to database: { writing: :animals }
end
```

```ruby
Monkey.first
# => `animals` DBにアクセス
```
