#### [Add support for custom serializers for Active Job arguments](https://github.com/rails/rails/pull/30941)

```ruby
class MoneySerializer < ActiveJob::Serializers::ObjectSerializer
  def serialize(money)
    super("amount" => money.amount, "currency" => money.currency)
  end

  def deserialize(hash)
    Money.new(hash["amount"], hash["currency"])
  end

  private
    def klass
      Money
    end
end
```

```ruby
Rails.application.config.active_job.custom_serializers << MoneySerializer
```

<small>
https://github.com/rails/rails/tree/master/activejob/lib/active_job/serializers 辺りをご参考。
</small>
