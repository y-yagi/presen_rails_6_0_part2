#### [Add `ActiveRecord::Base.create_or_find_by`/`!`](https://github.com/rails/rails/pull/31989)

* createしてレコードが既にある場合(ActiveRecord::RecordNotUniqueでエラーになった場合)にfindを実行

```ruby
def create_or_find_by(attributes, &block)
  transaction(requires_new: true) { create(attributes, &block) }
rescue ActiveRecord::RecordNotUnique
  find_by!(attributes)
end
```
