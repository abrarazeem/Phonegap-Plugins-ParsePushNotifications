Phonegap-Plugins-ParsePushNotifications
=======================================
> receive push message from Parse.com in your phonegap app

Auto Installation:
=============
phonegap plugin add https://github.com/abrarazeem/Phonegap-Plugins-ParsePushNotifications/

cordova plugin add https://github.com/abrarazeem/Phonegap-Plugins-ParsePushNotifications/


Usage:
=======

To use this plugin first register device with parse.com using following in your device ready or if you are using ionic framework use it inside $ionicPlatform.ready function like this

```javascript
window.parsePush.register({appId:"parse.com applicaion Id",clientKey:"parse.com clientkey"},
      function(success){
        alert("Device successfully register at parse.com ");
      },
      function(error){
        alert("Error registering device at parse.com");
      }
      
);
```

Handling Notifaction and Notifaction Data:
==========================================
```javascript
window.parsePush.ontrigger = function(appState,data){
  alert(JSON.stringify(data));  
}
```

###Android Only
Application Crashing in background due to parse receiver application so,
Register Parse Application in AndroidManifest.xml as application tag android:name=""
just like below
```xml
<application android:hardwareAccelerated="true" android:icon="@drawable/icon" android:label="@string/app_name" android:name="com.stratogos.cordova.parsePushNotifications.ParseApplication" android:supportsRtl="true">
```




