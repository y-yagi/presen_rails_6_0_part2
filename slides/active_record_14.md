#### [Add `touch_all` method to `ActiveRecord::Relation`](https://github.com/rails/rails/pull/31513)

* 名前の通り複数のレコードに対してtouchする為のメソッド

```ruby
Person.where(name: 'David').touch_all
# => "UPDATE \"people\" SET \"updated_at\" = '2018-01-04 22:55:23.132670' WHERE \"people\".\"name\" = 'David'"
```

