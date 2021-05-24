---
layout: default
title:  "Building"
parent: Software
grand_parent: Falix
permalink: /falix/software/building/
tags: Falix software building source code electron
---

# Preparing to Build
## Requirements
 - [NodeJS](https://nodejs.org/en/) 14.16.0 or above
 - [Python](https://www.python.org/) 3.9 or above
 - [Visual Studio Community](https://visualstudio.microsoft.com/) (Install Desktop Development with C++) (on Windows)
 - [Visual C++ Redistributable](https://support.microsoft.com/en-us/topic/the-latest-supported-visual-c-downloads-2647da03-1eea-4433-9aff-95f26a218cc0) (on Windows)
 - At least 8GB of storage

## Downloading Source Code
### Using Git
If you have Git already installed, run the following command to download and automatically extract the source code from our GitHub:
```
git clone https://github.com/FalixNodes-Software/Desktop-App/
```

### Using GitHub CLI
If you have GitHub CLI already installed, run the following command to download and automatically extract the source code from our GitHub:
```
gh repo clone FalixNodes-Software/Desktop-App
```

If you don't have Git or GitHub CLI installed, you can download it manually from our [GitHub](https://github.com/FalixNodes-Software/Desktop-App/) or install [Git](https://git-scm.com/) or install [GitHub CLI](https://cli.github.com/).

# Building
## Installing Dependencies
FalixNodes Software uses Electron and other required packages to run the app and uses Electron Builder to package it up nicely. Run the following commands to install them:
```
npm install install
```

Make sure Electron says `^9.4.4` in the __package.json__, everything else can be updated to it's latest version.

The reason why we use Electron 9.4.4 is because the new terminal built-in won't work properly on later versions of Elecron.

Make sure Electron Builder are under `devDependencies` in the __package.json__ file or it will refuse to build.

## Running
After all required dependencies are installed, you should be able to run the software with the start command provided in __package.json__.

To run the start command, simply run the following command:
```
npm start
```

## Create a Package
Wanna create an installer? You can do this with Electron Builder, there is already a build command ready which is provided in __package.json__.

To start building the installer, run the following command: 
```
npm run build
```

NOTE: If you're using versions of Windows older than Windows 10, please change `appx` to `exe` in the build configuration found in __package.json__, `appx` files are for Windows 10 only.

If you're using Windows 10, Electron may have some issues building the APPX file, as we don't use Electron Builder for Window 10.