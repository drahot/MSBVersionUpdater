[ ![Download](https://api.bintray.com/packages/misyobun/maven/MSBVersionUpdater/images/download.svg) ](https://bintray.com/misyobun/maven/MSBVersionUpdater/_latestVersion)

### This library is based on kazu0620’s SRGVersionUpdater which is iOS library. (https://github.com/kazu0620/SRGVersionUpdater)

### Difference between SRGVersionUpdater
if user cancel latest update, `MSBVersionUpdater` doesn't show again alert dialog unless required_version becomes latest.(When type is `optional`)


## Usage

### 1. Upload a JSON file below
```
{"required_version":"2.7.6","type":"force","update_url":"https://play.google.com/store/apps/details?id=[APP_PACKAGE_NAME]”}
```

| key | define |
| --: | --- | 
| required_version | The version of latest client application. | 
| type | The type of update, “force” or “optional”. |
| update_url | Google Play  URL of your app. |

### 2. Download MSBVersionUpdater

#### build.gradle

```
repositories {
        jcenter()
        maven {
            url 'http://misyobun.github.io/MSBVersionUpdater/repository/'
        }
    }
```

```
dependencies {
    compile 'jp.co.misyobun.lib.versionupdater:msb-version-updater:0.0.6'
}
```