By: Spidy123222
# Welcome to the List of Guides for Debugging/JIT on iOS/iPadOS 13+
This Page has List of Guides for Debugging and doing JIT on iOS/iPadOS 13+ but some of this can work in lower versions with less convinence by having to be tethered to a compter during the whole time so it is recommended to use these on iOS 13 and above.

## FAQ

**Q: Why would i need to use these?**

A: You would use these tutorials to debug on the go (Likely would like to keep logs somewhere) or use JIT for emulators or other things without being fully tethered to a computer on a developer liscenced app.

**Q: What is JIT?**

A: Having JIT is Required for most emulators and programs that use it because it recompiles the game or software in real-time for faster emulation. This can be useful for doing write and execution and reading for emulating a game or doing things in web-browsers like in safari.

**Q: What About Earlier Versions OF iOS/iPadOS that has native JIT support?**

A: iOS/iPadOS versions 14.4 and above are naturally incompatible with Non-Jailbroken versions of DolphiniOS due to the removal of Bugs to be able to debug an app for Just-in-time compilation (JIT) which programs like DolphiniOS and UTM uses. These apps can use these tutorial/programs below to do it on devices iOS/iPadOS 14.4 and above.


## List

**1. JIT Workaround by Spidy123222 and Jkcoxson**

_Link:_ [https://github.com/jkcoxson/DiOS-Instructions](https://github.com/jkcoxson/DiOS-Instructions)

This tutorial is written with using libimobiledevice which is a program to interface with iOS based Devices. It includes debugging/Enabling Jit for apps and All of the tutorials below uses LibiMobileDevice. This is considered the more compatible method if trying to activate jit or debug an app without mac or windows or just want to do it via a computer. This can be implimented with a SSH shortcut to the computer to activate remotely inside your network to actiavte JIT/debug (if computer is on). This method can be implimented very well into servers and portable devices.

**2. JitterBug by osy**

_Link:_ [https://github.com/osy/Jitterbug](https://github.com/osy/Jitterbug)

Jitterbug is a iOS/iPad app that can debug/enable JIT via apple devices. There are few methods being jitterbug lite allowing to activate JIT with a second device to debug the main device for JIT. The second one just called jitterbug which REQUIRES Paid Apple Developer account to use which creates a vpn to route to the device your on to activate on you're device. you can use a testflight version but it is unclear if it will always be up and running. all of this info is applyable to JitterBug-Tutorial on the list number 2.

**3. JitterBug-Tutorial by Spidy123222 and Mangus_Redd**

_Link:_ [https://spidy123222.github.io/Jitterbug-tutorial](https://spidy123222.github.io/Jitterbug-tutorial)

This is a written tutorial for jitterbug to make it easier than the orignial without messing up the original instructions and making it easy to understand.

**4. Altstore by Riley Testut (In Patreon Beta or Build program youself)**

_Link:_ [https://github.com/rileytestut/AltStore](https://spidy123222.github.io/Jitterbug-tutorial)

This method uses Altstore and is meant to be mostly automatic via AltJIT but not all apps might impliment or support it so most of what yuo need to do is install it install altstore to device. If an app doesnt use AltJIT; you can activate via altstore app by long pressing on app and enable JIT or select altstore and go to enable JIT and select device and then app.
