# Yesanith's Dalamud Plugins

A custom plugin repository for [Dalamud](https://github.com/goatcorp/Dalamud).
Add it once and every plugin below installs and updates like any other.

## Install

In game: `/xlsettings` → **Experimental** → paste into **Custom Plugin
Repositories**:

```
https://raw.githubusercontent.com/Yesanith/DalamudPlugins/main/repo.json
```

Tick **Enabled**, click **+**, then **Save and Close**. The plugins then appear
in `/xlplugins` under **All Plugins**.

## Plugins

| Plugin | What it does |
| --- | --- |
| [Regions of XIV](https://github.com/Yesanith/RegionsOfXIV) | Announces the region, zone, area and sub-area you walk into, with a styled, animated on-screen notification |

## Adding another plugin

`repo.json` is a JSON array — append one object per plugin. Most of the fields
are copied straight from the manifest the build produces next to the packaged
zip (`bin/x64/Release/<Name>/<Name>.json`); the rest are:

| Field | Value |
| --- | --- |
| `IconUrl` | a raw.githubusercontent URL to the plugin's `icon.png` |
| `DownloadLinkInstall` / `Update` / `Testing` | `https://github.com/Yesanith/<Plugin>/releases/latest/download/latest.zip` |
| `IsTestingExclusive` | `false` |

The download links use GitHub's *latest release* redirect, so they survive every
release without editing. `AssemblyVersion` is the one field that has to move
each time — it is what Dalamud compares to decide an update is available.

## Note

These are unofficial plugins, not affiliated with or endorsed by Square Enix.
Each carries its own licence in its own repository.
