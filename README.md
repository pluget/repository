# repository

## Source of truth

When downloading file, or taking data, you / script should source data in the following order:
Official Website > GitHub > GitLab > BitBucket > SpigotMC > Bukkit > PaperMC

## Design (DB structure)

`data.json`
```jsonc
  {
    "name": "Full name of plugin",
    "icon": "99999AF", // icon: cid
    "license": "GPL-3.0-or-later", // license: spdx
    "archived": false,
    "gitUrl": "https://github.com/mbledkowski/name_of_plugin.git",
    "description": "The best plugin in the entire world", // description: short description
    "data": [{
      "id": 213769, // if other than spigot/bukkit then optional
      "type": "spigot",
      "url": "https://spigotmc.org/resources/213769",
      "name": "Full name of plugin - The best plugin in the fing world", // optional
      "description": "The best plugin in the world. Download right now.", // optional
      "archived": false, // optional for custom websites
      "authors": ["Slayer420"], // optional for custom websites
      "icon": "666FFF", // optional, icon: cid
      "iconUrl": "https://www.spigotmc.org/data/resource_icons/9/9089.jpg" // optional
      "numberOfDownloads": 2115, // optional for other than spigot/bukkit
      "rating": 2, // scale 0-10; optional for other than spigot
      "numberOfVotes": 500, // optional for other than spigot
      "releasesPageUrl": "https://spigotmc.org/resources/213769/releases" // optional for custom
    }, {
      "type": "github",
      "url": "https://github.com/mbledkowski/name_of_plugin",
      "archived" false,
      "authors": ["mbledkowski"],
      "numberOfStars": 1400, //optional for other than github/gitlab
      "releasesPageUrl": "https://github.com/mbledkowski/name_of_plugin/releases"
    }]
  }
```

`versions.json`
```jsonc
   {
      "about": [{
      "type": "github",
      "sourceUrl": "https://github.com/mbledkowski/name_of_plugin/releases/2137",
      "downloadUrl": "https://github.com/mbledkowski/name_of_plugin/releases/2137/plugin.jar",
    }, {
      "type": "spigot",
      "sourceUrl": "https://spigotmc.org/resources/213769/releases/2137",
      "downloadUrl": "https://spigotmc.org/resources/213769/releases/2137/plugin.jar",
      "numberOfDownloads": 5000,
      "rating": 2, // scale 0-10, optional for other than spigot
      "numberOfVotes": 500, // optional for other than spigot
    }],
    "cid": "777AAA", // optional for meta-packages (like EssentialsX)
    "supportedApis": ["spigot", "paper", "glowkit"], // optional
    "dependencies": ["essentialsx-core"], // optional
    "optionalDependencies": [], // optional, dependencies that are recommended for use with certain package
    "supportedVersions": ["1.19"] // optional, supported Minecraft versions
  }
```

## Contributing

Contributors are welcome, please fork and send pull requests! If you find a bug
or have any ideas on how to improve this project please submit an issue.

