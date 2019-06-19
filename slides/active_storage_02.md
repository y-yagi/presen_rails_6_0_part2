#### [Use the `image_processing` gem for Active Storage variants. This replaces using `mini_magick` directly](https://github.com/rails/rails/pull/32471)

* ファイルの変換処理にImageMagick(mini_magick gem)を直接使用していたのを、[image_processing](https://github.com/janko-m/image_processing) gemを使用するよう変更
* image_processingはGraphicsMagickもサポートしているのでファイルの変換処理に[libvips](http://jcupitt.github.io/libvips/)(`ruby-vips` gem)も使用出来るようになった
  * vipsを使用したい場合はconfig.active_storage.variant_processorにvipsを指定すればOK
* これにより、mini_magick gemを直接使用するのはdepecateになった
  * 因みに、変換処理でImageMagickのオペレーションを直接指定していたのを、image_processingが提供するメソッド(resize_to_fit、resize_to_fill等々)を使用するよう変更する必要があります
