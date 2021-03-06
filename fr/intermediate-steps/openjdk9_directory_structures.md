# Structure des répertoires d'OpenJDK 9

Observez la [structure des répertoires](https://gist.github.com/neomatrix369/5be36b5af8768353eca4) de divers projets dans OpenJDK.

**répertoire build**
```
$ tree -fL 2 build
```
```
build
└── build/linux-x86_64-normal-server-release
    ├── build/linux-x86_64-normal-server-release/bootcycle-spec.gmk
    ├── build/linux-x86_64-normal-server-release/build.log
    ├── build/linux-x86_64-normal-server-release/build.log.old
    ├── build/linux-x86_64-normal-server-release/buildtools
    ├── build/linux-x86_64-normal-server-release/compare.sh
    ├── build/linux-x86_64-normal-server-release/config.h
    ├── build/linux-x86_64-normal-server-release/config.log
    ├── build/linux-x86_64-normal-server-release/config.status
    ├── build/linux-x86_64-normal-server-release/hotspot
    ├── build/linux-x86_64-normal-server-release/hotspot-spec.gmk
    ├── build/linux-x86_64-normal-server-release/images
    ├── build/linux-x86_64-normal-server-release/jdk
    ├── build/linux-x86_64-normal-server-release/Makefile
    ├── build/linux-x86_64-normal-server-release/make-support
    ├── build/linux-x86_64-normal-server-release/nashorn
    ├── build/linux-x86_64-normal-server-release/source_tips
    ├── build/linux-x86_64-normal-server-release/spec.gmk
    ├── build/linux-x86_64-normal-server-release/spec.sh
    └── build/linux-x86_64-normal-server-release/support
```
---

**répertoire build/[nom-en-fonction-de-l-os]/images**
<br/>
*[nom-en-fonction-de-l-os] - peut être ```linux....``` ou ```macosx...```  ```windows...```.

``` 
$ tree -fL 2 images
```
```
images
├── images/demo
│   ├── images/demo/applets
│   ├── images/demo/jfc
│   ├── images/demo/jvmti
│   ├── images/demo/management
│   ├── images/demo/nbproject
│   ├── images/demo/README
│   └── images/demo/scripting
├── images/jdk
│   ├── images/jdk/ASSEMBLY_EXCEPTION
│   ├── images/jdk/bin
│   ├── images/jdk/conf
│   ├── images/jdk/demo
│   ├── images/jdk/include
│   ├── images/jdk/jrt-fs.jar
│   ├── images/jdk/lib
│   ├── images/jdk/LICENSE
│   ├── images/jdk/man
│   ├── images/jdk/release
│   ├── images/jdk/sample
│   ├── images/jdk/src.zip
│   └── images/jdk/THIRD_PARTY_README
├── images/_jdk-jimages-create.marker
├── images/jdk-sorted-modules
├── images/jre
│   ├── images/jre/ASSEMBLY_EXCEPTION
│   ├── images/jre/bin
│   ├── images/jre/conf
│   ├── images/jre/lib
│   ├── images/jre/LICENSE
│   ├── images/jre/man
│   ├── images/jre/release
│   └── images/jre/THIRD_PARTY_README
├── images/_jre-jimages-create.marker
├── images/jre-sorted-modules
├── images/sample
│   ├── images/sample/annotations
│   ├── images/sample/forkjoin
│   ├── images/sample/jmx
│   ├── images/sample/lambda
│   ├── images/sample/nbproject
│   ├── images/sample/nio
│   ├── images/sample/README
│   ├── images/sample/scripting
│   └── images/sample/try-with-resources
└── images/sec-bin.zip
```
---
**répertoire jdk/src**
```
$ cd sources/jdk9/jdk/src
```
or
```
$ cd dev/jdk9_dev/jdk/src
```

```
$ tree -dflL 5 java.base/share/classes/java/util
 
java.base/share/classes/java/util
├── java.base/share/classes/java/util/concurrent
│   ├── java.base/share/classes/java/util/concurrent/atomic
│   └── java.base/share/classes/java/util/concurrent/locks
├── java.base/share/classes/java/util/function
├── java.base/share/classes/java/util/jar
├── java.base/share/classes/java/util/regex
├── java.base/share/classes/java/util/spi
├── java.base/share/classes/java/util/stream
└── java.base/share/classes/java/util/zip
```
---

**répertoire java.base**
```
$ tree -fldL 5 java.base  | less

$ tree -dflL 5 java.base/share/classes/java  
 
$ tree -dflL 5 java.base/share/classes/java  
```

---

**package java.io**
```
$  tree -flL 5 java.base/share/classes/java/io
$  tree -dflL 5 java.base/share/classes/java/io
│   ├── java.base/share/classes/java/io
```

---

**package java.lang** 
```
$  tree -dflL 5 java.base/share/classes/java/lang
│   ├── java.base/share/classes/java/lang
.
.
.
```
---

**package java.nio**
```
$  tree -dflL 5 java.base/share/classes/java/nio
│   ├── java.base/share/classes/java/nio
```
---

**package java.text**
```
$  tree -dflL 5 java.base/share/classes/java/text
│   ├── java.base/share/classes/java/text
.
```
---

**package java.time**
```
$  tree -dflL 5 java.base/share/classes/java/time
│   ├── java.base/share/classes/java/time
.
.
.
```
---

**package java.util**
```
$ tree -dflL 5 java.base/share/classes/java/util
│   └── java.base/share/classes/java/util
```
---

**répertoire (sources/jdk9/jdk/src) ou (dev/jdk9_dev/jdk/src)**
```
$ tree -dflL 5 java.base/share/classes/java/util
 
java.base/share/classes/java/util
├── java.base/share/classes/java/util/concurrent
│   ├── java.base/share/classes/java/util/concurrent/atomic
│   └── java.base/share/classes/java/util/concurrent/locks
├── java.base/share/classes/java/util/function
├── java.base/share/classes/java/util/jar
├── java.base/share/classes/java/util/regex
├── java.base/share/classes/java/util/spi
├── java.base/share/classes/java/util/stream
└── java.base/share/classes/java/util/zip
```
---

**répertoire (sources/jdk9/jdk/src) ou (dev/jdk9_dev/jdk/src)**
```
$ tree -fl | grep "/Socket." 
```
 
**OpenJDK 9 - jdk9 (sources/jdk9/jdk/src) ou (dev/jdk9_dev/jdk/src)**
```
$ ls java.sql/share/classes/java/sql
```