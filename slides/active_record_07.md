#### [Add negative scopes for all enum values](https://github.com/rails/rails/pull/35381)

* enumでnegative scope(not_xxx)も定義するようになった
  * メソッド名のコンフリ気をつけてね

```ruby
class Post < ActiveRecord::Base
  enum status: %i[ drafted active trashed ]
end

Post.not_drafted # => where.not(status: :drafted)
Post.not_active  # => where.not(status: :active)
Post.not_trashed # => where.not(status: :trashed)
```
