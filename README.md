swift build instructions for the impatient
------------------------------------------

install dependencies: `cmake` and `ninja`

optional dependency for generating documentation: `sphinx`

copy and paste this block to a terminal:

```
git clone --depth=1 https://github.com/apple/swift.git swift
git clone --depth=1 https://github.com/apple/swift-llvm.git llvm
git clone --depth=1 https://github.com/apple/swift-clang.git clang
git clone --depth=1 https://github.com/apple/swift-lldb.git lldb
git clone --depth=1 https://github.com/apple/swift-cmark.git cmark
git clone --depth=1 https://github.com/apple/swift-llbuild.git llbuild
git clone --depth=1 https://github.com/apple/swift-package-manager.git swiftpm
git clone --depth=1 https://github.com/apple/swift-corelibs-xctest.git
git clone --depth=1 https://github.com/apple/swift-corelibs-foundation.git
```

build llvm, clang, swift and swift standard library:

```
./swift/utils/build-script
```

create xcode project capable of building swift:

```
./swift/utils/build-script -x -R
```

create xcode project for editing swift sources:

```
./swift/utils/build-script -X -R
```

more options of the build script can be found in its help text:

https://github.com/apple/swift/blob/master/utils/build-script#L172
