#### [Add `Relation#pick` as short-hand for single-value plucks](https://github.com/rails/rails/pull/31941)

* single-valueを取得する為のメソッド
* pluck同様、record objectは生成せずに値だけを取得する
  * limit(1).pluck(*column_names).firstのショートハンド

```ruby
Person.where(id: 1).pick(:name)
# SELECT people.name FROM people WHERE id = 1 LIMIT 1
# => 'David'

Person.where(id: 1).pick(:name, :email_address)
# SELECT people.name, people.email_address FROM people WHERE id = 1 LIMIT 1
# => [ 'David', 'david@loudthinking.com' ]
```
