---
title: "Swift Package Manager Commands"
date: 2019-02-28T00:15:41+09:00
draft: false
---

## Init package(Executable)
```
$ swift package init --type executable
```

## Init package(Library)
```
$ swift package init --type library
```

## Build package
```
$ swift build
```

## Test package
```
$ swift test
```

## Run package
```
$ swift run
```

## Define dependent package
### Local
```
.package(path: "../Module"),
```

### Branch
```
.package(url: "https://github.com/<USER>/<REPO>.git", .branch("master")),
```
