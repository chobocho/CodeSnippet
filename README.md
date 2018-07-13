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


* HandlerThread
```
mHandlerThread = new HandlerThread("Processing Thread");
mHandlerThread.start();
mHexaHandler = new Handler(mHandlerThread.getLooper()){
	@Override
	public void handleMessage(Message msg){
		Log.d("Hexa", "Handler: There is a event : " + msg.what);
		if (player == null) {
			return;
		}

		if (msg.what == PRESS_KEY) {
			player.onTouchScreen(msg.arg1, msg.arg2);
		}
	}
};
```    
