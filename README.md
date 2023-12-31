By: Spidy123222
# Welcome to the List of Guides for Debugging/JIT on iOS/iPadOS 13+
This page has a list of guides for debugging and activating JIT on iOS/iPadOS 13+. 

*Note: Some of these methods can work on lower versions with less convenience by having to be tethered to a compter during the whole time, so it is recommended to use these on iOS 13 and above.*

**NOTICE: Currently All Below tutorials use a computer of some sort! However there is a few that only need a pair file and that's all rest of it is no computer.**

## FAQ

**Q: Why would I need to use these?**

A: You would use one of these tutorials to debug an app on the go, use JIT for emulators or other things without being fully tethered to a computer on a developer liscenced app.

**Q: What is JIT?**

A: Having JIT is required for most emulators and programs that Re-compile code at runtime to run on the device. This can be useful for speeding up writing, execution and reading for emulating a game or doing things in web-browsers like in Safari because it can run faster because its not being interpited in real time which can be a big task for the cpu.

**Q: What About Earlier Versions of iOS/iPadOS that has native JIT support? Why doesn't current versions have it?**

A: iOS/iPadOS versions 14.4 and above are naturally incompatible with non-jailbroken versions of iOS/iPadOS due to the removal of an exploit that allowed an app to debug itself, and therefore enabling JIT. These apps can use these tutorials/programs below to do it on devices running iOS/iPadOS 14.4 and above.

**Q: What Tricks have been used in the past to activate JIT and why were they removed?**

A: A few tricks were used and they were all removed because they were bugs and that could lead to security vulnerabilities.

One notible one was that developers used the `ptrace()` trick used for debugging and activating JIT. This allowed a developer to activate a debug from the app (ppsspp used this trick early on). This trick had a side effect that if you force close the app you would experience buggy behavior and the exploit was not able to use the app again until you restarted your iDevice. This trick was used on iOS/iPadOS 13 versions and was patched on iOS/iPadOS 14

Another exploit used was using sandbox escapes, like the ``phycicpaper`` exploit for iOS/iPadOS 13.4.1 and below. This allowed kernel access to features like Safari's jit or extended memory access which DolphiniOS took advantage of for its first non-jailbroken version of the app.

For a brief moment on iOS/iPadOS 14.2-14.3 there was a bug to enable a debugger which allowed developers to enable JIT on apps similar to the ``ptrace()`` trick, but did not have the restrictions or any command related to it. All that had to be program the app with the ``get-task-allow`` functionality. This trick was utilized in a way where apps could natively support JIT without much extra work or tricks for exiting apps to end the task. The only problem was this only supported devices with an A12 bionic chip and above, which excluded devices with A11 bionic chips and below to use this exploit.

Not long after, a method was found to enable a debugger for JIT on any iOS/iPadOS 13+. This birthed AltJIT by Riley Testut, JIT workaround by jkcoxson and Spidy123222, and Conath on Discord telling how to use detach on Xcode's debuger whilst keeping JIT capability. This allowed to have JIT on these versions with only problem being that if the program that has debug priviledges was put in the background it would lose the JIT capabilities. You would then have to activate again when you want to use a program with JIT or a debugger.

Q: Does iOS/iPadOS 17 still work with jit apps?

A: It does work but apple has changed how debugging works on iOS/iPadOS 17 making libraries like pymobiledevice3 to need to research how to debug on other platforms than macos. So that makes it harder to access jit for all the stuff that its used for.

## List

Since iOS 17 debugging is different. i will mark iOS 17 compatible programs for enabling jit only with ($). Not if the app can do its other functions.

**1. Sidestore by SideTeam
[_link_](https://sidestore.io)

Sidestore is a fork of altstore that is the sucessor to jitstreamer created via past iOS developers like jkcoxson, Joelle, joematt, spidy123222, nythepegasus, jjtech, naturecodevoided and now with nee developers to help out when they want to. The project aims to be a sideloading/jit method that works without needing a computer to do its functions.
You can also enable jit on sidestore same way as altstore. one of its goals is to be open about development and contributions. Sidestore doesnt need a paid developer account like jitterbug for using a on device vpn because it utilizes wireguard app to host the vpn and sidestore just acts as the wireguard server.

**2. Jitstreamer by jkcoxson and spidy123222

[_Link_](http://jitstreamer.com/)

This tutorial is written using a port of jitterbug which is a automation of rusty_libimobiledevice.
JitShipper works by using a pairFile you get from the jitExtractor and you connect via a vpn and grab the shortcut and pair via the shortcut and activate jit on apps listed. This requires no app other than zerotier one on the App Store for the vpn connection.


**3. JIT Workaround by Spidy123222 and jkcoxson**

[_Link_](https://jkcoxson.github.io/DiOS-Instructions/)

This tutorial is written using libimobiledevice which is a program to interface with iOS based Devices. This includes debugging/enabling JIT for apps.

*Note: all of the tutorials below use libimobiledevice. It is supported on Windows, Linux (x86 and Arm64), and macOS* 

This is considered to be a more compatible method of trying to activate JIT or debug, as it is well supported across many OS's. This can be implemented with an SSH shortcut to the computer to activate debugging remotely inside your network to activate JIT/debug (if computer is on). This method can be implimented easily to servers and portable devices.


**4. JitterBug by osy**

[_Link_](https://github.com/osy/Jitterbug)

Jitterbug is an iOS/iPad app that can debug/enable JIT via other Apple devices. There are a few methods, one being Jitterbug lite which allows a second iOS device to activate JIT on the first.

The second one which is just called Jitterbug **REQUIRES a paid Apple Developer account** to use. It creates a VPN to route debugging packets in a loopback from the iOS device to itself. Alternatively, you can use an Apple Testflight version but it is unclear if it will always be up and running. All of this info is applicable to JitterBug-Tutorial on the list number 3.


**5. Altstore by Riley Testut and Shang ($) = MacOS only**

[_Link_](https://github.com/rileytestut/AltStore)

This method uses AltStore (a computer is required to use) and is meant to be mostly automatic via AltJIT. All that is required is an install of AltStore on the computer that you plan to use as the JIT enabler. 

*Note: not all apps support AltJIT automatically, as it must be implimented by the developer of the app*

If an app doesnt use AltJIT; you can activate via the AltStore app by long pressing on the app and selecting `enable JIT`. This still requires a PC to activate an app manually from the AltStore app.

**6. pymobiledevice3 by doronz88 ($) = MacOS only**

[_Link_](https://github.com/iOSForensics/pymobiledevice)

Pymobiledevice is a library to imterface with iDevices. It is written in python and you can debug apps to enable jit.
