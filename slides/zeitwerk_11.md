### Zeitwerk

* Ruby 2.5でiseq cache + TracePointの挙動があやしい
  * Ruby 2.6では大丈夫
* Ruby 2.5でiseq cacheを活用しているライブラリとの相性があやしい
  * ようはbootsnap
* bootsnapは1.4.4以上だとRuby 2.5でiseq cacheを無効化するようにしている
  * Disable iseq cache in Ruby 2.5 https://github.com/Shopify/bootsnap/pull/257
