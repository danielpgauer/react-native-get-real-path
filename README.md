## react-native-get-real-path

Get real file path from file uri

## Installation (iOS)

Currently No Support

## Installation (Android)

`npm i react-native-get-real-path@https://github.com/danielpgauer/react-native-get-real-path.git --save`

Make alterations to the following files:

* `android/settings.gradle`

```gradle
...
include ':react-native-get-real-path'
project(':react-native-get-real-path').projectDir = new File(settingsDir, '../node_modules/react-native-get-real-path/android')
```

* `android/app/build.gradle`

```gradle
...
dependencies {
    ...
    compile project(':react-native-get-real-path')
}
```


```java
import com.rngrp.RNGRPPackage; // <------- add package

public class MainApplication extends ReactActivity {
   // ...
    @Override
    protected List<ReactPackage> getPackages() {
      return Arrays.<ReactPackage>asList(
        new MainReactPackage(), // <---- add comma
        new RNGRPPackage() // <---------- add package
      );
    }
```

## Example usage (Android only)

```javascript
// require the module
var RNGRP = require('react-native-get-real-path');

RNGRP.getRealPath(fileUri).then(filePath =>
  console.log(filePath)
)
```

