# JoJoLauncher Auto Update 
JoJoLauncher will check for a .xml file at https://raw.githubusercontent.com/jojomamanbebe/updates/master/update.xml, It will then compare the version number in the XML file to the version number of the App installed and if there is a newer version available it will prompt the user to download and install the new apk. Examples of the XML file format can be found below.

### Example XML
```xml
<AppUpdater>
  <update>
    <latestVersion>1.2.2</latestVersion>
    <latestVersionCode>10</latestVersionCode>
    <url>https://github.com/jojomamanbebe/JoJoLauncher/releases</url>
  </update>
</AppUpdater>
```

### Adding Release Notes
```xml
<AppUpdater>
  <update>
    <latestVersion>1.2.2</latestVersion>
    <latestVersionCode>10</latestVersionCode>
    <url>https://github.com/jojomamanbebe/JoJoLauncher/releases</url>
    <releaseNotes>
- First Note
- Second Note
- Bug fixes
- Etc Etc..
    </releaseNotes>
  </update>
</AppUpdater>
```

### Values
- latestVersion: Required.

- latestVersionCode: Optional.

- url: Required.

- releaseNotes: Optional.

### Customizing The Title, Description, Buttons & More
• You can customise the pop-up shown to the stores, available options are:

```java
new AppUpdater(this)
	.setTitleOnUpdateAvailable("Update available")
	.setContentOnUpdateAvailable("Check out the latest version available of my app!")
	.setTitleOnUpdateNotAvailable("Update not available")
	.setContentOnUpdateNotAvailable("No update available. Check for updates again later!")
	.setButtonUpdate("Update now?")
	.setButtonUpdateClickListener(...)
	.setButtonDismiss("Maybe later")
	.setButtonDismissClickListener(...)
	.setButtonDoNotShowAgain("Huh, not interested")
	.setButtonDoNotShowAgainClickListener(...)
	.setIcon(R.drawable.ic_update) // Notification icon 
	.setCancelable(false) // Dialog could not be dismissable
	...
```

### Notes:
*If latestVersionCode is included in the XML, latestVersion will only be used to display the latest version in the dialog and the versionCode will be used to compare the installed and latest update.*

