#### [Add a `action_controller.default_enforce_utf8` configuration option to handle enforcing UTF-8 encoding. This defaults to `false`](https://github.com/rails/rails/pull/32125)

* `utf8=✓`がinput要素に生成されているようになっていたのを、デフォルトでは生成されないよう修正
  * 古いIE(8以下)でUnicodeでエンコードされるようにする為だったのですが、流石にもうええやろ、ということで
