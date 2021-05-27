# ahUpdater
### Coming Soon
ahUpdater is a software updater to make your application easier to update and commercial ready. It's easy to set up, lightweight, customizable and user friendly.

## How to install
- Download ahUpdater [here](https://google.com)
- Unzip and put the files on your main application directory
- Change the `update.ini` to change the style and the text inside ahUpdater
- Create json file on your server/website with this format :
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
Note that the `package` is can be as many as you like.
### information
- `app` : The application that will open when the update is finished (parameters/arguments can be used).
Example:
```bash
mainApplication.exe arg1 arg2 argN
```
Or just
```bash
mainApplication.exe
```
- `forceUpdate` : If set to false, after ahUpdater checking for updates the user get to choose between update or cancel. If set to true, the user cannot choose cancel and the system will automatically update.

## How to use
- Call the ahUpdtr.exe with 2 parameters/arguments. The first arguments is your app current version and the second arguments is your json link.
Example:
```bash
ahUpdtr.exe 1.0 http://yourwebsite.com/version.json
```
