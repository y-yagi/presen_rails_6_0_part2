#### [Add `ActiveRecord::Base.create_or_find_by`/`!`](https://github.com/rails/rails/pull/31989)

* create_or_find_by! はcreateではなくcreate!を使用する
* find_or_create_byだとfind(select)とcreate(insert)の間にレコードが追加されてしまった場合にエラーになってしまうので、そのようなケースを避けるよう
* insertに失敗した場合もprimary keyの値はインクリメントされる
  * primary keyにintegerを使用している場合、integerの上限への注意が必要
  * [Document int Primary Key issue with `create_or_find_by`](https://github.com/rails/rails/pull/35573)
