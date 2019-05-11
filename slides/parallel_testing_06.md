### Parallel Testing

* Parallel Testingはがっつりminitestの機能に依存している
  * 元々minitestにParallel Testingのための機能がありそれを使用している
  * ワーカーにスレッドを使用した場合の実装はminitestの機能
* そのため、RSpecユーザがそのまま使用出来るような機能ではない
