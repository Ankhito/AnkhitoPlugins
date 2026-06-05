# Sekhmet Plugins

Dalamud custom repository for SekhmetAnkh plugins.

Add this URL in Dalamud's Custom Plugin Repositories list:

```text
https://raw.githubusercontent.com/SekhmetAnkh/SekhmetPlugins/main/pluginmaster.json
```

## Plugins

- PositionalPilot: assistive, safety-gated melee positional movement.
- GBR Monster Hunter: routes to drop-only materials from GatherBuddy Reborn/Vulcan crafting plans.

## Updating

`pluginmaster.json` is generated from the plugin repositories listed in `plugins.json`.
The updater reads each plugin's source manifest for static metadata, reads the
published release zip for generated Dalamud manifest fields, and writes pinned
GitHub release asset URLs.

Run the updater manually with:

```powershell
./scripts/Update-PluginMaster.ps1
```

Plugin release workflows can dispatch the updater when they define a
`SEKHMETPLUGINS_DISPATCH_TOKEN` secret with access to this repository.
