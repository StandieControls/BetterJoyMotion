<p align="center">
  <img src="title.png">
</p>

# BetterJoy: Motion Control Edition
Your Joy-Con pair will work as an Xbox 360 controller, with the addition of being able to press buttons by moving the Joy-Cons.

**Features:**

* Use left and right joy-con motions to activate buttons
* Want to map horizontal swipes to light attacks, vertical swipes to heavy attacks and forward thrusts to special attacks? You can!
* Use SL or SR to modify the motion control behavior, or map them to buttons directly
* Use an optional rumble setting to activate rumble whenever a motion input is used
* Unlike BetterJoy, the gyro aiming function is now solely controlled with the right joy-con in a pair



Warning: This adaption of BetterJoy is entirely focused on motion controls with Joy-Con pairs. Other features that are not related to using Joy-Con pairs as an Xbox 360 controller may have been broken and other controllers are not supported/tested.

If anyone would like to donate to the original creator of BetterJoy, [you can do so here](https://www.paypal.me/DavidKhachaturov/5). 

# How to use
1. Install drivers
    1. Read the READMEs (they're there for a reason!)
    1. Run *Drivers/ViGEmBus_Setup_1.16.116.exe*
    1. Restart your computer
2. Configure the .config file (preferably with an advanced text editor like Notepad++) or replace its content with one of the presets from the preset folder. Otherwise no motion controls will be mapped
3. Run *BetterJoyForCemu.exe* **If it crashes, there is likely an issue with your .config file and you should start over with one of the presets**
4. Connect your Joy-Cons **Always ensure that the right Joy-Con is connected first and the left Joy-Con is second, or there will be button issues**
5. Test whether your motion controls work in-game, [in your browser](https://hardwaretester.com/gamepad), or by activating the 'rumble on shake' feature in the .config file

### Screenshot
![Order Example](https://github-production-user-asset-6210df.s3.amazonaws.com/154834381/307151079-204e1cff-bcb6-4a28-8ae7-0ccef4e3d945.png?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240222%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240222T211124Z&X-Amz-Expires=300&X-Amz-Signature=08478d0972e694fb7c14dd66f07392d9b560168cf52f341fca4eed79a0b30006&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=0)

*This is the only correct order of joy-cons in BetterJoyMotion*

### Gameplay
https://github-production-user-asset-6210df.s3.amazonaws.com/154834381/307155706-2b93f30d-2dd0-4fd1-9ca5-ed9453f7a4b9.mp4?X-Amz-Algorithm=AWS4-HMAC-SHA256&X-Amz-Credential=AKIAVCODYLSA53PQK4ZA%2F20240222%2Fus-east-1%2Fs3%2Faws4_request&X-Amz-Date=20240222T212951Z&X-Amz-Expires=300&X-Amz-Signature=553c8b1138ff7477cdbe2ff306e1bbbefe72181e0241c1910e929f77373a3897&X-Amz-SignedHeaders=host&actor_id=0&key_id=0&repo_id=0

# Downloads
Go to the [Releases tab](https://github.com/StandieNL/BetterJoyMotion/releases)!

# More Info
Instructions on how to configure the motion controls are within the .config file.

You can check out the out the [wiki](https://github.com/Davidobot/BetterJoy/wiki) for more information about how to use the general version of BetterJoy, which may or may not be useful for using BetterJoyMotion.

BetterJoyMotion succeeds [my previous motion control application](https://github.com/StandieNL/Standies-Motion-Controls), which lacked the thumstick and rumble support that BetterJoy provided.

### The Future of BetterJoyMotion
This is a passion project of someone who can't code. I only managed to get it working by using ChatGPT and dozens of hours of trial and error. Any help from actual coders would be greatly appreciated. Freelancers are welcome to apply for modest compensation. 

Version 0.8 takes care of all the basic functions and some extras. There are still two major functions I want to add, but they have thus far proved too difficult. I also have various other cool features in mind, but it could take years to accomplish.
I'm honestly hoping Steam, reWASD or other remapping tools end up implementing their own motion control support so I can retire.

The future of the project also greatly depends on the compatibility of new superior motion controllers (like of the Switch 2), as they might make the regular Joy-Cons obsolete.

# Connecting and Disconnecting the Controller
## Bluetooth Mode
 * Hold down the small button (sync) on the top of the controller for 5 seconds - this puts the controller into broadcasting mode.
 * Search for it in your bluetooth settings and pair normally. I advise you to pair the right joy-con first for an easier experience with BetterJoyMotion
 * To disconnect the controller - hold the home button (or capture button) down for 2 seconds (or press the sync button). To reconnect - press any button on your controller.

## USB Mode
 * Plug the controller into your computer. (controllers other than joy-cons are not supported/tested in BetterJoyMotion
 
## Disconnecting \[Windows 10]
1. Go into "Bluetooth and other devices settings"
1. Under the first category "Mouse, keyboard, & pen", there should be the pro controller.
1. Click on it and a "Remove" button will be revealed.
1. Press the "Remove" button

# Building

**Note: My version is identical to the latest official BetterJoy, except for changes to joycon.cs and App.config**

## Visual Studio (IDE)

1. If you didn't already, install **Visual Studio Community 2019** via
   [the official guide](https://docs.microsoft.com/en-us/visualstudio/install/install-visual-studio?view=vs-2019).
   When asked about the workloads, select **.NET Desktop Development**.
2. Get the code project via Git or by using the *Download ZIP* button.
3. Open Visual Studio Community and open the solution file (*BetterJoy.sln*).
4. Open the NuGet manager via *Tools > NuGet Package Manager > Package Manager Settings*.
5. You should have a warning mentioning *restoring your packages*. Click on the **Restore** button.
6. You can now run and build BetterJoyMotion.

## Visual Studio Build Tools (CLI)
1. Download **Visual Studio Build Tools** via
   [the official link](https://visualstudio.microsoft.com/it/downloads/#build-tools-for-visual-studio-2019).
2. Install **NuGet** by following
   [the official guide](https://docs.microsoft.com/en-us/nuget/install-nuget-client-tools#nugetexe-cli).
   You should follow the section for ***nuget.exe***.
   Verify that you can run `nuget` from your favourite terminal.
3. Get the code project via Git or by using the *Download ZIP* button.
4. Open a terminal (*cmd*, *PowerShell*, ...) and enter the folder with the source code.
5. Restore the NuGet dependencies by running: `nuget restore`
6. Now build the app with MSBuild:
   ```
   msbuild .\BetterJoy.sln -p:Configuration=CONFIGURATION -p:Platform=PLATFORM -t:Rebuild
   ```
   The available values for **CONFIGURATION** are *Release* and *Debug*.
   The available values for **PLATFORM** are *x86* and *x64* (you want the latter 99.99% of the time).
7. You have now built the app. See the next section for locating the binaries.

## Binaries location
The built binaries are located under

*BetterJoyForCemu\bin\PLATFORM\CONFIGURATION*

where `PLATFORM` and `CONFIGURATION` are the one provided at build time. 

# Acknowledgements

All credit goes to:

[Davidobot](https://github.com/Davidobot) for creating the fantastic BetterJoy and answering my long-winded questions, as well as [everyone who helped create and improve it](https://github.com/Davidobot/BetterJoy/tree/master?tab=readme-ov-file#acknowledgements)

[tomayac](https://github.com/tomayac) for creating [chrome-dino-webhid](https://github.com/tomayac/chrome-dino-webhid) and helping me understand motion programming a bit better.

[SuperLouis64](https://github.com/SuperLouis64) for representing the fun of motion controls on [YouTube](https://www.youtube.com/@SuperLouis64).

This code also would not have been possible without ChatGPT.
