#### [Allow `ActionDispatch::SystemTestCase.driven_by` to be called with a block to define specific browser capabilities](https://github.com/rails/rails/pull/35081)

* システムテストにbrowser capabilitiesを指定出来るようになった
* driven_byにブロックを指定+そのブロックでbrowser capabilitiesを指定出来る

```ruby
driven_by :selenium, using: :headless_chrome, screen_size: [1400, 1400]  do |driver_option|
  # driver_option.class => Selenium::WebDriver::Chrome::Options
  driver_option.add_emulation(device_name: 'iPhone 6')
end
```
