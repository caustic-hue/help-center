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
 - NodeJS 14 or above
 - Python 3.6 or above
 - Visual C++ Redistributable (on Windows)

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
FalixNodes Software uses Electron and Glasstron to run the app and uses Electron Builder to package it up nicely. Run the following commands to install them:
```
npm install electron@9.4.4
npm install glasstron@latest
npm install electron-builder@20.0.0
```

The reason why we use Electron 9.4.4 is because there are errors like `BrowserWindow not defined` or similar errors in Electron 10 and up. Also we use Electron Builder 20 because newer versions won't install properly on our end.

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