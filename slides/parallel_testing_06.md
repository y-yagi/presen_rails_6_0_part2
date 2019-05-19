### Parallel Testing

* Parallel Testingはがっつりminitestに依存している
  * 元々minitestにParallel Testingのための機能がありそれを使用している
  * ワーカにスレッドを使用した場合の実装はminitestの機能そのまま
  * Railsではワーカにプロセスを使用した場合の実装が提供されている
* そのため、RSpecユーザがそのまま使用出来るような機能ではない
  * Add support for Rails 6 built-in Parallel Testing(https://github.com/rspec/rspec-rails/issues/2104)
