---
title: "Library register to CocoaPods"
date: 2019-02-25T11:39:09+09:00
draft: false
---

## First time
1. Create podspec
  - `pod spec create MyLib`

1. Edit podspec
  - Do not include *info.plist* in *source_files*.

1. Check Lint
  - `$ pod lib lint`

1. Register acount to CocoaPods
  - `$ pod trunk register mail@addr 'Account name'`

1. Create Tag
  - `$ git tag 1.0.1`
  - `$ git push origin 1.0.1`

1. Push
  - `$ pod trunk push MyLib.podspec`


## on Update

1. Check Lint
  - `$ pod lib lint`

1. Create Tag
  - `$ git tag 1.0.2`
  - `$ git push origin 1.0.2`

1. Push
  - `$ pod trunk push MyLib.podspec`

