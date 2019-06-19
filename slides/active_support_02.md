#### [Add cpu time, idle time, and allocations features to log subscriber events](https://github.com/rails/rails/pull/33449)

* ActiveSupport::Notifications::Eventが保持するデータに、cpu time, idle time, 及びオブジェクトの数を追加
  * Action Viewのtemplate renderingで表示しているAllocationsはこの値を使用している
* この対応で時間を取得するのにCLOCK_MONOTONICを使用するようになったが、これは非互換という事で後ほどrevertされた
  * 最終的に、ActiveSupport::Notifications.monotonic_subscribeという別のメソッドにする事で対応
  * [Introduce ActiveSupport::Notifications.monotonic_subscribe](https://github.com/rails/rails/pull/36184)
