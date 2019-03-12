---
layout: single
title: "iOS animations using Lottie"
date: 2019-03-03
categories: posts
classes: wide
tags: ios swift lottie animations bodymovin adobe-after-effects
---

[Lottie](https://github.com/airbnb/lottie-ios) is a mobile library for Android and iOS that parses Adobe After Effects animations exported as json with [bodymovin](https://github.com/bodymovin/bodymovin) and renders the vector animations natively on mobile and through React Native!

Animations, especially complex animations can take a long to implement by hand when using Core Animation or even just simple UIView animations. Using Lottie can save you a lot of time a manual effort. Getting started is really easy, so let's get started!

## Setting up Lottie

The easiest way to install and use Lottie is by using [CocoaPods](https://cocoapods.org). We start by creating a Podfile in the same directory as our Xcode project and add the lottie-ios pod:

```bash
target 'LottieAnimations' do
  use_frameworks!
  pod 'lottie-ios'
end
```

With the `lottie-ios` pod added we simply need to do install the pod:

```bash
pod install
```

CocoaPods will create a new Xcode Workspace which we will use instead of the previous Xcode project.

## Working with LOTAnimationView

Animations in Lottie is exported to JSON from Adobe After Effect sand can be loaded from your app's bundle or from a URL. In the example below we are loading a file from the bundle called "loading.json":

```swift
let loadingAnimation = LOTAnimationView(name: "loading")
    loadingAnimation.autoresizingMask = [.flexibleHeight, .flexibleWidth]
    loadingAnimation.contentMode = .scaleAspectFit
    loadingAnimation.frame = view.bounds

    view.addSubview(loadingAnimation)

    loadingAnimation.loopAnimation = true
    loadingAnimation.play(fromProgress: 0,
                        toProgress: 0.76,
                        withCompletion: nil)
```

## Lottie Files

- download pre-designed files