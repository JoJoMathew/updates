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

### Values
- latestVersion: Required.

- latestVersionCode: Optional.

- url: Required.

- releaseNotes: Optional.

### Note:
If latestVersionCode is included in the XML, latestVersion will only be used to display the latest version in the dialog and the versionCode will be used to compare the installed and latest update.
