# Android to WearOS bluetooth communication

> This following example is inspired by the following publication: [website](https://developer.android.com/training/wearables/data/data-layer#cloud)

This example serves to show how to connect and effectively perpetuate a bluetooth link between an Android device and a wearable WearOS device

## Regarding the setup:

1. Open the 'AndroidManifest.xml' file and add the following permissions to both the Android and WearOS devices:

```XML
<uses-permission android:name="android.permission.BLUETOOTH"/>
<uses-permission android:name="android.permission.BLUETOOTH_ADMIN"/>
```

2. Remember to declare the service in the "AndroidManifest.xml" file for the WearOS device

```XML
<service android:name=".DataLayerListenerService">
   <intent-filter>
       <action android:name="com.google.android.gms.wearable.BIND_LISTENER"/>
   </intent-filter>
</service>
```

## Note:

* For both devices you'll have to in order to instantiate end-to-end communication you'll need to know each devices MAC address "00:00:00:00:00:00"