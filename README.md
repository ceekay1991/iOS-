## iOS-开发笔记
## 1、json和pilst转换
    json to plist:
    plutil -convert xml1 data.json -o data.plist
    plist to json: 
    plutil -convert json data.plist -o data.json
## 2、dyld: Library not loaded: @rpath
    dyld: Library not loaded: @rpath/UnrarKit.framework/UnrarKit
    Referenced from:
    Reason: image not found
  
  #解决方案 
  * BuildSettings  -- Linking Mach-O Type 修改为 Static Library
  * 重新编译
  
## 3、Framework 真机模拟器合并
        lipo -create Release-iphoneos/UnrarKit.framework/UnrarKit Release-iphonesimulator/UnrarKit.framework/UnrarKit -o Release-iphoneos/UnrarKit.framework/UnrarKit

