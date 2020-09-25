Android TV Plugin for Cordova
==============================

Cordova plugin to add support for Android TV to your project's AndroidManifest.xml. This fork has following changes:

- Has been updated to work with cordova > 8
- Standardised cordova plugin name
- Removed the JavaScript hook that modifies AndroidManifest.xml and instead instruct to use <edit-config> feature inside the app config.xml, this way the isGame property is configurable
- Accounts for the new location of AndroidManifest.xml at `platforms/android/app/src/main/AndroidManifest.xml`

Install
-------

`cordova plugin add https://github.com/playsignage/cordova-plugin-android-tv`

To avoid edit-config conflicts, add following lines to your cordova `config.xml` inside `<platform name="android">` tag:

```
<edit-config comment="" file="app/src/main/AndroidManifest.xml" mode="merge" target="/manifest/application">
  <application android:banner="@drawable/banner" android:isGame="false" />
</edit-config>
```

AndroidTV requires a banner image that is 320x180 png file, create it and add to your project. You will also need to include the banner file in the Android build, add following line to your `config.xml` inside `<platform name="android">` tag:

`<resource-file src="path/to/your/banner.png" target="app/src/main/res/drawable/banner.png" />`

Source
-------------
https://github.com/playsignage/cordova-plugin-android-tv

License
-------

This has been released under MIT license; see LICENSE for details.

Forked from
-----------
https://github.com/hughisaacs2/Cordova-Android-TV-Plugin
