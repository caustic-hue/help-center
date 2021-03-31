---
layout: default
title:  "Setting Up"
date:   2021-03-31 01:58:53 -0400
nav_order: 1
author: Korbs
parent: Software
grand_parent: FalixNodes
permalink: /falixnodes/software/setting-up/
tags: falixnodes software download
---

> This article is still a work in progress

# Installing Process
FalixNodes Software is built on Electron, meaning it's cross-platform and supports Windows, macOS, Linux, and ChromeOS. The installation is easy to follow and you should of the software installed within at least 2 minutes or less(depending on your internet speed).

## Windows 10
You can install the software easily in the Microsoft Store on Windows 10\. Just search "FalixNodes" and the software should show up. Select it and click install.

or you can click here:

<a href="https://www.microsoft.com/en-us/p/falixnodes-software/9p5mmnfs825p"><img width="250px" src="https://developer.microsoft.com/en-us/store/badges/images/English_get-it-from-MS.png"></a>

## macOS

Due to restriction with Apple, the software is not available in the App Store, but we have provided a DMG option instead.

If you're using macOS, click the download button on the software website. A DMG file will be provided. Open the DMG file and simply drag the FalixNodes app into the Applications folder.

## Linux
On Linux, there are many ways to install software like apt, [deb](https://en.wikipedia.org/wiki/Deb_(file_format)), [rpm](https://en.wikipedia.org/wiki/RPM_Package_Manager), [pacman](https://en.wikipedia.org/wiki/Arch_Linux#Pacman), etc. We've chosen the Snapstore for easy distrubing and to make it easy to add auto updating.

Use the following commands to install Snap on your distro(Snap comes pre-installed on Pop OS, Fedora, and Ubuntu):

Also note, if you're using Fedora, replace `apt` with `dnf` instead.

```
sudo apt install snapd
sudo snap install falixnodes
```

# Updating
## Windows 10
Since FalixNodes Software is available in the Microsoft Store, you can easily manage updates.

[Learn how to updates app on Windows 10](https://support.microsoft.com/en-us/account-billing/get-updates-for-apps-and-games-in-microsoft-store-a1fe19c0-532d-ec47-7035-d1c5a1dd464f)

## macOS
Auto updating is still not available for macOS users, you'll need to manually install new updates. When a new update is available, just re-download FalixNodes and install the newer version.

## Linux
Since FalixNodes Software is available in the Snapstore, you can easily update. For some distros, the update might be available through the app store included with your distro, if this isn't the case, try the following command:

```
sudo snap refresh falixnodes
```

# Uninstalling Process

# Troubleshooting
## Stuck on advertisement in Game Panel or Client Panel
If you've misclicked on an advertisement in the Client Panel, there is no way to back out. Controls currently don't work properly in the Client tab, you'll need to reload the software. You can reload the software by pressing Ctrl R or clicking the reload button found at the bottom of the Settings tab.

If you've misclicked on an advertisement in the Game Panel, click the back button. If for whatever reason this isn't working, click the kill button(x button) and load the panel again.

## Software is not opening
For Linux users, assuming you installed from Snap, Snap apps can take a moment to open as they're being sandboxed. The first boot will take longer. If you're not using Snap and choice to build the software instead, there may of been an error. Please read and troubleshoot any errors that show up on in your terminal.

For Windows users, please check your task manager and see if FalixNodes Software is running. Since it's built on Electron, you may see a few instances of it running. You can kill the process and try again, if it's not working on the second try, you can try re-installing the software.

## FalixNodes Software caused BSOD on Windows
This issue has been reported a few times, but has not ben seen by Korbs(developer). If for whatever reason this does happen, please let us know.

## The sidebar is completely transparent
You can adjust the transpancy of the sidebar in your Apperances setting, select at least 60% - 100% for the opacity. If the setting isn't working for whatever reason, please report an issue

# Troubleshooting - Building
These are issues you may get while building the software from GitHub

## Glasstron not found or not defined
Glasstron is widely used in the software, you'll need to make sure you've installed it's dependency. To install Glasstron, use the following command:

```
npm install glasstron
```

## Electron and/or BrowserView not defined
This will occur if you've choosen Electron v10 and up. Please only use Electron v9.0.0 - v9.4.3\. Run the following commands:

```
npm uninstall electron
npm install electron@9.4.3
```

This issue is the reason why we use Electron v9.

## Electron Builder has errors while installing
We're not sure what's causing the issue either, please try installing an older version of Electron Builder instead. In our case, we just use:

```
npm install electron-builder@20.0.0
```

Electron Builder v20 still has all the features we need to build FalixNodes Software, with no issues.

## Appx file won't open
If you've built a APPX file on Windows 7 or Windows 8.1, this file can't be used. APPX file is built for Windows 10 only.

[What's an APPX file?](https://help.falixnodes.net/article/falixnodes/software/faq-for-developers/)

## Appx file won't let me install on Windows 10
We recommend that you actually EXE format instead of APPX. Please change the target under Windows to "nsis". NSIS will provide a EXE setup file.

If you want to use Appx, keep reading:

Assuming you've tried to build a Appx file with Electron Builder, we didn't use this. We use Electron Windows Store dependency instead, we use the following command to build:

```
electron-windows-store --input-directory C:\Users\YOURUSERNAMEHERE\Documents\Desktop-App\dist\win-unpacked  --output-directory C:\FalixNodes-Software\ --package-version 2.3.31.1 --package-name falixnodes --publisher-display-name "Korbs Studio" --identity-name "32203KorbsStudio.FalixNodesSoftware" --package-display-name "FalixNodes Software" --assets C:\Users\YOURUSERNAMEHERE\Documents\assets
```

You'll need to setup and change some of these paths and download assets for the Windows 10 version. Also, please do use Electron Builder to unpack the app(usually creates a win-unpacked folder)