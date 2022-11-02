# pluget repository

## Source of truth

When downloading file or fetching data, you/your script should source the data in the following order:

Official Website > GitHub > GitLab > BitBucket > SpigotMC > Bukkit > PaperMC

Although this order can be ignored if the data is more accurate/in higher quality in certain source.

## Database structure

- `f` (first letter)
  - `full-name`
    - `data.json`
    - `spigot.json`
    - `versions`
      - `2.0.1` (version)
        - `data.json`
        - `spigot.json`

## Files and their structure

`data.json`
```jsonc
  {
    "name": "Full name of plugin",
    "icon": "99999AF", // icon: cid
    "license": "GPL-3.0-or-later", // license: spdx
    "archived": false,
    "gitUrl": "https://github.com/mbledkowski/name_of_plugin.git",
    "description": "The best plugin in the entire world", // description: short description
    "releaseDate": 1364368440, // optional if meta-package
    "updateDate": 1515903349 // optional if meta-package
  }
```

`readme.*` (e.g. `readme.md`, `readme.txt`)
```txt
  README file of the plugin.
```

`*.json` (e.g. `spigot.json`, `bukkit.json`, `github.json`)
```jsonc
  {
    "id": 213769, // optional if other than spigot/bukkit
    "url": "https://spigotmc.org/resources/213769",
    "name": "Full name of plugin - The best plugin in the fing world", // optional if other than spigot/bukkit 
    "description": "The best plugin in the world. Download right now.", // optional if other than spigot/bukkit
    "archived": false, // optional if custom website/spigot
    "authors": ["Slayer420"], // optional if custom website
    "icon": "666FFF", // optional if no icon, icon: cid
    "iconUrl": "https://www.spigotmc.org/data/resource_icons/9/9089.jpg", // optional if no icon
    "numberOfDownloads": 2115, // optional if other than spigot/bukkit
    "rating": 2, // scale 0-10; optional if other than spigot
    "numberOfVotes": 500, // optional if other than spigot
    "releasesPageUrl": "https://spigotmc.org/resources/213769/releases", // optional if custom
    "gitUrl": "https://github.com/mbledkowski/name_of_plugin/releases", // optional
    "donationUrl": "https://paypal.me/ineedmoney", // optional
    "releaseDate": 2137, // optional if other than spigot
    "updateDate": 2137, // optional if other than spigot
    "versions": ["1.18", "1.19"] // optional
  }
```
```jsonc
  {
    "url": "https://github.com/mbledkowski/name_of_plugin",
    "archived" false,
    "authors": ["mbledkowski"],
    "numberOfStars": 1400, //optional if other than github/gitlab
    "releasesPageUrl": "https://github.com/mbledkowski/name_of_plugin/releases"
  }]
```

`versions/*/data.json` (e.g. `versions/2.0.1/data.json`)
```jsonc
   "cid": "777AAA", // optional if meta-package (like EssentialsX)
   "supportedApis": ["spigot", "paper", "glowkit"], // optional
   "dependencies": ["essentialsx-core"], // optional
   "optionalDependencies": [], // optional, dependencies that are recommended for use with certain package
   "releaseDate": 1364392800, // earliest date of release
   "supportedVersions": ["1.19"] // optional, supported Minecraft versions
  }
```

`versions/*/*.json` (e.g. `versions/2.0.1/spigot.json`, `versions/2.0.1/github.json`)
```jsonc
  {
    "sourceUrl": "https://spigotmc.org/resources/213769/releases/2137",
    "downloadUrl": "https://spigotmc.org/resources/213769/releases/2137/plugin.jar",
    "numberOfDownloads": 5000,
    "rating": 2, // scale 0-10, float, optional if other than spigot
    "numberOfVotes": 500, // optional if other than spigot
    "releaseDate": 1364392800 // optional
  }
```
```jsonc
  {
    "sourceUrl": "https://github.com/mbledkowski/name_of_plugin/releases/2137",
    "downloadUrl": "https://github.com/mbledkowski/name_of_plugin/releases/2137/plugin.jar"
  }
```

## Contributing

Contributors are welcome, please fork and send pull requests!
If you found an error or have any ideas on how to improve this project please submit an issue.

