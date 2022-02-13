#### Make

```
git clone https://github.com/xiph/ogg.git
cd ./ogg
# git checkout 3069cc2
cmake -Bbuild -G Xcode .
```

#### Build

```
cd ./build
xcodebuild -scheme ogg -sdk macosx -configuration Release -SKIP_INSTALL=NO
xcodebuild -scheme ogg -sdk iphoneos -configuration Release -SKIP_INSTALL=NO
xcodebuild -scheme ogg -sdk iphonesimulator -configuration Release -SKIP_INSTALL=NO
```

#### Copy

```
cp ./Release/libogg.a ../../libogg.xcframework/macos-arm64/libogg.a
cp ./Release-iphoneos/libogg.a ../../libogg.xcframework/ios-arm64/libogg.a
cp ./Release-iphonesimulator/libogg.a ../../libogg.xcframework/ios-arm64-simulator/libogg.a
```