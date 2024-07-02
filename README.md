![Maven build](https://github.com/abstractfoundry/lumicube-daemon/actions/workflows/maven-package.yml/badge.svg)

# lumicube-daemon

LumiCube service for the Raspberry Pi.

## Building

You can build this using Maven (either from the command-line, or e.g. using NetBeans).

The resulting .zip (containing all the JAR files) can either be extracted and run directly, or packaged with a JVM into an AppImage using build.sh.

Note: This last step requires Docker (and therefore also root permissions).

Grafster - This also only seems to work on x86 Linux, but the resulting AppImage works OK on Raspberry Pi

## Maven

The steps to build an image (example Daemon-1.10-SNAPSHOT) are:

```
sudo apt install maven
mvn package
cp target/Daemon-1.10-SNAPSHOT.zip .
sudo ./build.sh Daemon-1.10-SNAPSHOT
```