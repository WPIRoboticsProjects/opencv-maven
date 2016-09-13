# opencv-maven
A maven repository for OpenCV artifacts


## Usage
### Gradle dependency

To use this as a maven repository:

```groovy
repositories {
  maven {
    url 'https://github.com/WPIRoboticsProjects/opencv-maven/raw/mvn-repo'
  }
}
```

### Available platforms

Binaries are currently only available for OS X and 64-bit linux. 32-bit linux and 32/64 bit Windows are planned for support as well. The Java library and C++ headers are OS-independent and may be used on any operating system.

Platform-specific artifacts have the platform in the artifact ID. For example, native libraries for 32-bit windows are specified by

```groovy
opencv-natives-windows-x86
```

#### Platform format

Platform formats:

| OS | Architecture | Platform |
|---|---|---|
| Windows | x86 | windows-x86 |
| Windows | x86_64 | windows-x86_64 |
| Mac OS X | x86_64 | osx-x86_64 |
| linux | x86 | linux-x86 | 
| linux | x86_64 | linux-x86_64 |
| linux | arm | linux-arm | 
| linux | armhf | linux-armhf |

## Artifact name and version formats

### Names

Available packages are:

| Name | Description |
|---|---|
| opencv-java | Java library. Does _not_ include JNI |
| opencv-jni | JNI bindings |
| opencv-headers | C++ headers |
| opencv-natives | Compiled native binaries |

### Versions

Currently, only OpenCV 3.1.0 is available
