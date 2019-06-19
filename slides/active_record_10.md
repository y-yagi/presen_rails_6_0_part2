#### [Add support in `#where` for endless ranges introduced in Ruby 2.6](https://github.com/rails/rails/pull/34906)

* whereでendless rangeが使えるよ

```ruby
User.where(id: 1..).to_sql
#=> "SELECT \"users\".* FROM \"users\" WHERE \"users\".\"id\" >= 1"
```

* PostgreSQLのrange typesにでもendless rangeが使えるよ
  * [PostgreSQL: Support endless range values for range types](https://github.com/rails/rails/commit/fd919ec881c8ae9e7c7e9251372109849b6888d8)
