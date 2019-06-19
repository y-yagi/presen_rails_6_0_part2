#### [Add support for event object to the Active Support notification system](https://github.com/rails/rails/pull/33451)

* ActiveSupport::Notifications.subscribeのブロックに指定したパラメータが一つだけだった場合、ActiveSupport::Notifications::Eventのインスタンスをブロックに渡すよう変更
* 元々、ActiveSupport::Notifications.subscribeのブロックに渡されるパラメータはeventに関する各種情報(eventの名前、開始時刻、終了時刻、payload等)で、ActiveSupport::Notifications::Eventのインスタンスが必要な場合、それらのパラメータを使って、明示的にオブジェクトの生成処理を行う必要があった
* この対応により、ActiveSupport::Notifications::Eventのインスタンスが必要な場合、ActiveSupport::Notifications.subscribeのブロックから直接受け取れるようになった
