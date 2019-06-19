#### [Add allocations to template renderer subscription](https://github.com/rails/rails/pull/34136)

* template rendering instrumentationでAllocationsの値(GC.stat :total_allocated_objectsの値)を表示するようになった

```
  Rendering posts/new.html.erb within layouts/application
  Rendered posts/_form.html.erb (Duration: 7.1ms | Allocations: 6004)
  Rendered posts/new.html.erb within layouts/application (Duration: 8.3ms | Allocations: 6654)
Completed 200 OK in 858ms (Views: 848.4ms | ActiveRecord: 0.4ms | Allocations: 1539564)
```

