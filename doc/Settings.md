# WinGet CLI Settings

You can configure WinGet by editing the `settings.json` file. The file can be open with the default json editor by running `winget settings`. If no editor is configure, notepad.exe will be used.

## File Location

Settings file is located in %LOCALAPPDATA%\Packages\Microsoft.DesktopAppInstaller_8wekyb3d8bbwe\LocalState\settings.json

If you are using the non-packaged winget version by building it from source code the file will be located under %LOCALAPPDATA%\Microsoft\WinGet\Settings\settings.json

## Source

These settings involve configuration to the WinGet source.

```
    "source": {
        "autoUpdateIntervalInMinutes": 3
    },
``` 

### autoUpdateIntervalInMinutes

A positive integer represents the update interval in minutes. The check for updates only happens when a source is used. A zero will disable the check for updates to a source. Any other values are invalid.

- Disable: 0
- Default: 5

To manually update the source use `winget source update`

## Visual

These settings involve visual elements that are displayed by WinGet

```
    "visual": {
        "progressBar": "accent"
    },
```

### progressBar

Color of the progress bar that WinGet displays when not specified by arguments. 

- accent (default)
- retro
- rainbow

### experimentalFeatures

In order to allow work to be done in master, and distributed to early adopters for their feedback, settings have the ability to control "experimental" features.

Currently there are no experimental features, just sample ones. Once they get implemented this file will be updated.

```
   "experimentalFeatures": {
       "experimentalCmd": true,
       "experimentalArg": false,
   },
```
