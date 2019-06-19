#### [Move all npm packages to @rails scope](https://github.com/rails/rails/pull/34905)

* Railsで提供しているnpm packages@rails namespace配下に移動
* 古いpackageは更新されなくなる

```
actioncable   → @rails/actioncable
actiontext    → @rails/actiontext
activestorage → @rails/activestorage
rails-ujs     → @rails/ujs
```
