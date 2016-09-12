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

#### Platform format

Platform formats (used when specifying versions of native artifacts):

| OS | Architecture | Platform |
|---|---|---|
| Windows | x86 | win32 |
| Windows | x86_64 | win64 |
| Mac OS X | x86_64 | osx |
| linux | x86 | linux32 | 
| linux | x86_64 | linux64 |

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

Currently, only OpenCV 3.1.0 is available. Additionally, native packages have the platform before the OpenCV version in the maven version identifier.

| Artifact | Version format |
|---|---|
| opencv-java | ${opencv-version} | 
| opencv-jni | ${platform}-${opencv-version} |
| opencv-headers | ${opencv-version} |
| opencv-natives | ${platform}-${opencv-version} |
