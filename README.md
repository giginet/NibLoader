# NibLoaderKit 

[![Build Status](https://travis-ci.org/giginet/NibLoaderKit.svg?branch=master)](https://travis-ci.org/giginet/NibLoaderKit) 
[![codecov](https://codecov.io/gh/giginet/NibLoaderKit/branch/master/graph/badge.svg)](https://codecov.io/gh/giginet/NibLoaderKit) 
[![CocoaPods Compatible](https://img.shields.io/cocoapods/v/NibLoaderKit.svg)](https://img.shields.io/cocoapods/v/NibLoaderKit.svg)
[![Carthage compatible](https://img.shields.io/badge/Carthage-compatible-4BC51D.svg?style=flat)](https://github.com/Carthage/Carthage) 
[![Platform](https://img.shields.io/cocoapods/p/NibLoaderKit.svg?style=flat)](http://cocoadocs.org/docsets/NibLoaderKit)

This is a micro utility to create UIView/NSView from nib files.

# Usage

## 1. Declare CustomView class

```swift
class CustomView: UIView { }
```

## 2. Place `CustomView.xib`

- `xib` must contains just one top level view.

## 3. Set custom class

- Set custom class of the top level view to `CustomView`.

![](https://raw.githubusercontent.com/giginet/NibLoaderKit/master/Documentation/Images/custom_view.png)

## 4. Load from code

```swift
let customView: CustomView = CustomView.view(withOwner: self)
```

`CustomView.xib` will be loaded and generated the view.

You can also pass the nibName and bundle.

```swift
let customView: CustomView = UIView.view(
    fromNibNamed: "MyCustomView", 
    owner: self, 
    bundle: NSBundle(forClass: self.dynamicType)
)
```

# Installation

## Carthage

```
github "giginet/NibLoaderKit"
```

## CocoaPods

```ruby
use_frameworks!

pod 'giginet/NibLoaderKit'
```

# Requirements

- >= iOS 8
- >= macOS 10.10
- >= tvOS 9
- Swift 2.2

## LICENSE

MIT License
