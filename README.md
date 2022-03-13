# Android-Sanitization

Now a days world is moving towards digital and it has some pros and cons too, like each and every day we put tons of our personal data online willingly or unwillingly and it is getting upload viva our devices like smart phones, tablet and computers etc.

In this our focus is more will be on Mobile Phones. 

We love to use the products which come's free and cheap with loaded lots features and functionality thats makes our life more easy simple.

    "If you do not pay for a service, you are the product they sell. so it ever has been.(Tom Webster)"


******************************************************************************************************************************************************************

Android sanitization without custom ROMs, unlocked boot-loaders, or rooted devices.

You may be surprised how easily you can make any Android device more private and secure. 

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
    
    Disable a package for primary user: adb shell pm disable-user --user 0 com.google.android.youtube 
    
    Reenable a package for primary user: adb shell pm enable com.google.android.youtube 
    
Google services and apps examples: 

![After_Installing_Youtube_and_List](https://user-images.githubusercontent.com/53815408/158075915-37e9087e-7185-4c9a-97a3-e3e68100c864.png)


    Simple Tools: https://www.simplemobiletools.com 

Extract and Install Example: adb shell pm path com.android.gallery3d adb pull /product/app/Gallery2/Gallery2.apk adb install --user 0 Gallery2.apk 

Secondary Profiles: adb shell pm list packages --user 10 adb shell pm list package --user 10 | grep 'google' 

adb install --user 10 adb shell pm uninstall -k --user 10 com.google.android.youtube 

adb shell cmd package install-existing --user 10 com.google.android.youtube 

adb shell pm disable-user --user 10 com.google.android.youtube 

adb shell pm enable --user 10 com.google.android.youtube 

******************************************************************************************************************************************************************
