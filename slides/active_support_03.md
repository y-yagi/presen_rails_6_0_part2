#### [Add support for event object to the Active Support notification system](https://github.com/rails/rails/pull/33451)

* AS::Notifications.subscribeのブロックに指定したパラメータが一つだけだった場合、ActiveSupport::Notifications::Eventのインスタンスをブロックに渡すよう変更
* 元々、AS::Notifications.subscribeのブロックに渡されるパラメータはeventに関する各種情報(名前、payload等)で、AS::Notifications::Eventのインスタンスが必要な場合、それらのパラメータを使って、明示的にオブジェクトの生成処理を行う必要があった
* この対応により、AS::Notifications::Eventのインスタンスが必要な場合、AS::Notifications.subscribeのブロックから直接受け取れるようになった
