# Code snippet


## History
Date      |Description                     |Memo
----------|--------------------------------|-----
2018.06.28|Release first version           |

  
* 회전방지

```
<activity
   android:screenOrientation="portrait">
</activity>
```

  
* JAVA 1.8 사용

```
build.gradle(Module:app)
android {
    // ...
    compileOptions {
        sourceCompatibility JavaVersion.VERSION_1_8
        targetCompatibility JavaVersion.VERSION_1_8
    }
}
```
