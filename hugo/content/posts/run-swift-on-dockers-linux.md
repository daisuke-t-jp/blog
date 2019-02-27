---
title: "Run Swift on Docker's Linux"
date: 2019-02-27T23:33:53+09:00
draft: false
---

## References
- [Download Swift](https://swift.org/download/#using-downloads)
- [Swift](https://github.com/apple/swift#getting-started)


## Step
### Docker
1. Install Docker
```
$ brew cask install docker
```

1. Get Ubuntu image
```
$ docker pull ubuntu
```

1. Create container of Ubuntu
```
$ docker run --privileged -it ubuntu /bin/bash
```

1. Start container
```
$ docker start ID
```

1. Attach container
```
$ docker attach ID
```
 
 
### Ubuntu
1.  Update packages
```
# apt update
```

1. Install packages that dependent Swift
```
# apt-get install git cmake ninja-build clang python uuid-dev libicu-dev icu-devtools libbsd-dev libedit-dev libxml2-dev libsqlite3-dev swig libpython-dev libncurses5-dev pkg-config libblocksruntime-dev libcurl4-openssl-dev systemtap-sdt-dev tzdata rsync
```

1. Download Swift
```
# cd /opt/
# apt-get install wget
# wget https://swift.org/builds/swift-4.2-release/ubuntu1804/swift-4.2-RELEASE/swift-4.2-RELEASE-ubuntu18.04.tar.gz
```

1. Unzip
```
# tar xvfz swift-4.2-RELEASE-ubuntu18.04.tar.gz
# mv swift-4.2-RELEASE-ubuntu18.04 swift
```

1. Set path
```
# export PATH=/opt/swift/usr/bin:"${PATH}"
```

1. Test
```
# swift -version
Swift version 4.2 (swift-4.2-RELEASE)
Target: x86_64-unknown-linux-gnu
```


## Memo
Copy host's file to container
```
$ docker cp file.cnf <ID>:/etc/file.cnf
$ docker cp dir <ID>:/etc/dir
```
