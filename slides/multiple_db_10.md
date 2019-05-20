### multiple DB

* Railsはデフォルトで書き込み用のロールとしてwriting、読み込み用のロールとしてreadingという名前を使用している
  * ロール名は変更可能
  * このロール名は後で説明するRackミドルウェアで使用される

```ruby
ActiveRecord::Base.reading_role # => :reading
ActiveRecord::Base.writing_role # => :writing

ActiveRecord::Base.reading_role = :readonly
ActiveRecord::Base.writing_role = :default

ActiveRecord::Base.reading_role # => :default
ActiveRecord::Base.writing_role # => :readonly
```
