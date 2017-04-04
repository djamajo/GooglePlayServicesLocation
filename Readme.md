Overview
--------

The following example illustrates how to use the Google Play services for getting the Location position updates.


Setting up for using google services
------------------------------------

* Edit ```build.gradle```
```
        // This compile was added for using the google play services
        compile 'com.google.android.gms:play-services:10.2.1'
```


* Add the required permissions into the ```AndroidManifiest.xml```   

```xml
    <uses-permission android:name="android.permission.ACCESS_FINE_LOCATION"/>
```

or  

```xml
     <uses-permission android:name="android.permission.ACCESS_COARSE_LOCATION" />
```


* Add the following meta information within the ```AndroidManifiest.xml``` within the ```<application ....> </application>```  section

```xml
    <meta-data android:name="com.google.android.gms.version"  
                android:value="@integer/google_play_services_version"/>
```


API 23 (android 6.0) or higher consideration
--------------------------------------------

If the target SDK for you application is 23 or higher the permission have to accepted by the user. Therefore it has to be implemented the verification if the ```ndroid.permission.ACCESS_FINE_LOCATION``` was granted.  
In case the the permission was not granted it has to be requested during the execution time.  

https://developer.android.com/training/permissions/requesting.html


