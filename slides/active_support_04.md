#### [Add support for event object to the Active Support notification system](https://github.com/rails/rails/pull/33451)

```ruby
# before
ActiveSupport::Notifications.subscribe('wait') do |*args|
  @event = ActiveSupport::Notifications::Event.new(*args)
end

ActiveSupport::Notifications.instrument('wait') { sleep 1 }

@event.duration # => 1000.138
```

```ruby
# after
ActiveSupport::Notifications.subscribe('wait') { |event| @event = event }

ActiveSupport::Notifications.instrument('wait') { sleep 1 }

@event.duration # => 1000.138
```
