# Android-Sanitization

Nowadays the world is moving towards digital and it has some pros and cons too, like every day we put tons of our data online willingly or unwillingly and it is getting uploaded via our devices like smartphones, tablets, computers, etc.

In this, our focus is more will be on Android Mobile Phones.

    "If you do not pay for a service, you are the product they sell. so it ever has been.(Tom Webster)"


******************************************************************************************************************************************************************

Android developed by a consortium of developers known as the Open Handset Alliance and commercially sponsored by Google, 
every android device has running Google android OS comes free with devices it consumes lots of google services.

Google collects tons of our data with or without our concern with the help of devices and OS.

I am more concerned about my privacy and data than anything, that's why I tried to get rid of Google's Services which comes by default with stock android devices and along with Bloatware, I don't like this free stuff that much because they use to suck our information at every stage while we are using that Android OS and Android devices.

I do not use any mobile devices browser for internet browsing because lots of other apps can have access to that data.

The data collected can include:
your location, what device you're using, which advertisements you've clicked on, and many more.

Apple does not allow us to have custom ROM and other stuff.

Over android, we can achieve that by having custom ROM with the help of GrapheneOS and many more, but if not want to mess 
with our new stock phone is worth 20k to 70k, we can also achieve that just by getting rid of stock programs and 
bloatware which collects lots of our data even without concern.

Ungoogled Rom to get rid of google services it has done to protect our privacy.

DISCLAIMER
   
    I take no responsibility if you replicate any of my steps and screw up your devices, I am not telling you to do what I am telling is what I did.

If you removed too much stuff and the device stopped working then boot the device in recovery mode and reset it will become good as new.

Bloatware "(potentially unwanted programs- PUP) or we can say pre-installed software on the device" application which we cannot uninstall it from the devices we stop it just by doing force quit and if the phone get restart 

Manually or due to software updates may start automatically right after the restart.

Android sanitization without custom ROMs unlocked boot-loaders or rooted devices.

You may be surprised how easily you can make any Android device more private and secure.

I want to remove that applications via Android Debug Bridge (ADB) is a versatile command-line tool that lets you 
communicate with a device. The ADB command facilitates a variety of device actions, such as installing and debugging apps, and provides access to a Unix shell that you can use to run a variety of commands on a device.)

ADB Installation:
    
    Linux: sudo apt update && sudo apt install android-tools-adb android-tools-fastboot

    Mac: $ brew install android-platform-tools 

    Windows: C:/ choco install adb 

USB Debugging: Settings > About Phone > Build Number (x7) Settings > System > Advanced > Developer Options > Enable > USB Debugging > Enable ADB 

    Test: adb devices 

    List all packages: adb shell pm list packages --user 0
    
    List specific packages: adb shell pm list package --user 0 | grep 'google'
    
    Uninstall a package for primary user: adb shell pm uninstall -k --user 0 com.google.android.youtube 
    
    Reinstall a package for primary user: adb shell cmd package install-existing com.google.android.youtube 
      
The applications don't vanish completely because OS itself has those applications in it and I want to reinstall it I can do that.

But it doesn't not visible in your profile, you can't execute it in your profile and it can't run in the background doing various things and transmitting the data without it being present.

Google services and apps examples:

    Google Services: com.google.android.gsf
    Google Play: com.google.android.gms
    Google Store: com.android.vending 
    Google Carriers: com.google.android.ims 
    Google Speech: com.google.android.tts 
    Google Telemetry: com.google.mainline.telemetry 
    Google Photos: com.google.android.apps.photos 
    Google Maps: com.google.android.apps.maps 
    Google Calendar: com.google.android.calendar 
    Google Contacts: com.google.android.contacts 
    Google Messages: com.google.android.apps.messaging 
    Google Dialer: com.google.android.dialer 
    Google Keyboard: com.google.android.inputmethod.latin 
    Gmail: com.google.android.gm 
    Youtube: com.google.android.youtube 

By doing all we can achieve 95% sanitization because Facebook is still there but it is not running on the devices and we cannot accidentally click it and it does not send data to Facebook.
    
![Packages_list](https://user-images.githubusercontent.com/53815408/158075997-ce191268-8449-4189-a429-2d6ffaa5fb83.png)
 
![Packages_1](https://user-images.githubusercontent.com/53815408/158076017-d354f492-502a-4363-adca-3146b700640a.png)

    
    Google services and apps examples:
    
![Google_Package_List](https://user-images.githubusercontent.com/53815408/158076064-4461a582-d090-4f82-897a-6cb3442ef62f.png)

    After Uninstalling : com.google.android.youtube 
    
![Youtube_Uninstall_and_List](https://user-images.githubusercontent.com/53815408/158076117-c514e65d-fe41-4065-8562-7922ed36fb6e.png)

    After installing : com.google.android.youtube 

![After_Installing_Youtube_and_List](https://user-images.githubusercontent.com/53815408/158075915-37e9087e-7185-4c9a-97a3-e3e68100c864.png)

If we do not want to remove we can disable it by just executing the below commands.

But it gets enabled automatically sometimes due to some bigger update like OS update from 11 to 12 which is a bigger update and it may enable that applications.

Removing it than disabling it is a much bigger step.

So here we are hiding the applications we are not fully removing, we are killing them at the point they don't run and we are eliminating connections that applications were made if they are installed.

    Disable a package for primary user: adb shell pm disable-user --user 0 com.google.android.youtube 
    
    Reenable a package for primary user: adb shell pm enable com.google.android.youtube 

If you remove the default gallery using the below commands you can install a new gallery application from Legion OS.

    Extract and Install Example: adb shell pm path com.android.gallery3d adb pull /product/app/Gallery2/Gallery2.apk adb install --user 0 Gallery2.apk 

Secondary Profiles:

Android now has a built-in feature that allows you to set up multiple user accounts, which means you can set up a secondary user profile that shares absolutely no data with your own. It's a great way to maintain your privacy.

It is for a secondary profile.

    Secondary Profiles: adb shell pm list packages --user 10 adb shell pm list package --user 10 | grep 'google' 

    adb install --user 10 adb shell pm uninstall -k --user 10 com.google.android.youtube 

    adb shell cmd package install-existing --user 10 com.google.android.youtube 

    adb shell pm disable-user --user 10 com.google.android.youtube 

    adb shell pm enable --user 10 com.google.android.youtube 

******************************************************************************************************************************************************************

We can replace the apps with other apps that provide more privacy and security.

    https://www.simplemobiletools.com/

![simplemobiletools](https://user-images.githubusercontent.com/53815408/158333274-7a2aa192-2b16-40ce-996c-0aea3a6110c9.png)

Other tools links:

    https://privacy.com/
    
![privacy](https://user-images.githubusercontent.com/53815408/158334364-1e152671-1a8e-467f-b354-4c2c2c2a1e7a.png)

    https://grapheneos.org/
    
![grapheneos](https://user-images.githubusercontent.com/53815408/158334417-22e812d4-abb1-4dee-9438-4379871a4333.png)

    https://blokada.org/
    
![blokada](https://user-images.githubusercontent.com/53815408/158334462-5a11a4a2-8648-4a79-b6db-8d5848f81732.png)

    https://blog.legionos.org/
    
![legionos](https://user-images.githubusercontent.com/53815408/158334514-f6a48815-1c9c-4bd8-8bfd-92a571081e17.png)

    Thank you.
