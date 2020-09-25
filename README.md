Android TV Plugin for Cordova
==============================

Cordova plugin to add support for Android TV to your project's AndroidManifest.xml. This fork has following changes:

- Has been updated to work with cordova > 8
- Standardised cordova plugin name
- Uses newer cordova feature `edit-config` instead of a JavaScript hook modifying AndoridManifest directly
- Sets `android:isGame=false` declaration in the manifest instead of `true`
- Accounts for the new location of AndroidManifest.xml at `platforms/android/app/src/main/AndroidManifest.xml`

Install
-------

`cordova plugin add https://github.com/playsignage/cordova-plugin-android-tv`

AndroidTV requires a banner image that is 320x180 png file. You will need to add following line to your cordova config.xml that will copy the banner file, else the app won't compile.

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
