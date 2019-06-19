#### [Add `#destroy_by` and `#delete_by` for conditional removals](https://github.com/rails/rails/pull/35316)

* 条件を指定してのdestroyを行う為メソッド
  * where(condition).destroy_all とwhere(condition).delete_all のショートハンド

```ruby
Person.destroy_by(id: 13)
Person.delete_by("published_at < ?", 2.weeks.ago)
```
