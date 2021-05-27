# ahUpdater
### Coming Soon
ahUpdater is a software updater to make your application easier to update and commercial ready. It's easy to set up, lightweight, customizable and user friendly.

## How to install
- Download ahUpdater [here](https://google.com)
- Unzip and put the files on your main application directory
- Change the update.ini to change the style and the text inside ahUpdater
- Create json file on your server/website with this format

<json_format>

### information
- app : the application that will open when the update is finished (parameters/arguments can be used). (E.g. "mainApplication.exe arg1 arg2 argN" or just "mainApplication.exe")
- forceUpdate : if set to false, after ahUpdater checking for updates the user get to choose between update or cancel. If set to true, the user cannot choose cancel and the system will automatically update.

## How to use
- Call the ahUpdtr.exe with 2 parameters/arguments. The first arguments is your app current version and the second arguments is your json link. (E.g. "ahUpdtr.exe 1.0 http://yourwebsite.com/version.json")
