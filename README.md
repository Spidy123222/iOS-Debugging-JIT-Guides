By: Spidy123222
# Welcome to the List of Guides for Debugging/JIT on iOS/iPadOS 13+
This Page has List of Guides for Debugging and doing JIT on iOS/iPadOS 13+ but some of this can work in lower versions with less convinence by having to be tethered to a compter during the whole time so it is recommended to use these on iOS 13 and above.

**NOTICE: Currently All Below tutorials use a computer of some sort!**

## FAQ

**Q: Why would i need to use these?**

A: You would use these tutorials to debug on the go (Likely would need to keep logs somewhere) or use JIT for emulators or other things without being fully tethered to a computer on a developer liscenced app.

**Q: What is JIT?**

A: Having JIT is Required for most emulators and programs that use it because it recompiles the game or software in real-time for faster emulation. This can be useful for doing write and execution and reading for emulating a game or doing things in web-browsers like in safari.

**Q: What About Earlier Versions OF iOS/iPadOS that has native JIT support. Why doesnt current versions have it?**

A: iOS/iPadOS versions 14.4 and above are naturally incompatible with Non-Jailbroken versions of iOS/iPadOS due to the removal of Bugs to be able to debug an app for Just-in-time compilation (JIT) which programs like DolphiniOS and UTM uses. These apps can use these tutorial/programs below to do it on devices iOS/iPadOS 14.4 and above.

**Q: What Tricks were used back then to do jit and what are their restrictions and why was it removed?**

A: A few tricks were used and it wass removed all because it was bugs that could lead to security problems.

But one notible one that was used for jit was the ptrace() trick. Wich allowed to activate a debug from the app (ppsspp used this trick early on). This trick had a side effect of if you force close the app you would experience biggy behavior and not able to use the app again until you restart your idevice. This trick was used on iOS/iPadOS 13 versions and was patched on iOS/iPadOS 14

Using sandbox escapes, like phycicpaper exploit for iOS/iPadOS 13.4.1 and below. This allowed kernel access to features like safari's jit or more memory access which DolphiniOS took advantage of for their first non-jailbroken version of their app.

For a brief moment on iOS/iPadOS 14.2-14.3 there was a bug to use a debugger which allowed to add jit to apps similar to ptrace() but didnt need the restrictions or the command and set the app to have get-task-allow. This trick was utilized in a way where apps were natively supported to do JIT without much extra work or tricks for exiting apps to end the task.Only problem was this only supported devices with a A12 bionic chip and above which excluded devices with A11 bionic chips and below to not get any benifit.

Which while not long after A method was found to enable a debugger for JIT on any iOS/iPadOS 13+. Which birthed Altjit by riley testut, Jit workaround by jkcoxson and spidy123222,conath on discord telling how to use detach on xcode to activate UTM's jit and use anywhere after detaching.



## List

**1. JIT Workaround by Spidy123222 and Jkcoxson**

_Link:_ [https://github.com/jkcoxson/DiOS-Instructions](https://github.com/jkcoxson/DiOS-Instructions)

This tutorial is written with using libimobiledevice which is a program to interface with iOS based Devices. It includes debugging/Enabling Jit for apps and All of the tutorials below uses LibiMobileDevice. This program is supported on windows 10, debian linux, macOS 

This is considered the more compatible method if trying to activate jit or debug an app without mac or windows via debian linux or just want to do it via a computer. This can be implimented with a SSH shortcut to the computer to activate remotely inside your network to actiavte JIT/debug (if computer is on). This method can be implimented very well into servers and portable devices.


**2. JitterBug by osy**

_Link:_ [https://github.com/osy/Jitterbug](https://github.com/osy/Jitterbug)

Jitterbug is a iOS/iPad app that can debug/enable JIT via apple devices. There are few methods being jitterbug lite allowing to activate JIT with a second device to debug the main device for JIT. 

The second one just called jitterbug which REQUIRES Paid Apple Developer account to use which creates a vpn to route to the device your on to activate on you're device. you can use a testflight version but it is unclear if it will always be up and running. all of this info is applyable to JitterBug-Tutorial on the list number 2.


**3. JitterBug-Tutorial (unfinished) by Spidy123222 and Mangus_Redd**

_Link:_ [https://spidy123222.github.io/Jitterbug-tutorial](https://spidy123222.github.io/Jitterbug-tutorial)

This is a written tutorial for jitterbug to make it easier than the orignial without messing up the original instructions and making it easy to understand.


**4. Altstore by Riley Testut (In Patreon Beta or Build program youself)**

_Link:_ [https://github.com/rileytestut/AltStore](https://spidy123222.github.io/Jitterbug-tutorial)

This method uses Altstore (computer required to use) and is meant to be mostly automatic via AltJIT but not all apps might impliment or support it so most of what you need to do is install it install altstore to device.

If an app doesnt use AltJIT; you can activate via altstore app by long pressing on app and enable JIT or select altstore and go to enable JIT and select device and then app.
