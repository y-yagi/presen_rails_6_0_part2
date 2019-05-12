### Zeitwerk

* STIのケースは自動では解決出来ない
* preload用のAPIが提供されているので、それをユーザ側で使用する必要がある

```ruby
sti_leaves = %w(
  app/models/leaf1.rb
  app/models/leaf2.rb
  app/models/leaf3.rb
)
Rails.autoloaders.main.preload(sti_leaves)
```
