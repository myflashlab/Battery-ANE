# Battery ANE for Android+iOS
You can know the battery level of the device in your app and also, events will be dispatched when the battery state changes. You will know if the device is charging or not!

[find the latest **asdoc** for this ANE here.](http://myflashlab.github.io/asdoc/com/myflashlab/air/extensions/battery/package-detail.html)

# AIR Usage
For the complete AS3 code usage, see the [demo project here](https://github.com/myflashlab/Battery-ANE/blob/master/AIR/src/Main.as).

```actionscript
import com.myflashlab.air.extensions.battery.*;

// init the ANE and add the listener to know when the battery state changes
Battery.init();
Battery.listener.addEventListener(BatteryEvents.BATTERY_STATE, onBatteryStateChanged);

function onBatteryStateChanged(e:BatteryEvents):void
{
	/*
		BatteryState.FULL
		BatteryState.CHARGING
		BatteryState.DISCHARGING
	*/
	trace("onBatteryStateChanged: " + e.state);
}

// get the current device's battery level
trace("batteryLevel: " + Battery.batteryLevel);
```

# Air .xml manifest
```xml
<!--
Embedding the ANE:
-->
  <extensions>
	<extensionID>com.myflashlab.air.extensions.battery</extensionID>
	
	<!-- dependency ANEs https://github.com/myflashlab/common-dependencies-ANE -->
	<extensionID>com.myflashlab.air.extensions.dependency.overrideAir</extensionID>
  </extensions>
-->
```

# Requirements
* Android API 19+
* iOS SDK 8.0+
* AIR SDK 31.0+

# Tutorials
[How to embed ANEs into **FlashBuilder**, **FlashCC** and **FlashDevelop**](https://www.youtube.com/watch?v=Oubsb_3F3ec&list=PL_mmSjScdnxnSDTMYb1iDX4LemhIJrt1O)  

# Premium Support #
[![Premium Support package](https://www.myflashlabs.com/wp-content/uploads/2016/06/professional-support.jpg)](https://www.myflashlabs.com/product/myflashlabs-support/)
If you are an [active MyFlashLabs club member](https://www.myflashlabs.com/product/myflashlabs-club-membership/), you will have access to our private and secure support ticket system for all our ANEs. Even if you are not a member, you can still receive premium help if you purchase the [premium support package](https://www.myflashlabs.com/product/myflashlabs-support/).