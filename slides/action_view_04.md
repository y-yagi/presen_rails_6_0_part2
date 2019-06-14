#### Refactoring Action View

* そもそもdev環境でメモリリークが発生している、という問題があった
  * Rails development mode memory leak and slowdown, also on new apps https://github.com/rails/rails/issues/32892
* この対策としてviewレンダリング周りの処理の改善が行われた
  * (何か関係ないのも含まれているきがするが)
* Railsアプリの開発者は影響無いと思うが、Action Viewを拡張するgem作者は影響あると思います
