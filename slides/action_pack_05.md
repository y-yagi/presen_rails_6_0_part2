#### [Add purpose and expiry metadata inside signed/encrypted cookies to prevent copying the value of cookies into one another](https://github.com/rails/rails/pull/32937)

* メタデータが埋め込まれたcookieは古いバージョンで作られたcookieと互換性がないので注意が必要
  * メタデータはデフォルトでは無効されており、action_dispatch.use_cookies_with_metadataにtrueを指定した場合のみ有効化される
* GSoC案件
  * https://gist.github.com/assain/fed04b9b610b8c190566a1956f523cc1
