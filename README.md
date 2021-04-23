# DolphinSampleUWP

A port of the classic Dolphin Xbox XDK sample to UWP, based on Joshua-Ashton's [Win32 port](https://github.com/Joshua-Ashton/Dolphins), which in turn is based on the public [front-buffer Xbox One XDK sample](https://github.com/microsoft/Xbox-ATG-Samples/tree/master/XDKSamples/System/FrontPanelDolphin) part of Xbox-ATG-Samples.

Runs on Windows and Xbox One/Series X|S, since it's a UWP application.

## Prerequisites

[Visual Studio 2015*, 2017 or 2019*](https://visualstudio.microsoft.com/vs/older-downloads/) with UWP development workload installed. (Basically the requirements for the UWP compiling from Xbox-ATG-Samples)
Visual Studio 2017 or higher is recommended, but *both 2015 and 2019 have not been tested.

DirectXTK and ATGTK are already included.

If you want to deploy this app to Xbox, you will need to have joined the Xbox Creators Program, and have activated your Xbox console through the [Xbox Dev Mode](https://www.microsoft.com/en-us/p/xbox-dev-mode/9nljhzjrn0f4) app. If you have activated your console before 9/30/2020, you will need to download the newer app, as the original Xbox One app no longer seems to work properly.

It has not been tested, but an up-to-date Xbox One/Series X|S XDK unit (likely acquired and activated through ID@Xbox) should also work.

## Note

During the pieceing together and troubleshooting of this solution, I have had to remove the ARM, ARM64, and x86 platforms from it, but they can likely be easily added back in.

## Compiling

If needed, change Configuration to Debug. 

If deploying to Xbox, go to DolphinSample > Configuration Properties > Debugging.

Change "Debugger to launch:" to Remote Machine, or change it in the dropdown menu in the main window. By default, Machine Name is set to XBOXONE. If your Xbox has a different name, or you purely rely on inputting an IP address, input it here.

Press the "Start Debugging" button, which should say either "Local Machine" or "Remote Machine", and the solution will compile and deploy.

## Controls

### Gamepad (Xbox Controller)

View button: Exit sample

### Keyboard

Esc: Exit sample

## To-Do

As observed in the [Project Scorpio Xbox Development Kit video](https://www.youtube.com/watch?v=KfARlsRtdPY&t=268s), the Xbox-ATG-Samples version of the demo has the following features missing:

* Add/delete dolphins (max 4 dolphins)

* Wireframe mode

So far, I cannot figure out how to implement the former feature, due to use of arrays, and my lack of understanding of. Wireframe mode might be straightforward though. But apparently, this is because I used the FrontPanelDolphin version, while the full version they were using is in FrontPanelDemo. Oops. Expect another large commit soon-ish? 

Additionally, I want to add these features:

* Extra modes that simulate the older Xbox and Xbox 360 versions

* Text at the top saying "DolphinSampleUWP" to the left, and text to the right indicating the FPS, similar to the older samples.

Any help implementing these features would be apreciated, especially the top two. Please use own-made implementations, or ones under the same license, though!

## Screenshots

### Windows 10
![DolphinSampleUWP 3_17_2021 8_33_48 PM](https://user-images.githubusercontent.com/22670693/111577101-adb74e80-877f-11eb-8f0a-ebac4c20c9f6.png)

### Xbox One (S)
![Screenshot_2021-03-17_23-47-10](https://user-images.githubusercontent.com/22670693/111577205-d93a3900-877f-11eb-8f63-c5fd10e9a712.png)

### Very important notice

These dolphins will never threaten to stab you, and in-fact, cannot speak.

All jokes aside, though...

### Notice

This repository is based on code from publically available GitHub repositories made by Microsoft Corporation, and has been released under the MIT License. This repository is in no part affiliated with the company, other than being the original authors. Regardless, no illegal activity is intended, since I'm just making this sample available in a more modern plaform for everyone to use, and due to the original license terms of the public Microsoft repository.

Microsoft, Windows, Xbox, and all other related terms are property of Microsoft Corporation, and are presumed to be used under fair use. 
