### Parallel Testing

* Parallel Testingはがっつりminitest依存している
  * 元々minitestにParallel Testingのための機能がありそれを使用している
  * ワーカーにスレッドを使用した場合の実装はminitestの機能そのまま
* そのため、RSpecユーザがそのまま使用出来るような機能ではない
