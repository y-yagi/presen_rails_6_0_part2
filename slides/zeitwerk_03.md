### Zeitwerk


```ruby
module Admin
  class UsersController < ApplicationController
    def index
      @users = User.all
    end
  end
end
```

vs

```ruby
class Admin::UsersController < ApplicationController
  def index
    @users = User.all
  end
end
```

