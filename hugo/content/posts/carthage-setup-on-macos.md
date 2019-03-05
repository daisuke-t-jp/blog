---
title: "Carthage Setup on macOS"
date: 2019-03-06T06:34:46+09:00
draft: false
---

## Reference
- [Carthage](https://github.com/Carthage/Carthage)

## 1. Install Carthage
```
$ brew update
$ brew install carthage
```


## 2. Make Cartfile file
Case of use *https://github.com/tadija/AEXML* on iOS platform.

```
github "tadija/AEXML"
```

or

```
git "https://github.com/tadija/AEXML.git"
```


## 3. Update *.gitignore*
```
/Carthage # Adding
```


## 4. Build Carthage
```
carthage update --platform iOS 
```
If build was succeed, There is framework in "Carthage/Build/iOS/".


## 5. Add Carthage framework to Xcode project
You Carthage framework add to target *BuildPhase*'s *Link Binary With Libraries*.  
  
Next,  
You add new *Run Script Phase* in *BuildPhase*.  
```
/usr/local/bin/carthage copy-frameworks
```
  
and,  
File add to *Input Files*. 
```
$(SRCROOT)/Carthage/Build/iOS/AEXML.framework
```