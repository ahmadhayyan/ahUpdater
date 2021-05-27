# ahUpdater - Coming Soon
ahUpdater is a software updater to make your application easier to update and commercial ready. It's easy to set up, lightweight, customizable and user friendly.

## How to install
- Download ahUpdater [here](https://google.com)
- Unzip and put the files on your main application directory
- Change the `update.ini` to change the style and the text inside ahUpdater
- Create a `json` file on your server/website with this format :
```bash
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
- `app` : The application that will open when the update is finished (parameters/arguments can be used).
Example:
```bash
mainApplication.exe arg1 arg2 argN
```
Or just
```bash
mainApplication.exe
```
- `forceUpdate` : If set to false, after ahUpdater checking for updates the user gets to choose between update or cancel. If set to true, the user cannot choose cancel and the system will automatically update.
- `package` : The package can be as many as you like and you can also name it whatever you want to.

<br/>
### Implementation Example
```bash
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
<br/>

## How to use
- Call the ahUpdtr.exe with 2 parameters/arguments. The first arguments is your app current version and the second arguments is your json link.
Example:
```bash
ahUpdtr.exe 1.0 http://yourwebsite.com/version.json
```
