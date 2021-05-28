# ahUpdater - Coming Soon
ahUpdater is a software updater to make your application easier to update and commercial ready. It's easy to set up, lightweight, customizable and user friendly.

<p align="center" style="display: flex;">
  <img src="img/ahUpdater.gif" width="568" height="609" alt="ahUpdater">
  <br/>
  <span style="max-width: 300px;">
    <img src="img/updateAvailable.png" width="283" height="302" alt="ahUpdater">
    <img src="img/downloadPackage.png" width="283" height="302" alt="ahUpdater">
  </span>
</p>

## Table of Contents
1. [How to Install](#how-to-install)
2. [How to Use](#how-to-use)

## How to install
- Download ahUpdater [here](https://google.com)
- Unzip and put the files on your main application directory
- Change the `update.ini` to change the style and the text inside ahUpdater
- Create a `json` file on your server/website with this format :
```json
[
    {
        "app": "",
        "forceUpdate": false,
        "package1": {
            "version": "",
            "url": ""
        },
        "package2": {
            "version": "",
            "url": ""
        },
        "packageN": {
            "version": "",
            "url": ""
        }
    }
]
```
#### A couple things about the json format :
- **app** : The application that will open when the update is finished (parameters/arguments can be used). Example: `mainApplication.exe arg1 arg2 argN` or just `mainApplication.exe`
- **forceUpdate** : If set to false, after ahUpdater checking for updates the user gets to choose between update or cancel. If set to true, the user cannot choose cancel and the system will automatically update.
- **package** : The package can be as many as you like and you can also name it whatever you want to.
- **version** : If you want to update your specific package, make sure the version is higher than your current application version. And vice versa if you don't want some package to be updated, make sure the version is lower or same as your current application version.
- **url** : Is the url to download your new package.

### Implementation Example
```json
[
    {
        "app": "mainApplication.exe",
        "forceUpdate": false,
        "package1": {
            "version": "1.1",
            "url": "http://yourwebsite.com/files/mainApplication.exe"
        },
        "package2": {
            "version": "1.1",
            "url": "http://yourwebsite.com/files/package2.zip"
        },
        "packageN": {
            "version": "1.0",
            "url": "http://yourwebsite.com/files/packageN.zip"
        }
    }
]
```

## How to use
- Call the ahUpdtr.exe with 2 parameters/arguments. The first arguments is your app current version and the second arguments is your json link. Call the ahUpdtr.exe without parent it to your main application, because you need to close your application after calling ahUpdtr.exe in order to update.
```batch
ahUpdtr.exe <your-app-current-version> <your-json-data-on-website>

::Example
::ahUpdtr.exe 1.0 http://yourwebsite.com/version.json
```
