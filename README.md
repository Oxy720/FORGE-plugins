# FORGE-plugins Registry

Central registry for FORGE panel plugins. This repository hosts the plugin definitions that the FORGE panel fetches to discover and install available plugins.

## About

The FORGE-plugins registry is a JSON-based plugin database that the [FORGE panel](https://github.com/Oxy720/FORGE) uses to:
- Discover available plugins
- Fetch plugin metadata and descriptions
- Download and install plugins
- Check for plugin updates

## Registry Structure

The registry is defined in `registry.json`:

```json
{
  "id": "plugin-id",
  "repoOwner": "Oxy720",
  "repoName": "plugin-repository-name",
  "repoPath": "path/to/plugin"
}
```

Each entry points to a separate GitHub repository where the plugin lives.

## Current Plugins

| ID | Repository | Description |
|---|---|---|
| **mold** | [mold](https://github.com/Oxy720/mold) | Create folder templates inside Premiere Pro projects |

## Adding a Plugin

To add a new plugin to the registry:

1. Create a plugin repository under the `Oxy720/` GitHub account with a valid CEP extension structure
2. Add an entry to `registry.json` with the plugin ID, repo owner, and repo name
3. Submit a pull request with the updated registry

### Plugin Repository Requirements

Each plugin repository must contain:
- Valid CEP panel structure (CSXS folder with manifest.xml)
- Plugin manifest with metadata (name, version, description)
- Installation and usage instructions in README.md
- Source code and assets

## How FORGE Uses This Registry

The FORGE panel queries `registry.json` to:
1. Fetch the list of available plugins
2. For each plugin, clone or download the repository
3. Extract plugin metadata from the manifest
4. Display available plugins in the panel UI
5. Enable one-click installation directly into Premiere Pro

## Registry URL

```
https://raw.githubusercontent.com/Oxy720/FORGE-plugins/main/registry.json
```

This URL is referenced in the FORGE panel configuration.

## Support

For issues or feature requests:
- FORGE Panel: https://github.com/Oxy720/FORGE
- MOLD Plugin: https://github.com/Oxy720/mold

---

Built with assistance. Optimized for post-production workflows.
