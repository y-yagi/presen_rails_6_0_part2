#### [Add `ActiveRecord::Relation#annotate` for adding SQL comments to ActiveRecord::Relation queries](https://github.com/rails/rails/pull/35617)

* queryにSQLコメントを追加する為のメソッド

```ruby
Post.where(id: 123).annotate("this is a comment").to_sql
# SELECT "posts".* FROM "posts" WHERE "posts"."id" = 123 /* this is a comment */
```

* 引数にはArrayを指定する事が出来、Arrayを指定した場合は別のコメントとして出力される

```ruby
User.annotate("selecting", "user", "names").select(:name)
# SELECT "users"."name" FROM "users" /* selecting */ /* user */ /* names */ LIMIT ?  [["LIMIT", 11]]
```

