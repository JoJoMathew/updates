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

### Adding release notes
```xml
<AppUpdater>
  <update>
    <latestVersion>1.2.2</latestVersion>
    <latestVersionCode>10</latestVersionCode>
    <url>https://github.com/javiersantos/AppUpdater/releases</url>
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

### Note:
If latestVersionCode is included in the XML, latestVersion will only be used to display the latest version in the dialog and the versionCode will be used to compare the installed and latest update.
