#### [Add ability to see the output of `rails routes` in expanded format](https://github.com/rails/rails/pull/32130)

* rails routesコマンドに結果を縦に表示する為の"--expanded"オプションを追加
  * psqlの"--expanded"と同じ形

```
./bin/rails routes --expanded
--[ Route 1 ]------------------------------------------------------------
Prefix            | users
Verb              | GET
URI               | /users(.:format)
Controller#Action | users#index
--[ Route 2 ]------------------------------------------------------------
Prefix            |
Verb              | POST
URI               | /users(.:format)
Controller#Action | users#create
```
