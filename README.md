# SwiftDebouncer
A simple Swift Library for a Debouncer class to delay function calls

[![Badge w/ Version](https://cocoapod-badges.herokuapp.com/v/SwiftDebouncer/badge.png)](https://cocoadocs.org/docsets/SwiftDebouncer)
[![Language](https://img.shields.io/badge/language-swift%204-1b7cb9.svg)](https://img.shields.io/badge/language-swift%204-1b7cb9.svg)
[![iOS](https://img.shields.io/badge/iOS-8.0%2B-1b7cb9.svg)](https://img.shields.io/badge/iOS-9.0%2B-1b7cb9.svg)
[![GitHub license](https://img.shields.io/badge/license-MIT-blue.svg)](https://github.com/xremix/SwiftDebouncer/blob/master/LICENSE)

## Description
A Swift Library for a debounce function, similar to the JavaScript debounce.
The Debouncer will delay a function call, and every time it's getting called it will delay the preceding call until the delay time is over.

## Getting started

Usage is as simple as the following code:

```SWIFT
let d = Debouncer(delay: 10)
d.callback = {
// your code here
}

d.call()
```

You can pass a parameter `delay` (in `ms` of type TimerInterval) and optional an callback function.

Make sure to check out the [Unit Tests](https://github.com/xremix/SwiftDebouncer/tree/master/SwiftDebouncerTests) for further code samples.

###  Properties

- `callback` Callback that is getting called when the timer fires
- `delay` Delay Time in ms
- `fireDate` Next Date when the Debouncer will fire

### Functions
- `call` Call debouncer to start the callback after the delayed time. Multiple calls will ignore the older calls and overwrite the firing time


## Installation

### CocoaPods

You can install [the library](https://cocoapods.org/pods/SwiftDebouncer) to your project by using [CocoaPods](https://cocoapods.org). Add the following code to your `Podfile`:
```
platform :ios, '8.0'
use_frameworks!

target 'MyApp' do
pod 'SwiftDebouncer'
end
```

### Git Submodule

You can add the project as a git `submodule`. Simply drag the `SwiftGS1Barcode.xcodeproj` file into your Xcode project.
**Don't forget to add the framework in your application target**

### Manually

Just copy and paste the [`Debouncer.swift`](https://github.com/xremix/SwiftDebouncer/blob/master/SwiftDebouncer/Debouncer.swift) file into your project.



![Analytics](https://ga-beacon.appspot.com/UA-40522413-9/SwiftDebouncer/readme?pixel)

## About this

- This was developed to not copy over and over the same classes due different projects
- Test coverage should be pretty good - was developed using TDD
- Oriented on [this](https://www.appcoda.com/cocoapods-making-guide/) article on how to deploy this on CocoaPods
- Contributors are very welcome
