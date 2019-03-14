## Java Packager

- [J Package](https://www.infoq.com/news/2019/03/jep-343-jpackage)

## Install

```bash

wget \
    -c https://download.java.net/java/early_access/jpackage/archive/17/binaries/openjdk-13-jpackage+17_osx-x64_bin.tar.gz \
    --output-document resource/jdk.tar.gz
gunzip -c .temp/jdk.tar.gz | tar xopf -
```

## Pack

```bash
mvn package
```

## Create Image

```bash
jdk-13.jdk/Contents/Home/bin/jpackage --help
jdk-13.jdk/Contents/Home/bin/jpackage create-image   \
    --input target \
    --main-jar target/Hello-0.1.0.jar \
    --output .output        \
    --name HelloWorld       \
    --main-class wk.Program
```

## Execute

```bash
.output/HelloWorld.app/Contents/MacOS/HelloWorld
```